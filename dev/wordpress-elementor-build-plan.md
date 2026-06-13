# WordPress + Elementor Build Plan
## California Care Agency Website

**Version:** 1.0
**Date:** 2026-06-13
**Platform:** WordPress + Elementor Pro + ACF Pro
**Hosting:** SiteGround (recommended) or equivalent managed WordPress host

---

## Project Roadmap

### Phase 1 — Foundation (Week 1–2)

| Task | Owner | Status |
|------|-------|--------|
| Purchase and set up hosting | Agency | Not Started |
| Purchase domain name | Agency | Not Started |
| Install WordPress | Developer | Not Started |
| Install recommended plugins | Developer | Not Started |
| Configure WordPress settings | Developer | Not Started |
| Configure Elementor global styles | Developer | Not Started |
| Build header template | Developer | Not Started |
| Build footer template | Developer | Not Started |
| Set up user roles and access | Developer | Not Started |
| Collect agency brand assets | Agency | Not Started |

### Phase 2 — Core Pages (Week 3–5)

| Task | Owner | Status |
|------|-------|--------|
| Home page — full build | Developer | Not Started |
| About page | Developer | Not Started |
| Services overview | Developer | Not Started |
| Individual service pages (x6) | Developer | Not Started |
| Contact page | Developer | Not Started |
| Careers page | Developer | Not Started |
| For Families section | Developer | Not Started |
| Referral Sources page | Developer | Not Started |
| Testimonials page | Developer | Not Started |
| FAQ page | Developer | Not Started |

### Phase 3 — Portals & Authentication (Week 5–7)

| Task | Owner | Status |
|------|-------|--------|
| Employee portal build | Developer | Not Started |
| Admin portal build | Developer | Not Started |
| Login / Registration pages | Developer | Not Started |
| User role gating | Developer | Not Started |
| Approval workflow | Developer | Not Started |
| Portal navigation | Developer | Not Started |
| Document management setup | Developer | Not Started |

### Phase 4 — Content & Legal (Week 7–8)

| Task | Owner | Status |
|------|-------|--------|
| Agency content populated | Agency/Developer | Not Started |
| Privacy Policy page | Attorney + Developer | Not Started |
| Terms of Use page | Attorney + Developer | Not Started |
| Accessibility Statement | Developer | Not Started |
| All forms tested | Developer | Not Started |
| Email delivery confirmed | Developer | Not Started |

### Phase 5 — SEO & Performance (Week 8–9)

| Task | Owner | Status |
|------|-------|--------|
| Rank Math configured | Developer | Not Started |
| All pages: meta title + description | Developer | Not Started |
| XML sitemap submitted | Developer | Not Started |
| Google Search Console linked | Developer | Not Started |
| GA4 installed | Developer | Not Started |
| Page speed optimized | Developer | Not Started |
| Image optimization | Developer | Not Started |

### Phase 6 — QA & Launch (Week 9–10)

| Task | Owner | Status |
|------|-------|--------|
| Cross-browser testing | Developer | Not Started |
| Mobile responsiveness testing | Developer | Not Started |
| Accessibility audit (WAVE) | Developer | Not Started |
| Forms end-to-end testing | Developer | Not Started |
| Portal testing (all roles) | Developer | Not Started |
| Backups confirmed | Developer | Not Started |
| DNS/domain pointed to hosting | Agency | Not Started |
| SSL certificate active | Developer | Not Started |
| Site goes live | Developer | Not Started |

---

## WordPress Initial Configuration

### Permalink Structure
```
Settings > Permalinks > Post name: /%postname%/
```

### Reading Settings
```
Settings > Reading:
- Your homepage displays: A static page
- Homepage: [Home page created in Elementor]
- Posts page: [Blog page]
```

### Discussion Settings
```
Settings > Discussion:
- Disable comments on all new pages by default
  (unless blog comments are explicitly desired)
```

### Media Settings
```
Settings > Media:
- Thumbnail size: 150×150 (crop)
- Medium size: 300×300
- Large size: 1024×1024
```

### User Settings
```
Settings > General:
- Anyone can register: UNCHECKED (registration controlled by plugin)
- New user default role: Subscriber (overridden by portal plugin)
```

---

## Elementor Configuration

### Kit Settings (Site Identity)

1. Open Elementor Kit Settings:
   `Elementor > Site Settings > Site Identity`
   - Site name: [Agency Name]
   - Site logo: Upload agency logo
   - Favicon: Upload favicon

### Global Colors

In Elementor > Site Settings > Global Colors, add:

```
Color Name        Hex Value
─────────────────────────────
Primary           CONTENT NEEDED (brand primary)
Secondary         CONTENT NEEDED (brand secondary)
Accent            CONTENT NEEDED (brand accent)
Text              #1E293B (dark slate)
Text Light        #64748B (medium gray)
Background        #F8FAFC (off-white)
White             #FFFFFF
Success           #22C55E
Warning           #F59E0B
Error             #EF4444
```

### Global Fonts

In Elementor > Site Settings > Global Fonts:

```
Font Role    Family              Weight   Notes
──────────────────────────────────────────────────
Primary      CONTENT NEEDED      700     (headings)
Secondary    CONTENT NEEDED      400     (body)
Text         CONTENT NEEDED      400     (standard text)
Accent       CONTENT NEEDED      600     (buttons, labels)
```

Placeholder until brand fonts confirmed:
- Headings: Inter Bold
- Body: Inter Regular
- Source: Google Fonts (free)

### Typography System

In Elementor > Site Settings > Typography:

