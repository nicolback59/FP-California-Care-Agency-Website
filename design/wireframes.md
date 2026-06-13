# Wireframe Recommendations
## California Care Agency — Page Layout Specifications

**Version:** 1.0
**Date:** 2026-06-13
**Platform:** WordPress + Elementor Pro
**Approach:** Section-by-section Elementor layout specifications

---

## HOME PAGE WIREFRAME

### Section 1 — Hero

```
┌─────────────────────────────────────────────────────────────────┐
│  [STICKY HEADER]  LOGO  |  About  Services  Families  Careers  │
│                                    Contact  📞 (XXX) XXX-XXXX  │
├─────────────────────────────────────────────────────────────────┤
│                                                                  │
│   [FULL-WIDTH HERO IMAGE — dark overlay gradient]               │
│                                                                  │
│   ┌──────────────────────────────────┐                          │
│   │  HEADLINE (H1, White, Large)     │                          │
│   │  Supporting text (White, 18px)   │                          │
│   │                                  │                          │
│   │  [PRIMARY CTA]  [SECONDARY CTA]  │                          │
│   └──────────────────────────────────┘                          │
│                                                                  │
│   Height: 90vh desktop, auto mobile                             │
└─────────────────────────────────────────────────────────────────┘
```

**Elementor Elements:**
- Section: Full-width, min-height 90vh
- Background: Image with overlay (semi-transparent dark gradient)
- Inner section: 2 columns (content 60% + empty 40%)
- Widgets: Heading, Text Editor, Button (x2)

### Section 2 — Trust Bar

```
┌─────────────────────────────────────────────────────────────────┐
│  [DDS Vendored]  [Insured & Bonded]  [Background Checked]       │
│  [XX Years Experience]  [Regional Center Partner]               │
└─────────────────────────────────────────────────────────────────┘
```

**Elementor Elements:**
- Section: Full-width, background: primary color, 60px padding
- Inner section: 5 equal columns
- Each column: Icon Widget + Text Widget

### Section 3 — Mission

```
┌─────────────────────────────────────────────────────────────────┐
│                                                                  │
│   ┌────────────────┐    ┌─────────────────────────────────┐    │
│   │                │    │  H2: Our Mission                 │    │
│   │  [IMAGE]       │    │                                  │    │
│   │  600x500px     │    │  Mission statement paragraph     │    │
│   │                │    │                                  │    │
│   │                │    │  Values:                         │    │
│   │                │    │  ● Value 1                       │    │
│   │                │    │  ● Value 2                       │    │
│   │                │    │  ● Value 3                       │    │
│   └────────────────┘    └─────────────────────────────────┘    │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

**Elementor Elements:**
- Section: Boxed, 80px vertical padding
- 2 columns: Image (50%) + Content (50%)
- Widgets: Image, Heading, Text, Icon List

### Section 4 — Services Grid

```
┌─────────────────────────────────────────────────────────────────┐
│                                                                  │
│              H2: Our Services (centered)                        │
│              Supporting text (centered)                         │
│                                                                  │
│   ┌─────────┐  ┌─────────┐  ┌─────────┐  ┌─────────────────┐  │
│   │ [ICON]  │  │ [ICON]  │  │ [ICON]  │  │   (Responsive:  │  │
│   │         │  │         │  │         │  │   3 cols desktop │  │
│   │  SLS    │  │  ILS    │  │Community│  │   2 cols tablet  │  │
│   │         │  │         │  │         │  │   1 col mobile)  │  │
│   │  Brief  │  │  Brief  │  │  Brief  │  │                  │  │
│   │  desc   │  │  desc   │  │  desc   │  │                  │  │
│   │         │  │         │  │         │  │                  │  │
│   │[Learn ▶]│  │[Learn ▶]│  │[Learn ▶]│  │                  │  │
│   └─────────┘  └─────────┘  └─────────┘  └─────────────────┘  │
│                                                                  │
│   [Row 2: Person-Centered | Respite | Crisis Support]           │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

