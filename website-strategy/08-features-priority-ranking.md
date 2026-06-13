# Features, Priorities & Developer Handoff Reference
## New California For-Profit Care Agency Website

---

## Features to Add (Beyond Trinity Change)

| Feature | Why It Matters | Priority |
|---------|---------------|----------|
| Persistent header with phone + CTA | #1 conversion mechanism | Must Have |
| Audience-segmented navigation | Families, SCs, job seekers need different paths | Must Have |
| Dedicated referral sources landing page | SCs want a page built for them | Must Have |
| Make-a-Referral form (SC-specific) | Structured referral data capture | Must Have |
| Compliance & Credentials page | DDS vendor #, licensing, insurance | Must Have |
| Downloadable Capability Statement PDF | Leave-behind for RC meetings | Must Have |
| Service-specific inquiry forms | Families need different form than SCs | Must Have |
| Dynamic job listings (ACF custom post type) | Admin can update without developer | Must Have |
| DSP-focused careers content | Most agencies have generic "join us" copy | Must Have |
| Google Business Profile integration | #1 trust signal for local search | Must Have |
| Regional center logos / partner list | Vendor credibility for SC audience | Must Have |
| Person-Centered Planning page | Differentiator; few agencies explain their philosophy | Must Have |
| Respite / Crisis Support page | Captures urgent families | Must Have |
| FAQ page (family-facing) | Handles objections at scale; supports SEO | Must Have |
| "How It Works" page | Reduces intake friction | Must Have |
| Team / Staff page with real photos | Trust-builder | Must Have |
| Mobile click-to-call phone numbers | Majority of family visitors are on mobile | Must Have |
| HTTPS / SSL + privacy policy | Required | Must Have |
| Accessibility statement | Expected by regional center partners | Must Have |
| **Admin dashboard** | **Developer builds — WP native admin + role customization** | **Must Have** |
| **Employee login + dashboard** | **Developer builds — ProfilePress + Members plugin** | **Must Have** |
| **Onboarding walkthrough** | **Developer builds — step-page flow** | **Must Have** |
| Blog / resource library | Long-term SEO | Nice to Have |
| DDS System Guide (resource page) | SEO magnet; trust-builder | Nice to Have |
| Live chat or callback widget | Reduces friction | Nice to Have |
| Email newsletter opt-in | CRM list building | Nice to Have |
| Video testimonials | Most powerful trust content | Nice to Have |
| Service area / county-specific pages | Local SEO | Nice to Have |
| Schema markup | Structured data for Google | Nice to Have |
| Training video library | Protected employee content | Future Phase |
| Employee forms hub | Timesheets, PTO, incident reports | Future Phase |
| Digital handbook with acknowledgment | Replaces paper handbook | Future Phase |
| Announcements feed (employees only) | Internal communications | Future Phase |

---

## Features to Avoid

| Feature | Why to Avoid |
|---------|-------------|
| Custom CRM on WordPress | Use Therap, CareSmartz360 instead |
| HIPAA data storage on website | Never — use compliant EHR |
| Online payroll or HR processing | Use Gusto, ADP instead |
| Real-time scheduling system | Use dedicated DSP scheduling platform |
| WooCommerce / e-commerce | No products to sell |
| Custom mobile app | Too expensive for launch |
| Multilingual site at launch | Adds significant scope; plan Spanish for Phase 2 |
| AI chatbot | Cost + quality risk; good forms outperform |
| Forum or community platform | Moderation overhead; no clear benefit |
| Agency-built ATS | Use Indeed/ZipRecruiter or simple form |

---

## Priority Ranking Summary

### Must Have (Launch Blockers)

- [ ] Home page (all 12 sections)
- [ ] About Us — Our Story, Our Team, Mission & Values, Credentials
- [ ] Services — SLS, ILS, Community Integration, Person-Centered, Respite
- [ ] For Families — How It Works, Getting Started, FAQ
- [ ] Referral Sources — SC landing page + Make a Referral form
- [ ] Careers — Why Work With Us, Open Positions, Benefits & Pay, Hiring Process, Apply Now
- [ ] Contact page (multi-audience form)
- [ ] **Employee Login + Dashboard (Developer builds)**
- [ ] **Admin Dashboard setup (Developer configures)**
- [ ] Privacy Policy + Terms of Use + Accessibility Statement
- [ ] Persistent header with phone + CTA
- [ ] Mobile-responsive (tested iOS + Android)
- [ ] SSL / HTTPS
- [ ] Google Business Profile (claimed + linked)
- [ ] Rank Math/Yoast installed, all pages have title + meta desc
- [ ] Page speed < 3 seconds
- [ ] Downloadable Capability Statement PDF