```
Element         Size    Weight  Line Height  Letter Spacing
──────────────────────────────────────────────────────────
H1              56px    700     1.2          -0.5px
H2              40px    700     1.25         -0.25px
H3              32px    600     1.3          0
H4              24px    600     1.35         0
H5              20px    600     1.4          0
Body Text       16px    400     1.65         0
```

### Theme Builder Templates

Build the following Elementor Theme Builder templates:

1. **Header — Default** (applies to all public pages)
   - Logo (links to home)
   - Primary navigation with mega menu for Services
   - Phone number (click-to-call)
   - "Get Started" CTA button
   - Sticky on scroll

2. **Header — Portal** (applies to /employee-portal/ and /admin-portal/)
   - Logo only (no main nav)
   - Logged-in user name
   - Logout link

3. **Footer — Default** (applies to all public pages)
   - 5-column navigation
   - Agency info + contact
   - Social links
   - Legal links row
   - Copyright

4. **Footer — Minimal** (applies to login/register pages)
   - Logo only
   - Privacy Policy link

5. **Single — Service** (applies to all service CPT or service pages)
   - Breadcrumb
   - Standard service page sections
   - Sidebar CTA

6. **Single — Job Listing** (applies to Job Listing CPT)
   - Job details
   - Apply form

---

## Custom Post Types (ACF Pro)

### Team Members CPT

```
Post Type: team_member
URL:       /team/[name]/
Fields:
  - Member name (auto from post title)
  - Position/title (text)
  - Biography (WYSIWYG)
  - Photo (image)
  - Email (email) — optional, admin controls visibility
  - LinkedIn URL — optional
  - Display order (number)
  - Active (true/false) — to hide without deleting
```

### Job Listings CPT

```
Post Type: job_listing
URL:       /careers/[position-name]/
Fields:
  - Position title (auto from post title)
  - Department (select: DSP, Admin, Clinical, Management)
  - Location (text)
  - Type (select: Full-Time, Part-Time, Per-Diem)
  - Pay range (text: e.g., "$18–$22/hr")
  - Schedule (text)
  - Description (WYSIWYG)
  - Requirements (WYSIWYG)
  - Benefits (WYSIWYG)
  - Application deadline (date picker)
  - Apply URL or use site form (radio)
  - External apply URL (URL field — conditional)
  - Active (true/false)
```

### Testimonials CPT

```
Post Type: testimonial
Fields:
  - Quote text (WYSIWYG)
  - Attribution name (text — first name or initials only per policy)
  - Attribution role (text: Parent, Family Member, Service Coordinator, etc.)
  - Photo (image — with release confirmation checkbox)
  - Consent on file (true/false — admin only)
  - Category (taxonomy: Client/Family/Professional)
  - Featured (true/false — shows on homepage)
```

### Resources/Documents CPT (Employee Portal)

```
Post Type: employee_document
Fields:
  - Document title (auto from post title)
  - Category (taxonomy: Onboarding, Handbook, Forms, HR, Policies, Training)
  - File upload (file field)
  - Description (textarea)
  - Version (text)
  - Effective date (date)
  - Visible to (select: All Employees, Managers, Admin Only)
  - Active (true/false)
```

### Announcements CPT (Employee Portal)

```
Post Type: announcement
Fields:
  - Title (auto)
  - Content (WYSIWYG)
  - Priority (select: Normal, Important, Urgent)
  - Target audience (select: All, DSPs, Management, Admin)
  - Pinned (true/false)
  - Expiry date (date — hides announcement after this date)
```

---

## Elementor Page Structure — Home Page

All sections are built as Elementor sections within the Home page template.

```
Section ID          Type              Background       Padding
───────────────────────────────────────────────────────────────
#hero               Full-width        Image+overlay    90vh
#trust-bar          Full-width        Brand primary    60px
#mission            Boxed             White            96px
#services           Full-width        Off-white        96px
#why-us             Full-width        Brand dark       80px
#regional-center    Boxed             White            80px
#testimonials       Full-width        Off-white        80px
#careers-cta        Full-width        Image+overlay    96px
#contact-cta        Boxed             White            80px
```

---

## Hosting Requirements

| Spec | Minimum | Recommended |
|------|---------|-------------|
| PHP | 8.0 | 8.2 |
| MySQL | 5.7 | 8.0 |
| Storage | 10GB | 20GB+ |
| Memory limit | 256MB | 512MB |
| HTTPS/SSL | Required | Required |
| Automatic backups | Required | Required |

**Recommended Hosts:**
- SiteGround (GrowBig or higher) — Excellent WordPress support, staging, backups
- WP Engine (Startup) — Managed WordPress, dev/staging environments
- Kinsta (Starter) — Premium managed WordPress, excellent performance
- Cloudways (DigitalOcean 2GB) — More technical, great value

---

## Plugin Installation Order

Install in this order to avoid conflicts:

1. Hello Elementor (theme)
2. Elementor (free — required before Pro)
3. Elementor Pro (activate license)
4. Advanced Custom Fields Pro
5. Rank Math SEO
6. Wordfence Security
7. WP Mail SMTP
8. ProfilePress (user registration/login)
9. Members (role-based access)
10. WP Document Revisions
11. Fluent Forms
12. WPS Hide Login
13. Limit Login Attempts Reloaded
14. WP Accessibility Helper
15. CookieYes
16. Imagify (or ShortPixel)
17. SiteGround Optimizer (if on SiteGround) or WP Rocket

---

*Update this document as the build progresses. Mark tasks complete with ✅.*
