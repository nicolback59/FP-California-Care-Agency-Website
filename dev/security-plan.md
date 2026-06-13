# Security Plan
## California Care Agency Website

**Version:** 1.0
**Date:** 2026-06-13
**Standard:** WordPress Security Best Practices + OWASP Top 10 awareness

---

## Security Priority Matrix

| Risk | Likelihood | Impact | Mitigation |
|------|-----------|--------|------------|
| Brute force login attacks | High | High | Rate limiting, hidden login URL, strong passwords |
| Outdated plugin vulnerabilities | Medium | High | Auto-updates (minor), manual updates (major) |
| Spam form submissions | High | Medium | CAPTCHA, honeypot fields |
| SQL injection | Low | Critical | WordPress core protection + Wordfence WAF |
| XSS attacks | Low | High | Wordfence WAF + sanitized inputs |
| Unauthorized portal access | Medium | High | Role-based access, authentication checks |
| Sensitive data exposure | Low | Critical | No HIPAA data on site; proper file permissions |
| Malware injection | Low | Critical | Malware scanner, file integrity monitoring |
| DDoS attacks | Low | High | Cloudflare (recommended) or hosting-level protection |

---

## SSL / HTTPS

```
Requirement: MANDATORY before any page goes live

Implementation:
- Obtain SSL certificate (Let's Encrypt — free, or hosting-provided)
- Force HTTPS redirect (301) for all HTTP requests
- HSTS header: Strict-Transport-Security: max-age=31536000; includeSubDomains

WordPress configuration:
- Set WordPress Address and Site Address to https://
- Add to wp-config.php:
  define('FORCE_SSL_ADMIN', true);

Test with: https://www.ssllabs.com/ssltest/
Target grade: A or A+
```

---

## WordPress Core Hardening

### wp-config.php Security Settings

```php
// Security keys (generate at: https://api.wordpress.org/secret-key/1.1/salt/)
define('AUTH_KEY',         'UNIQUE_KEY');
define('SECURE_AUTH_KEY',  'UNIQUE_KEY');
define('LOGGED_IN_KEY',    'UNIQUE_KEY');
define('NONCE_KEY',        'UNIQUE_KEY');
define('AUTH_SALT',        'UNIQUE_KEY');
define('SECURE_AUTH_SALT', 'UNIQUE_KEY');
define('LOGGED_IN_SALT',   'UNIQUE_KEY');
define('NONCE_SALT',       'UNIQUE_KEY');

// Disable file editing via WP Admin
define('DISALLOW_FILE_EDIT', true);

// Limit post revisions
define('WP_POST_REVISIONS', 5);

// Force SSL for admin
define('FORCE_SSL_ADMIN', true);

// Disable debug output on production
define('WP_DEBUG', false);
define('WP_DEBUG_LOG', false);
define('WP_DEBUG_DISPLAY', false);
```

### File Permissions

```
Directory permissions: 755 (owner: read/write/execute; others: read/execute)
File permissions:       644 (owner: read/write; others: read)
wp-config.php:          640 (owner: read/write; group: read; others: none)
.htaccess:              644

NEVER set to 777 — any plugin that requires 777 is a security red flag.
```

### .htaccess Hardening

```apache
# Protect wp-config.php
<files wp-config.php>
  order allow,deny
  deny from all
</files>

# Disable directory browsing
Options -Indexes

# Block access to sensitive files
<FilesMatch "^(wp-config\.php|readme\.html|license\.txt|xmlrpc\.php)">
  Order Deny,Allow
  Deny from All
</FilesMatch>

# Block XML-RPC (if not needed)
<Files xmlrpc.php>
  Order Deny,Allow
  Deny from All
</Files>

# Prevent PHP execution in uploads directory
<Directory "/wp-content/uploads">
  <Files "*.php">
    Order Deny,Allow
    Deny from All
  </Files>
</Directory>
```

---

## Login Security

### Login URL Obfuscation

```
Plugin: WPS Hide Login
Default /wp-admin/ → Custom URL (e.g., /staff-access/)
Stores in database — not in .htaccess
IMPORTANT: Save the custom URL. If forgotten, recover via FTP/database.
```

### Brute Force Protection

```
Plugin: Limit Login Attempts Reloaded (or Wordfence built-in)
Settings:
- Allowed attempts before lockout: 3
- Lockout duration: 30 minutes
- Long lockout after: 4 lockouts
- Long lockout duration: 24 hours
- Email admin after lockout: Yes
```

### Password Policy

```
Plugin: ProfilePress (for employee accounts) or Password Policy Manager
Requirements:
- Minimum 12 characters
- Uppercase + lowercase
- At least 1 number
- At least 1 special character

Enforce via: ProfilePress registration form validation
Admin accounts: Use a password manager (1Password, Bitwarden) for 20+ character passwords
```

### Two-Factor Authentication (2FA)

```
Plugin: WP 2FA (free) or Wordfence 2FA
Apply to: Administrator and Manager roles (REQUIRED)
Employee role: Recommended, optional at launch

Method options:
- TOTP authenticator app (Google Authenticator, Authy) — Recommended
- Email one-time code — Secondary option
```

---

## Wordfence Configuration

### Installation Steps

```
1. Install Wordfence Security from WordPress plugin directory
2. Activate and enter license key (free license is fine for launch)
3. Run initial scan
4. Configure firewall:
   - Mode: Extended Protection (requires .htaccess modification)
   - Auto-update WAF rules: Enabled
5. Configure scan schedule: Weekly minimum
6. Configure alerts: Security-level events email to admin
```

