# Homepage Blueprint
## New California For-Profit Care Agency Website

**Built for: WordPress + Elementor Pro + ACF**

---

## Design Principles

- **Mobile-first** — majority of caregiver applicants and family visitors are on mobile
- **Three audiences, one page** — Families, Referral Sources, Job Seekers each get a clear path
- **Trust at every scroll** — credentials, faces, testimonials, and logos woven throughout
- **Persistent conversion** — phone number and primary CTA always visible

---

## Section-by-Section Blueprint

### SECTION 1 — Top Bar (Utility Bar)

**Position:** Above main navigation  
**Purpose:** Instant access to the most important conversion actions  
**Elementor Widget:** Icon List + Button

**Content:**
```
📞 (XXX) XXX-XXXX   |   Serving [County] County + Surrounding Areas   |   [Make a Referral Button]
```

**Design Notes:**
- High-contrast background (navy or dark green)
- White text
- Phone number is click-to-call on mobile
- Referral button links directly to `/referral-sources/make-a-referral/`

---

### SECTION 2 — Main Navigation Header

**Position:** Sticky — remains visible on scroll  
**Purpose:** Audience routing and brand anchoring  
**Elementor Widget:** Nav Menu (sticky)

**Navigation Structure:**
```
[Logo]    About ▾    Services ▾    For Families    Referral Sources ▾    Careers    Resources    Contact
                                                                                [Get Started — Button CTA]
```

**Design Notes:**
- Logo left-aligned
- "Get Started" button in header (high contrast — filled button, not ghost)
- Dropdown menus for About, Services, Referral Sources
- On mobile: hamburger menu, phone number, Get Started button

---

### SECTION 3 — Hero Section

**Position:** Full-width, above the fold  
**Purpose:** Immediate trust, emotional connection, and clear CTA  
**Elementor Widget:** Full-width section with background image/video + text overlay

**Content:**
```
HEADLINE:
"Empowering Independent Lives Across California"

SUBHEADLINE:
"Person-centered care services for individuals with developmental disabilities.
Supporting families, partnering with regional centers, and building a team
of compassionate caregivers."

PRIMARY CTA BUTTON:    [Get Started]
SECONDARY CTA BUTTON:  [Make a Referral]
```

**ACF Fields for Developer:**
- Hero Headline (text)
- Hero Subheadline (textarea)
- Hero Background Image (image)
- Primary CTA Label + URL (text + url)
- Secondary CTA Label + URL (text + url)

---

### SECTION 4 — Trust Bar / Credentials Strip

**Position:** Immediately below hero (no gap)  
**Purpose:** Instant credibility before visitor scrolls further  
**Elementor Widget:** Icon Box or Image Box row

**Content:**
```
[Icon] DDS Vendor #XXXXXX    |    [Icon] Licensed & Insured    |    [Icon] Serving [X] Regional Centers    |    [Icon] [X]+ Clients Supported    |    [Icon] Founded [Year]
```

---

### SECTION 5 — Mission Statement

**Content:**
```
EYEBROW TEXT: Our Mission

HEADLINE:
"We believe every person deserves to live with dignity, independence, and community."

BODY:
"[Agency Name] is a California-based care agency providing person-centered
Supported Living, Independent Living, and Community Integration services.
We partner with families, regional centers, and service coordinators to ensure
each individual receives the support they need — where they need it, when they need it."

CTA: [Learn About Us →]
```

---

### SECTION 6 — Services Overview

**Elementor Widget:** Card grid (3-column on desktop, 1-column on mobile)

| Card | Icon | Headline | Body | CTA |
|------|------|----------|------|-----|
| SLS | Home/house icon | Supported Living Services | Personalized in-home support for individuals living in their own homes or shared settings. | Learn More → |
| ILS | Person-walking icon | Independent Living Services | Skill-building and coaching to help individuals thrive independently in their communities. | Learn More → |
| Community Integration | Group/community icon | Community Integration | Connecting individuals to meaningful activities, relationships, and opportunities in the community. | Learn More → |
| Person-Centered Planning | Chart/person icon | Person-Centered Planning | Every support plan starts with the individual's goals, preferences, and vision for their future. | Learn More → |
| Respite & Crisis Support | Shield icon | Respite & Crisis Support | Reliable relief for families and fast-response support when it's needed most. | Learn More → |

---

### SECTION 7 — Why Choose Us

```
EYEBROW: Why Families and Partners Choose Us

✓  Person-Centered, Always
   We start with the individual — their goals, preferences, and vision. Every
   support plan is built around the person, not a program template.

✓  Qualified, Compassionate DSPs
   Our Direct Support Professionals are thoroughly screened, trained, and
   matched to each individual they support.

✓  Trusted by Regional Centers
   We are an active vendor partner with regional centers throughout California,
   with a track record of compliance, communication, and quality outcomes.

✓  Transparent, Responsive Communication
   Families and service coordinators always know what's happening. We return
   calls. We show up. We follow through.
```

---

### SECTION 8 — Testimonials

**Elementor Widget:** Testimonial Carousel or Grid

Minimum 3 testimonials at launch covering:
- A family member / parent
- A service coordinator or regional center contact
- A DSP / caregiver (for recruitment section credibility)

---

### SECTION 9 — Regional Center Partnerships

```
EYEBROW: Regional Center Partners

HEADLINE: Trusted Vendor Across California's Regional Center Network

[Logo grid of Regional Centers served — or text list if logos unavailable]

CTA: [For Service Coordinators →]    [Make a Referral →]
```

---

### SECTION 10 — Careers / Join Our Team Callout

```
EYEBROW: Careers

HEADLINE: Make a Difference Every Day

BODY:
"We're looking for compassionate, dedicated Direct Support Professionals
and caregivers to join our growing team. Competitive pay, flexible
scheduling, and a mission you can believe in."

CTA: [Explore Careers]    [Apply Now]
```

---

### SECTION 11 — Contact / Final CTA Strip

```
HEADLINE: Ready to Get Started?

SUBHEADLINE: Whether you're a family looking for support, a service coordinator
making a referral, or a caregiver looking for meaningful work — we're here.

[  Get Started — For Families  ]    [  Make a Referral  ]    [  Join Our Team  ]

Or call us directly: (XXX) XXX-XXXX
```

---

### SECTION 12 — Footer

```
[Logo]                     [Column 2]           [Column 3]         [Column 4]
[Tagline 1 line]           Services             Referral Sources   Contact
[Social icons]             - SLS                - For SCs          - Phone
[DDS Vendor #]             - ILS                - Make a Referral  - Email
[License info]             - Community Int.     - Capability PDF   - Address
                           - Person-Centered                       - Hours
                           About Us
                           - Our Story
                           - Team
                           - Credentials
                           Careers
                           Resources

© [Year] [Agency Name]. All Rights Reserved. | Privacy Policy | Terms of Use | Accessibility
```

---

## Homepage Mobile Priority Checklist

- [ ] Phone number click-to-call in top bar AND hero
- [ ] "Get Started" button visible without scrolling
- [ ] Navigation collapses to hamburger — test all dropdown items
- [ ] Hero image crops correctly on portrait phone
- [ ] Services grid is single-column
- [ ] Testimonial carousel has touch/swipe support
- [ ] Footer columns stack cleanly
- [ ] Load time under 3 seconds on 4G
