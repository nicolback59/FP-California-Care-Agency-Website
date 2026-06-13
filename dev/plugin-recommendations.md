# Plugin Recommendations
## California Care Agency — WordPress Plugin Stack

**Date:** 2026-06-13
**Platform:** WordPress + Elementor Pro

---

## Summary: Recommended Plugin Stack

| Category | Plugin | License | Cost/Year | Why Chosen |
|----------|--------|---------|-----------|------------|
| Page Builder | Elementor Pro | Paid | ~$99 | Best visual builder; required for Theme Builder |
| Custom Fields | ACF Pro | Paid | ~$49 | Essential for dynamic content (team, jobs, testimonials) |
| SEO | Rank Math | Free | $0 | Superior free tier; better schema tools than Yoast free |
| Forms | Fluent Forms | Free/Pro | $0–$79 | Best value; Elementor compatible; conditional logic |
| SMTP | WP Mail SMTP | Free | $0 | Ensures form emails deliver reliably |
| Security | Wordfence | Free | $0 | Industry standard; WAF + malware scanning |
| Login Protection | WPS Hide Login | Free | $0 | Obscures /wp-admin — reduces bot attacks |
| Rate Limiting | Limit Login Attempts Reloaded | Free | $0 | Blocks brute force attacks |
| User Portal | ProfilePress | Free/Pro | $0–$99 | Best balance of features/cost for employee portal |
| Role Access | Members | Free | $0 | Simple, reliable role-based content restriction |
| Documents | WP Document Revisions | Free | $0 | File management within WordPress |
| Backups | UpdraftPlus | Free | $0 | Reliable scheduled backups to cloud storage |
| Caching | SiteGround Optimizer | Free | $0 | Host-integrated; or WP Rocket ($59/yr) off SiteGround |
| Images | Imagify | Free tier | $0 | WebP conversion; 25MB/mo free tier |
| Accessibility | WP Accessibility Helper | Free | $0 | Skip links, focus management, accessibility fixes |
| Cookies | CookieYes | Free tier | $0 | GDPR/CCPA consent banner |
| Multilingual | None at launch | — | — | Add Polylang for Spanish in Phase 2 |

**Estimated Annual Plugin Cost:** ~$247–$327 (Elementor Pro + ACF Pro + ProfilePress Pro)
**Without Pro upgrades:** $0 (Elementor free is limited; most other plugins have viable free tiers)

---

## Detailed Recommendations

---

### 1. PORTAL / MEMBERSHIP PLUGIN

**Recommendation: ProfilePress (Free + Pro as needed)**

**Rationale:**

| Plugin | Pros | Cons | Best For |
|--------|------|------|----------|
| **ProfilePress** ✅ | Clean UI, Elementor-compatible login forms, approval workflow, custom user fields, free tier is generous | Pro needed for some advanced features | Employee portals, self-registration with approval |
| MemberPress | Most powerful; subscription/payment handling | $179/yr; overkill for no-payment use case | Paid membership sites |
| Ultimate Member | Good free tier; community-focused | UI a bit dated; heavier than ProfilePress | Forums, communities |
| Paid Memberships Pro | Strong for recurring payments | Payment-centric; more complex to set up | Paid subscription portals |
| WP User Manager | Clean and simple | Less actively developed | Small, simple portals |

**ProfilePress Setup for This Project:**

```
Free tier handles:
✅ Custom login page (Elementor-styled)
✅ Custom registration page
✅ Password reset page
✅ Email verification
✅ User approval workflow (Admin must approve new registrations)
✅ Custom user profile fields
✅ Role assignment

Pro tier adds ($0–$99/yr):
→ Advanced user directory
→ Additional form fields
→ More profile layouts
→ Content drip (onboarding sequences)
```

**Implementation:**
```
WordPress Users:
Role: Employee         → Access: /employee-portal/ pages
Role: Manager          → Access: /employee-portal/ + management features
Role: Administrator    → Full WP admin + /admin-portal/
```

**Combine with: Members plugin** for content restriction rules.

---

### 2. ROLE-BASED ACCESS

**Recommendation: Members (free by Justin Tadlock)**

Reasons:
- Simple, reliable, well-maintained
- Works cleanly with ProfilePress user roles
- Allows content restriction per page/post by role
- Shortcode support for mixed-content pages
- No conflicts with Elementor or ACF

**Alternative:** User Role Editor (also free, more technical)

---

### 3. SEO PLUGIN

**Recommendation: Rank Math (Free)**

| Plugin | Free Tier | Paid Tier | Recommendation |
|--------|-----------|-----------|----------------|
| **Rank Math** ✅ | Excellent — schema, sitemap, local SEO, 404 monitor, redirects | $79/yr for advanced | Best free SEO plugin available today |
| Yoast SEO | Good — basic schema, sitemap, readability | $99/yr for full features | Industry standard but Rank Math free tier wins |