### Wordfence Settings Checklist

```
Firewall:
✅ Web Application Firewall: Enabled, Extended Protection
✅ Brute force protection: Enabled
✅ Rate limiting: Enabled
✅ Block fake Googlebots: Enabled

Scan:
✅ Scan public-facing files for malware
✅ Scan core files against WordPress.org repository
✅ Scan themes and plugins against repository
✅ Check if site is blocklisted

Login Security:
✅ 2FA for administrators (required)
✅ CAPTCHA on login and registration
✅ Password strength checker

Notifications:
✅ Email: All critical alerts
✅ Email: Security scan results (weekly)
```

---

## Role-Based Permissions

### WordPress User Roles

| Role | WP Admin Access | Frontend Access | Portal Access |
|------|----------------|-----------------|---------------|
| Administrator | Full | All pages | /admin-portal/ + /employee-portal/ |
| Manager | Limited (no theme/plugin) | All pages | /employee-portal/ + limited /admin-portal/ |
| Employee | None | Public pages only | /employee-portal/ |
| Subscriber | None | Public pages only | None |
| Pending (custom) | None | Public pages only | None |

### Content Restriction Rules (Members Plugin)

```
Restrict by role on each private page:

Page: /employee-portal/*
  → Allowed: Employee, Manager, Administrator
  → Redirect if unauthorized: /login/?redirect_to=%s

Page: /admin-portal/*
  → Allowed: Administrator, Manager
  → Redirect if unauthorized: /login/?redirect_to=%s

Page: All public pages
  → Allowed: Everyone (no restriction)
```

---

## Search Engine Blocking for Private Pages

### robots.txt

```
User-agent: *
Disallow: /employee-portal/
Disallow: /admin-portal/
Disallow: /login/
Disallow: /register/
Disallow: /forgot-password/
Disallow: /wp-admin/
Disallow: /wp-login.php

Sitemap: https://[yourdomain.com]/sitemap.xml
```

Configure via: Rank Math SEO > General > Edit robots.txt

### Page-Level noindex

Set via Rank Math (per-page meta settings) or in code:

```php
// For portal pages, add in theme or plugin:
add_action('wp_head', function() {
  if (is_page(['employee-portal', 'admin-portal', 'login', 'register'])) {
    echo '<meta name="robots" content="noindex, nofollow">' . "\n";
  }
});
```

---

## SPAM & Form Security

### Form Protection

```
All contact forms:
✅ Honeypot field (invisible to humans, catches bots)
✅ CAPTCHA (Fluent Forms has reCAPTCHA v3 built-in)
✅ Rate limiting (max submissions per IP per hour)
✅ Email validation (require valid email format)
✅ Privacy consent checkbox (required before submission)
✅ Confirmation email to submitter
```

### Spam Registration Protection

```
Registration page:
✅ Email verification required
✅ Admin approval required (prevents auto-approval of spam accounts)
✅ reCAPTCHA on registration form (ProfilePress supports this)
```

---

## Backup Security

### UpdraftPlus Configuration

```
Backup schedule:
- Files: Weekly
- Database: Daily

Retention:
- Keep last 30 daily backups
- Keep last 12 weekly backups

Remote storage: Google Drive (free 15GB) or Dropbox
Encryption: Enable backup file encryption (set a strong passphrase)
Test restore: Perform monthly restore test on staging environment

IMPORTANT: Test your backups. A backup you've never restored is just a hope.
```

### Backup Storage Rule

```
Never store backups only on the same server as the live site.
Always use remote storage (Google Drive, Dropbox, S3, etc.)
```

---

## Security Monitoring

### Wordfence Alerts

Configure email alerts for:
- High-priority security events (immediate)
- Successful admin logins from new IP (immediate)
- Failed login threshold exceeded (immediate)
- Malware detected (immediate)
- Weekly scan summary (weekly)

### Uptime Monitoring

Use a free service to monitor site uptime:
- UptimeRobot (free for 50 monitors)
- Freshping (free tier)

Alert: Email + SMS when site goes down

---

## Incident Response Plan

If a security incident is detected:

```
Step 1: Take site offline (put in maintenance mode)
Step 2: Change all passwords immediately (WP admin, hosting, FTP, database)
Step 3: Run Wordfence malware scan
Step 4: Restore from last clean backup (if malware confirmed)
Step 5: Update all plugins, themes, WordPress core
Step 6: Harden any identified vulnerability
Step 7: Notify hosting provider
Step 8: If client data potentially exposed, consult attorney
Step 9: Document the incident
Step 10: Bring site back online after verification
```

---

## Pre-Launch Security Checklist

```
□ SSL certificate active and A+ rating
□ WordPress installed in subdirectory or with security prefix
□ All default WordPress usernames changed (no "admin" username)
□ wp-admin URL obscured (WPS Hide Login)
□ File permissions verified (755/644/640)
□ wp-config.php hardened
□ .htaccess hardened
□ XML-RPC disabled
□ WordPress version hidden from source
□ Wordfence installed, firewall active, first scan clean
□ Login rate limiting active
□ 2FA enabled for Administrator accounts
□ Portal pages verified: redirect to login (not 403/404)
□ Portal pages confirmed noindex in robots.txt
□ Form honeypot and CAPTCHA active
□ Backup running and tested
□ SSL auto-renew configured
□ Hosting account 2FA enabled
□ Admin email is monitored inbox (not a generic address)
```

---

*Review this security plan quarterly and after any major plugin updates or incidents.*
