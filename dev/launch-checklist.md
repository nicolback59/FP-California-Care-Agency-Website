# Launch Checklist
## California Care Agency Website

**Version:** 1.0
**Date:** 2026-06-13
**Target Launch:** CONTENT NEEDED

> Complete all Priority 1 items before launch. Priority 2 items should be
> completed within 30 days post-launch.

---

## PRE-LAUNCH: Content & Copy

### Priority 1 — Must Complete Before Launch

```
□ Agency legal name confirmed and used consistently
□ All CONTENT NEEDED items in /content/business-info-needed.md resolved
□ Home page: all sections have real copy (no placeholder text)
□ About page: agency story, mission, values finalized
□ All 6 service pages: complete with real descriptions
□ Contact page: real phone, email, address, hours
□ Careers page: real pay rates, benefits, open positions
□ Privacy Policy: attorney-drafted or approved
□ Terms of Use: attorney-drafted or approved
□ Accessibility Statement: published
□ All team member bios: approved by each team member
□ All team member photos: professional, approved, alt text added
□ All testimonials: written consent on file
□ All form submission emails tested and delivered
□ Regional center information: DDS vendor number confirmed
□ Legal disclaimer on all non-HIPAA pages confirmed with attorney
```

### Priority 2 — Complete Within 30 Days

```
□ First 3 blog posts published
□ FAQ fully populated
□ Resources/downloads section populated
□ Google Business Profile linked and photos added
□ Social media links added to footer
```

---

## PRE-LAUNCH: WordPress & Elementor

### WordPress Core

```
□ WordPress version: current stable (check wordpress.org)
□ PHP version: 8.0 or higher
□ Site URL configured correctly (https://yourdomain.com)
□ WordPress Address = Site Address (both HTTPS)
□ Permalink structure: /%postname%/
□ Sample page and sample post deleted
□ Hello Dolly plugin deleted
□ Default "Admin" username changed
□ Admin email: monitored real inbox
□ Tagline updated from "Just another WordPress site"
□ Search engine visibility: UNCHECKED (allows indexing)
□ Discussion/comments: disabled on all pages
□ Timezone set correctly (Pacific Time for California)
□ Date format: MM/DD/YYYY
```

### Elementor

```
□ Elementor version: current
□ Elementor Pro: activated with valid license
□ Global colors: all set to brand colors
□ Global fonts: set to brand fonts
□ Typography: H1–H6 sizes configured
□ Site logo: uploaded to Elementor kit
□ Favicon: uploaded and displaying
□ Header template: built, assigned, tested on all pages
□ Footer template: built, assigned, tested on all pages
□ All pages: published (not draft)
□ No pages showing "Add Media" placeholder in live view
□ All Elementor forms: named, working, email delivery confirmed
```

### Plugins

```
□ All plugins: current versions installed
□ No deactivated plugins left in system (delete unused)
□ Elementor Pro: licensed and active
□ ACF Pro: licensed and active
□ Rank Math: installed and activated
□ Wordfence: installed, firewall enabled, first scan clean
□ WPS Hide Login: custom URL saved in password manager
□ Limit Login Attempts: configured (3 attempts max)
□ WP Mail SMTP: configured, test email delivered
□ ProfilePress: configured, all roles created
□ Members: content restriction rules set for portal pages
□ WP Document Revisions: categories created, test upload complete
□ Fluent Forms: all forms built and tested
□ UpdraftPlus: backup schedule set, first backup complete
□ Imagify or ShortPixel: activated, all images compressed
□ Caching plugin: activated and tested
□ CookieYes: cookie banner live and functional
□ WP Accessibility Helper: activated
```

---

## PRE-LAUNCH: Security

```
□ SSL certificate: active, auto-renew enabled
□ HTTPS enforced: all HTTP → HTTPS redirects (301)
□ SSL grade: A or A+ (test at ssllabs.com)
□ wp-config.php: hardened per security-plan.md
□ .htaccess: hardened per security-plan.md
□ wp-admin URL: obscured with WPS Hide Login
□ File permissions: 755/644 on all directories/files
□ XML-RPC: disabled
□ WordPress version hidden from source HTML
□ Login rate limiting: 3 attempts max
□ 2FA: enabled for all Administrator accounts
□ Wordfence WAF: Extended Protection mode active
□ robots.txt: portal/login pages excluded from indexing
□ Portal pages: noindex meta tag confirmed
□ Portal pages: redirect to /login/ (not 403) when not logged in
□ All portal document files: protected from direct URL access
□ Backup: configured, tested with successful restore
□ Hosting account: 2FA enabled
□ Hosting account: strong password in password manager
```

---

## PRE-LAUNCH: SEO

```
□ Rank Math: configured with site name, logo, social profiles
□ XML sitemap: generated and accessible at /sitemap.xml
□ Sitemap: submitted to Google Search Console
□ Google Search Console: verified and active
□ GA4: installed and tracking page views
□ All pages: unique title tag (60 characters or less)
□ All pages: meta description (150–160 characters)
□ Home page: LocalBusiness schema configured in Rank Math
□ Service pages: schema configured
□ FAQ pages: FAQPage schema configured
□ Careers pages: JobPosting schema (per position)
□ No pages accidentally set to noindex
□ No orphaned pages (all pages linked from nav or internal links)
□ All URLs: lowercase, hyphenated, no spaces or special characters
□ Google Business Profile: claimed, verified, linked to website
□ Bing Webmaster Tools: submitted (secondary but recommended)
```

---

## PRE-LAUNCH: Performance