### Nice to Have (60–90 Days Post-Launch)

- [ ] Blog (first 3–5 posts)
- [ ] DDS System Guide resource page
- [ ] Service area pages (top 2–3 counties)
- [ ] Live chat or callback widget
- [ ] Email newsletter opt-in
- [ ] Google Reviews integration
- [ ] LinkedIn Company Page + social links
- [ ] Schema markup (LocalBusiness)

### Future Phase (3–12 Months)

- [ ] Training video library (employee portal)
- [ ] Employee forms hub
- [ ] Digital employee handbook
- [ ] Spanish-language pages (key service + intake)
- [ ] Video testimonials
- [ ] Advanced local SEO (per-county pages)
- [ ] JobPosting schema on careers pages

---

## WordPress + Elementor Developer Launch Checklist

### WordPress Setup
- [ ] WordPress on SiteGround (single site, not multisite)
- [ ] Admin user: strong password + 2FA
- [ ] Permalink structure: Post name (`/%postname%/`)
- [ ] SiteGround Optimizer installed and configured
- [ ] All plugins updated

### User Roles & Portal
- [ ] ProfilePress installed and configured
- [ ] Members plugin installed for role-based access
- [ ] `Employee` custom role created
- [ ] `Manager` custom role created (if needed)
- [ ] Employee portal pages created and role-gated
- [ ] Login page styled with Elementor / ProfilePress
- [ ] Admin email notifications for new employee registrations

### Elementor Setup
- [ ] Elementor Pro activated and licensed
- [ ] Site settings: typography, color palette, spacing
- [ ] Global templates: header, footer, CTA sections
- [ ] All pages published (not draft)

### ACF Setup
- [ ] ACF Pro activated
- [ ] Field groups: Service Pages, Job Listings, Testimonials, Team Members, Partners
- [ ] JSON sync enabled
- [ ] All fields tested with real content

### Performance
- [ ] SiteGround caching ON (dynamic caching)
- [ ] All images compressed (WebP preferred)
- [ ] PageSpeed score > 80 mobile
- [ ] Lazy loading on images

### Security
- [ ] HTTPS enforced (HTTP → HTTPS redirect)
- [ ] Login URL obscured (WPS Hide Login)
- [ ] Limit Login Attempts active
- [ ] XML-RPC disabled
- [ ] Regular backups configured

### SEO
- [ ] Rank Math installed and configured
- [ ] XML sitemap submitted to Google Search Console
- [ ] GA4 connected
- [ ] All pages: unique title tag + meta description
- [ ] No pages set to noindex accidentally
- [ ] Robots.txt blocking portal + login pages

### Forms
- [ ] All forms tested (submission → email delivery)
- [ ] WP Mail SMTP configured with SiteGround SMTP
- [ ] Privacy consent checkbox on all forms

### Accessibility
- [ ] All images have alt text
- [ ] Color contrast WCAG AA minimum
- [ ] Tab navigation works on all forms
- [ ] Accessibility plugin installed

### Final QA
- [ ] All internal links work (no 404s)
- [ ] Phone numbers click-to-call on mobile
- [ ] Contact, application, referral forms tested end-to-end
- [ ] Employee login tested (create account → login → dashboard)
- [ ] Admin login tested (wp-admin access)
- [ ] Site tested: Chrome, Safari, Firefox, Edge
- [ ] Site tested: iPhone Safari, Android Chrome
- [ ] Footer copyright year current

---

## Recommended Plugin Stack

| Category | Plugin | License |
|----------|--------|--------|
| Page Builder | Elementor Pro | Paid |
| Custom Fields | ACF Pro | Paid |
| SEO | Rank Math | Free |
| Forms | Elementor Forms + WPForms | Free/Paid |
| SMTP | WP Mail SMTP | Free |
| Caching | SiteGround Optimizer | Free (hosting) |
| Image Optimization | Imagify or ShortPixel | Free tier |
| Security | Wordfence or SiteGround Security | Free |
| Backups | SiteGround Backup | Included |
| Cookie Consent | CookieYes | Free tier |
| Accessibility | WP Accessibility Helper | Free |
| User Login/Registration | ProfilePress | Free/Paid |
| Role-Based Access | Members (MemberPress) | Free |
| Documents | WP Document Revisions | Free |
| Login Protection | WPS Hide Login | Free |

**Estimated paid plugin cost at launch:** Elementor Pro (~$59–$99/yr) + ACF Pro (~$49/yr). Ask developer if they carry agency licenses — often included in their fee.