**Rank Math Free Configuration:**
```
✅ XML Sitemap (exclude portal/login pages)
✅ Title + description templates for each post type
✅ Schema: LocalBusiness, Organization, FAQPage
✅ Google Search Console integration
✅ Robots.txt editor (noindex portal pages)
✅ Redirects manager
✅ 404 error monitor
✅ Open Graph (Facebook/LinkedIn share previews)
```

---

### 4. FORMS PLUGIN

**Recommendation: Fluent Forms (Free Tier + Pro if needed)**

| Plugin | Strengths | Weaknesses | Cost |
|--------|-----------|------------|------|
| **Fluent Forms** ✅ | Fast, conditional logic in free tier, Elementor widget, SMTP-compatible, PDF entries, GDPR tools | Support on free tier is limited | Free / $79/yr Pro |
| Gravity Forms | Most powerful; developer ecosystem | $59/yr entry — no meaningful free tier | $59–$259/yr |
| WPForms | Very easy to use; great for beginners | Free tier very limited; forms are basic | Free / $49–$200/yr |

**Forms Needed for This Site:**
```
1. General Contact Form (all audiences)
2. Service Inquiry Form (families)
3. Referral Form (service coordinators)
4. Employment Application Form
5. Testimonial Submission Form
6. Employee Registration (via ProfilePress — not Fluent Forms)
```

---

### 5. SECURITY

**Recommendation: Wordfence Security (Free)**

```
Free tier includes:
✅ Web Application Firewall (WAF)
✅ Malware scanner
✅ Login security (rate limiting, CAPTCHA)
✅ Blocked IPs
✅ Security alerts via email
✅ File integrity monitoring

Configure:
- Firewall: Extended Protection mode
- Email alerts: Security-level events
- Scheduled scan: Weekly minimum
- Login security: Limit to 3 attempts
- CAPTCHA on login and registration
```

**Additional Security:**
- WPS Hide Login — changes `/wp-admin/` to a custom URL
- Disable XML-RPC (via Wordfence or via Rank Math)
- Force HTTPS (via .htaccess or hosting panel)
- Strong passwords enforced via ProfilePress

---

### 6. BACKUP

**Recommendation: UpdraftPlus (Free)**

```
Configuration:
- Schedule: Daily automatic backups
- Storage: Google Drive or Dropbox (free)
- Retention: Keep last 30 days
- Scope: Database + Files + Plugins + Themes + Uploads
- Test restore: Verify monthly

Alternative: SiteGround Backup (if on SiteGround — included in plan)
Note: Always use 2 backup sources
```

---

### 7. CACHING

**If on SiteGround:** Use SiteGround Optimizer (free, included)
```
Enable:
✅ Dynamic cache
✅ Memcached (if available on plan)
✅ Image WebP conversion
✅ CSS/JS minification (test for Elementor conflicts)
✅ Lazy loading
```

**If not on SiteGround:** WP Rocket ($59/yr) — best overall caching plugin

**Free Alternative:** W3 Total Cache or LiteSpeed Cache (if LiteSpeed server)

---

### 8. IMAGE OPTIMIZATION

**Recommendation: Imagify (free tier)**
```
Free tier: 25MB/month (reset monthly)
- Auto-convert uploads to WebP
- Bulk optimize existing images
- Preserves originals for rollback

Alternative: ShortPixel (100 images/month free)
Alternative: Smush (1MB limit on free tier — less ideal)
```

---

## Plugins to Avoid

| Plugin | Why to Avoid |
|--------|-------------|
| WooCommerce | Unnecessary overhead; no e-commerce needed |
| Jetpack | Heavy plugin with features duplicated by others |
| Contact Form 7 | Outdated; Fluent Forms is superior |
| Hello Dolly | Decorative; delete from install |
| BuddyPress/BuddyBoss | Overkill for employee portal |
| Elementor + another page builder | Never run two page builders simultaneously |
| Multiple SEO plugins | Only one at a time |
| Multiple security plugins | Wordfence only; conflicts with others |
| Classic Editor | Stick with Gutenberg + Elementor |

---

## Plugin Conflict Notes

- Always test after adding new plugins
- Elementor and caching plugins: clear cache after Elementor saves
- ProfilePress and Members: complementary, no conflicts
- Rank Math and Wordfence: no conflicts
- Fluent Forms and WP Mail SMTP: works well together; test SMTP settings

---

## Plugin Update Policy

- Update plugins on staging environment first
- Never update plugins on live site without backup first
- Elementor Pro updates may require theme/template review
- ACF updates: test with all custom post types after update

---

*Review this stack 6 months post-launch and after any major WordPress updates.*