```
□ Google PageSpeed Insights: mobile score 70+ (target 80+)
□ Google PageSpeed Insights: desktop score 85+
□ Page load time: under 3 seconds on mobile
□ All images: WebP format or compressed JPEG
□ Hero images: under 500KB
□ All other images: under 200KB
□ Caching: enabled and verified (test with browser incognito mode)
□ CSS/JS: minified (test for Elementor conflicts before enabling)
□ Lazy loading: enabled for images below the fold
□ Google Fonts: loaded via Elementor (not separate plugin)
□ No render-blocking resources (check PageSpeed recommendations)
□ CDN: consider Cloudflare free plan for additional speed
```

---

## PRE-LAUNCH: ADA / Accessibility

```
□ WAVE tool: no errors on any public page (webaim.org/wave)
□ Color contrast: all text passes WCAG AA (4.5:1 minimum)
□ All images: descriptive alt text
□ All icons: aria-label or aria-hidden (if decorative)
□ All forms: labels associated with inputs
□ All form errors: announced to screen readers
□ Tab navigation: logical order on all pages
□ Skip to content link: present as first focusable element
□ Focus visible: keyboard focus indicator visible on all elements
□ No content relies solely on color to convey meaning
□ All videos: captions provided (if any video content)
□ Phone numbers: click-to-call links (tel: protocol)
□ Accessibility Statement: published at /accessibility/
□ Language attribute: html lang="en" present
```

---

## PRE-LAUNCH: Forms & Communication

```
□ WP Mail SMTP: configured with agency email (Google Workspace or similar)
□ All forms: test submission sent and email received
□ Contact form: reply-to set to submitter's email
□ Referral form: notification goes to correct staff member
□ Application form: notification goes to HR/hiring manager
□ All form success messages: confirm submission and next steps
□ All form error messages: clear, helpful, not technical
□ Privacy consent checkbox: present on all data-collecting forms
□ Form data: stored in WordPress (Fluent Forms entries) as backup
□ Spam protection: honeypot + CAPTCHA on all public forms
```

---

## PRE-LAUNCH: Employee Portal

```
□ /login/ page: styled and functional
□ /register/ page: styled and functional
□ /forgot-password/ page: functional
□ ProfilePress: registration approval workflow tested
  - Create account → Admin receives notification
  - Admin approves → Employee receives welcome email
  - Employee logs in → Redirected to /employee-portal/
□ Employee role: can access /employee-portal/
□ Employee role: cannot access /admin-portal/
□ Employee role: cannot access WP Admin
□ Portal navigation: functional for all portal sections
□ Onboarding page: content populated (see portal requirements doc)
□ Handbook page: document uploaded and downloadable
□ Forms section: at least 3 critical forms uploaded
□ Announcements: at least 1 welcome announcement posted
□ Logout: functional, redirects to /login/
□ Test with: 1 administrator account + 1 test employee account
```

---

## PRE-LAUNCH: Cross-Browser & Device Testing

### Browsers to Test

```
□ Chrome (latest — Mac/Windows)
□ Safari (latest — Mac)
□ Firefox (latest — Mac/Windows)
□ Microsoft Edge (latest — Windows)
□ Safari — iPhone (latest iOS)
□ Chrome — Android (latest)
```

### Devices / Screen Sizes to Test

```
□ Desktop: 1920px wide
□ Desktop: 1440px wide
□ Laptop: 1280px wide
□ Tablet: 768px wide (iPad portrait)
□ Mobile: 390px wide (iPhone 14)
□ Mobile: 375px wide (older iPhone)
□ Mobile: 360px wide (common Android)
```

### Pages to Test on All Devices

```
□ Home
□ About
□ Services overview
□ One service page (SLS or ILS)
□ Contact
□ Careers
□ Employee Portal login flow
□ Employee Portal dashboard
□ Forms (contact, referral, application)
```

---

## LAUNCH DAY

```
□ Final backup: taken immediately before going live
□ Maintenance mode: disabled
□ DNS: pointed to correct server IP
□ SSL: active on new DNS
□ Redirect: any old domain to new domain (if applicable)
□ Forms: final test after DNS resolves
□ GA4: verify tracking after launch
□ Rank Math sitemap: re-submit to Google Search Console
□ Announcement: notify staff (employees, leadership) that site is live
□ Google Business Profile: update website URL if changed
□ Social profiles: update website link if changed
□ Team notified: who to contact if something breaks
```

---

## POST-LAUNCH (30 Days)

```
□ Day 1: Monitor GA4 for traffic and errors
□ Day 3: Check Google Search Console for any index errors
□ Day 7: Confirm all forms still delivering emails
□ Day 7: Review Wordfence security alerts
□ Day 14: Check page speed (sites can slow after heavy use)
□ Day 30: Review GA4 data — which pages get the most traffic
□ Day 30: Review form submissions — any issues?
□ Day 30: Run WAVE accessibility check again
□ Day 30: Submit sitemap update if new pages added
□ Day 30: Check for broken links (use Broken Link Checker)
□ Day 30: Confirm backup completed successfully (check UpdraftPlus)
□ Day 30: Employee portal: verify at least 2 real employee accounts working
□ Day 30: Staff training: brief non-technical staff on how to update content
```

---

## Staff Training Checklist (Non-Technical)

Before launch, train agency staff on:

```
□ How to log into WordPress admin
□ How to update the Careers page with new job listings
□ How to add a team member
□ How to add an announcement to the Employee Portal
□ How to upload a document to the Employee Portal
□ How to view form submissions (contact, referral, applications)
□ How to approve a new employee registration
□ Who to contact if something breaks (developer contact on file)
□ How to export a backup (basic)
□ What NOT to change without developer help (Elementor templates, plugins)
```

---

*This checklist is the final gate before and after launch. Nothing ships without Priority 1 items complete.*
