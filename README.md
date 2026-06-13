# California Care Agency Website
## Project Repository

**Project Type:** WordPress + Elementor Pro Website
**Client:** California For-Profit Care Agency (DDS Vendored)
**Status:** Pre-Build Planning Phase
**Last Updated:** 2026-06-13

---

## Project Overview

This repository contains all planning, design, and development documentation
for the California Care Agency website build. The site will be:

- WordPress-based with Elementor Pro
- Mobile-responsive and ADA-conscious
- SEO-optimized for local California markets
- Secure with role-based access control
- Inclusive of a private Employee Portal and Admin Portal

---

## Repository Structure

```
/
├── README.md                              ← This file
│
├── content/
│   ├── trinity-change-audit.md           ← Reference site audit (manual review needed)
│   ├── business-info-needed.md           ← Missing information checklist (106 items)
│   ├── site-map.md                       ← Full website sitemap + navigation
│   └── page-copy-drafts.md               ← Page copy framework + placeholders
│
├── design/
│   ├── brand-notes.md                    ← Logo, colors, fonts, imagery guide
│   ├── reference-sites.md                ← Design inspiration + reference sites
│   └── wireframes.md                     ← Section-by-section page wireframes
│
├── dev/
│   ├── wordpress-elementor-build-plan.md ← Full build roadmap + Elementor config
│   ├── plugin-recommendations.md         ← Plugin stack with rationale
│   ├── admin-employee-portal-requirements.md ← Portal architecture + flows
│   ├── security-plan.md                  ← Security hardening plan
│   ├── seo-strategy.md                   ← SEO plan, schema, keywords
│   └── launch-checklist.md               ← Pre/post-launch verification checklist
│
├── legal/
│   ├── privacy-policy-notes.md           ← Privacy Policy planning notes (NOT final)
│   └── terms-accessibility-notes.md      ← Terms of Use + Accessibility planning
│
├── assets/
│   └── README.md                         ← Asset directory guide + status
│
└── website-strategy/                     ← Pre-existing strategy documents
    ├── 04-service-pages.md               ← Service page content templates
    └── 08-features-priority-ranking.md   ← Feature priority list + plugin stack
```

---

## Quick Status: What's Needed Before Development

> **106 items flagged as CONTENT NEEDED in `/content/business-info-needed.md`**

### Priority 1 — Launch Blockers

| Item | Status |
|------|--------|
| Agency legal name | CONTENT NEEDED |
| DDS Vendor Number | CONTENT NEEDED |
| Business phone + email + address | CONTENT NEEDED |
| Mission + Vision + Values | CONTENT NEEDED |
| Agency logo (SVG) | CONTENT NEEDED |
| Brand colors (hex codes) | CONTENT NEEDED |
| Leadership team bios + photos | CONTENT NEEDED |
| Privacy Policy (attorney-drafted) | CONTENT NEEDED |
| DSP pay rates + benefits | CONTENT NEEDED |
| Regional center partnerships | CONTENT NEEDED |
| Service counties | CONTENT NEEDED |
| Domain name + hosting | CONTENT NEEDED |

---

## Website at a Glance

### Public Pages (38 total)

| Section | Pages |
|---------|-------|
| Core | Home, About, Contact, FAQ |
| Services | Overview + 6 individual service pages |
| For Families | How It Works, Getting Started, FAQ |
| Referral Sources | Landing page + Referral form |
| Careers | Why Work With Us, Open Positions, Apply |
| Other | Testimonials, Resources, Blog |
| Legal | Privacy Policy, Terms of Use, Accessibility |

### Private Pages

| Section | URL | Access |
|---------|-----|--------|
| Employee Portal | `/employee-portal/` | Employees + Managers + Admin |
| Admin Portal | `/admin-portal/` | Admin + Managers |
| Login | `/login/` | Public (not indexed) |
| Register | `/register/` | Public (not indexed) |

---

## Technology Stack

| Category | Choice | Notes |
|----------|--------|-------|
| CMS | WordPress | Latest stable |
| Page Builder | Elementor Pro | Theme Builder required |
| Custom Fields | ACF Pro | Team, Jobs, Testimonials CPTs |
| Theme | Hello Elementor | Official Elementor theme |
| SEO | Rank Math (free) | Schema, sitemap, redirects |
| Forms | Fluent Forms | Contact, referral, application |
| User Portal | ProfilePress | Registration, login, approval |
| Access Control | Members plugin | Role-based page restriction |
| Security | Wordfence | WAF, malware scan |
| Backups | UpdraftPlus | Daily database, weekly files |
| SMTP | WP Mail SMTP | Form email delivery |
| Images | Imagify | WebP conversion |
| Hosting | SiteGround (recommended) | Or WP Engine / Kinsta |

---

## Development Phases

| Phase | Description | Timeline |
|-------|-------------|---------|
| 1 | Foundation — WP setup, plugins, global styles, header/footer | Weeks 1–2 |
| 2 | Core Pages — Home through Careers, all public pages | Weeks 3–5 |
| 3 | Portals — Employee + Admin portal, login system | Weeks 5–7 |
| 4 | Content & Legal — Populate real content, legal pages | Weeks 7–8 |
| 5 | SEO & Performance — Rank Math, GA4, speed optimization | Weeks 8–9 |
| 6 | QA & Launch — Testing, final checks, go live | Weeks 9–10 |

---

## Key Contacts

| Role | Name | Contact |
|------|------|---------|
| Agency Owner / Decision Maker | CONTENT NEEDED | CONTENT NEEDED |
| WordPress Developer | CONTENT NEEDED | CONTENT NEEDED |
| SEO Consultant | CONTENT NEEDED | CONTENT NEEDED |
| Attorney (legal pages) | CONTENT NEEDED | CONTENT NEEDED |
| Photographer | CONTENT NEEDED | CONTENT NEEDED |

---

## Git Branch Strategy

| Branch | Purpose |
|--------|---------|
| `main` | Source of truth — only merge completed, reviewed work |
| `claude/care-agency-website-plan-wh5xj3` | Planning and documentation development |
| `feature/*` | Individual feature or page builds |

---

## Important Notes

1. **Do NOT invent** DDS numbers, licensing info, vendor numbers, insurance data, testimonials, staff credentials, or any legal/regulatory information. All such data must come from the agency.

2. **Privacy compliance** — Have an attorney review Privacy Policy and Terms of Use before launch. Do not publish AI-generated legal documents as-is.

3. **HIPAA** — Do not store Protected Health Information (PHI) in WordPress. Keep medical/clinical data in a HIPAA-compliant EHR system.

4. **Testimonials** — Require written consent from the individual or authorized representative before publishing any testimonial, including name or photo.

5. **Employee portal** — Test all role-based access controls before launch. Verify unauthorized users cannot access portal content.

---

*This repository is the single source of truth for the website project. Update documentation as decisions are made and content is received.*