**Elementor Elements:**
- Section: Full-width, light background (#F8FAFC), 96px padding
- Inner: 3-column grid (responsively stacks)
- Each card: Icon Box widget (custom) with link button
- Or: Custom card using: Image/Icon, Heading, Text, Button

### Section 5 — Why Choose Us

```
┌─────────────────────────────────────────────────────────────────┐
│  [DARK/BRAND COLOR BACKGROUND]                                  │
│                                                                  │
│              H2: Why Families Choose Us (white)                 │
│                                                                  │
│  ┌──────────────┐ ┌──────────────┐ ┌──────────────┐ ┌────────┐ │
│  │  ✓ [Title]   │ │  ✓ [Title]   │ │  ✓ [Title]   │ │ [Title]│ │
│  │  Description │ │  Description │ │  Description │ │ Desc.  │ │
│  └──────────────┘ └──────────────┘ └──────────────┘ └────────┘ │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

### Section 6 — Regional Center Info

```
┌─────────────────────────────────────────────────────────────────┐
│                                                                  │
│  ┌──────────────────────────┐  ┌──────────────────────────────┐ │
│  │  H2: DDS Vendored &      │  │  [RC Partner Logos/Names]    │ │
│  │      Regional Center     │  │                              │ │
│  │      Partner             │  │  [Make a Referral Button]    │ │
│  │                          │  │                              │ │
│  │  Body explaining the     │  │  Vendor #: CONTENT NEEDED    │ │
│  │  referral process        │  │                              │ │
│  │                          │  │                              │ │
│  └──────────────────────────┘  └──────────────────────────────┘ │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

### Section 7 — Testimonials

```
┌─────────────────────────────────────────────────────────────────┐
│  [LIGHT BACKGROUND]                                             │
│                                                                  │
│              H2: What Families Are Saying                       │
│                                                                  │
│  ◀  ┌───────────────────────────────────────────────────┐  ▶  │
│     │                                                   │       │
│     │  "Testimonial quote text goes here..."            │       │
│     │                                                   │       │
│     │  — First Name, Relationship (e.g., Parent)        │       │
│     │                                                   │       │
│     └───────────────────────────────────────────────────┘       │
│                                                                  │
│                    ● ○ ○ ○  (dots)                               │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

**Elementor Elements:** Testimonial Carousel widget (Elementor Pro)

### Section 8 — Careers CTA

```
┌─────────────────────────────────────────────────────────────────┐
│  [BACKGROUND IMAGE — community/team photo, overlay]             │
│                                                                  │
│         H2: Join Our Team                                       │
│         Supporting text about culture and opportunity           │
│                                                                  │
│    ● $XX/hr starting   ● Flexible Schedule   ● Paid Training   │
│    ● Mileage Reimb.    ● PTO                 ● Benefits        │
│                                                                  │
│              [View Open Positions]                               │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

### Section 9 — Contact CTA

```
┌─────────────────────────────────────────────────────────────────┐
│                                                                  │
│  ┌──────────────────────────┐  ┌──────────────────────────────┐ │
│  │  H2: Ready to Get        │  │  [CONTACT FORM — Short]      │ │
│  │      Started?            │  │                              │ │
│  │                          │  │  Name: [_____________]       │ │
│  │  Phone: (XXX) XXX-XXXX  │  │  Email: [____________]       │ │
│  │  Email: xxx@xxx.com      │  │  I am a: [dropdown_____]    │ │
│  │  Hours: Mon–Fri 9–5      │  │  Message: [__________]      │ │
│  │                          │  │           [__________]      │ │
│  │                          │  │  [Submit Inquiry]           │ │
│  └──────────────────────────┘  └──────────────────────────────┘ │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

---

## ABOUT PAGE WIREFRAME

```
[HERO — Page title banner with background image]
[BREADCRUMB — Home > About]

[SECTION: Our Story — 2 cols: Image | Text]
[SECTION: Mission & Vision — centered, light bg]
[SECTION: Core Values — 3 or 4 icon cards]
[SECTION: Leadership Team — photo grid]
  - Each card: headshot + name + title + bio excerpt + [Read More]
[SECTION: Credentials & Compliance — list with icons]
[SECTION: CTA — "Let's Work Together" → Contact]
```

---

## SERVICE PAGE WIREFRAME (Template for all 6 services)

```
[HERO — Title + brief description + dual CTAs]
[BREADCRUMB — Home > Services > [Service Name]]

[SECTION 1: What Is [Service]? — plain language explanation]
[SECTION 2: Who It Serves — eligibility, ideal candidate]
[SECTION 3: What Support Looks Like — icon grid or bullet columns]
[SECTION 4: Our Approach — differentiator paragraph]
[SECTION 5: FAQ — accordion (Elementor Toggle widget)]
[SECTION 6: Related Services — card grid]
[SECTION 7: CTA — Inquiry form or phone number]
```

---

## CONTACT PAGE WIREFRAME

```
[HERO — "Get in Touch" with background]
[BREADCRUMB — Home > Contact]

[SECTION: 2 columns]
  Left column:
    - Phone (click-to-call link)
    - Email
    - Address
    - Hours
    - Google Map embed
  
  Right column:
    - Contact form (multiple audience paths)
    - For: Individual/Family | Service Coordinator | Job Seeker | Other

[SECTION: Referral Inquiry — separate form for SCs]
```

---

## CAREERS PAGE WIREFRAME

```
[HERO — "Make a Difference" with team/community imagery]

[SECTION: Why Work With Us — 4-column benefit cards]
[SECTION: DSP Role Description — 2 columns: text + image]
[SECTION: Compensation & Benefits — icon list]
[SECTION: Current Openings — Job Listings CPT loop]
  - Each job card: Title | Location | Type | Pay | [Apply Now]
[SECTION: Hiring Process — numbered steps]
[SECTION: Apply CTA — Application form embed]
```

---

## EMPLOYEE PORTAL WIREFRAME

```
[HEADER — Portal-specific header: Logo + Employee name + Logout]

[DASHBOARD]
┌─────────────────────────────────────────────────────────────────┐
│  Welcome, [Employee Name]           [Quick Links]              │
│                                                                  │
│  ┌──────────────┐ ┌──────────────┐ ┌──────────────┐           │
│  │ 📋 Onboarding│ │ 📖 Handbook  │ │ 🎓 Training  │           │
│  │  Checklist   │ │              │ │  Resources   │           │
│  └──────────────┘ └──────────────┘ └──────────────┘           │
│                                                                  │
│  ┌──────────────┐ ┌──────────────┐ ┌──────────────┐           │
│  │ 📄 Forms     │ │ 📢 Updates   │ │ 🔒 HR        │           │
│  │  & Downloads │ │              │ │  Resources   │           │
│  └──────────────┘ └──────────────┘ └──────────────┘           │
│                                                                  │
│  [Announcements Feed]                                            │
└─────────────────────────────────────────────────────────────────┘
```

---

## Wireframe Tools Recommended

For creating visual wireframes before Elementor build:

| Tool | Price | Notes |
|------|-------|-------|
| Figma | Free tier | Industry standard, shareable |
| Whimsical | Free tier | Fast wireframing, good for quick layouts |
| Miro | Free tier | Collaborative whiteboard |
| Balsamiq | $9/mo | Classic wireframe look |
| Elementor's own sections | Free | Sketch directly in Elementor |

**Recommendation:** Create Figma wireframes for Home, About, Services template, and Employee Portal before beginning Elementor build.

---

## Responsive Breakpoints (Elementor Default)

| Device | Width | Elementor Setting |
|--------|-------|-------------------|
| Desktop | 1025px+ | Default |
| Tablet | 768–1024px | Tablet mode |
| Mobile | 767px and below | Mobile mode |

All sections must be tested at all three breakpoints before launch.

---

*These wireframes represent the recommended structure. Final layout is determined during Elementor build.*
