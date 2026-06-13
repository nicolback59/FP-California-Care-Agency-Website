# Brand Notes
## California Care Agency — Visual Identity Guidelines

**Version:** 1.0 (Draft — Awaiting Agency Assets)
**Date:** 2026-06-13

> All items marked **CONTENT NEEDED** require agency input before Elementor
> global styles can be finalized.

---

## Logo

| Asset | Status | File Format | Notes |
|-------|--------|-------------|-------|
| Primary logo (full color) | CONTENT NEEDED | SVG preferred | |
| Logo — white version (for dark bg) | CONTENT NEEDED | SVG/PNG | |
| Logo — dark version (for light bg) | CONTENT NEEDED | SVG/PNG | |
| Logo — icon/mark only | CONTENT NEEDED | SVG/PNG | For favicon |
| Favicon (32x32, 16x16) | CONTENT NEEDED | ICO or PNG | |
| Apple touch icon (180x180) | CONTENT NEEDED | PNG | |

**Logo Usage Rules:**
- CONTENT NEEDED (minimum clear space, minimum size, do-nots)

---

## Color Palette

### Primary Colors

| Name | Hex | RGB | Usage |
|------|-----|-----|-------|
| Primary | CONTENT NEEDED | | Buttons, headlines, links |
| Secondary | CONTENT NEEDED | | Accents, highlights |
| Accent | CONTENT NEEDED | | CTAs, badges |

### Supporting Colors

| Name | Hex | RGB | Usage |
|------|-----|-----|-------|
| Dark | CONTENT NEEDED | | Body text, dark backgrounds |
| Light | CONTENT NEEDED | | Light backgrounds, cards |
| White | #FFFFFF | 255,255,255 | Backgrounds |
| Success | #22C55E | 34,197,94 | Form confirmations |
| Warning | #F59E0B | 245,158,11 | Alerts |
| Error | #EF4444 | 239,68,68 | Form errors |

### Elementor Global Colors (Placeholder)

Until brand colors are confirmed, use these professional care/health defaults:

| Elementor Name | Placeholder Hex | Notes |
|----------------|-----------------|-------|
| Primary | #2563EB | Professional blue — replace with brand color |
| Secondary | #059669 | Health green — replace with brand color |
| Accent | #F59E0B | Warm accent — replace with brand color |
| Text | #1E293B | Dark slate for readability |
| Text Light | #64748B | Secondary text |
| Background | #F8FAFC | Light page background |
| White | #FFFFFF | Pure white |

**WCAG AA Contrast Requirements:**
- All text on white: minimum 4.5:1 ratio
- Large text on colored backgrounds: minimum 3:1 ratio
- Test all color combinations at https://webaim.org/resources/contrastchecker/

---

## Typography

### Fonts

| Role | Font | Weight | Notes |
|------|------|--------|-------|
| Heading | CONTENT NEEDED | Bold/700 | Or use placeholder below |
| Body | CONTENT NEEDED | Regular/400 | |
| Button | CONTENT NEEDED | SemiBold/600 | |
| Caption | CONTENT NEEDED | Regular/400 | |
| Navigation | CONTENT NEEDED | Medium/500 | |

**Placeholder Font Stack (until brand fonts confirmed):**

```css
/* Elementor Global Fonts — Placeholder */
Heading:    'Inter', sans-serif (Google Fonts — free)
Body:       'Inter', sans-serif
Alt Option: 'Nunito', sans-serif (warmer, approachable — common in healthcare)
```

### Type Scale

| Element | Size (Desktop) | Size (Mobile) | Weight | Line Height |
|---------|---------------|---------------|--------|-------------|
| H1 | 48–56px | 32–36px | 700 | 1.2 |
| H2 | 36–40px | 28–32px | 700 | 1.25 |
| H3 | 28–32px | 22–26px | 600 | 1.3 |
| H4 | 22–24px | 18–20px | 600 | 1.35 |
| Body Large | 18px | 16px | 400 | 1.6 |
| Body | 16px | 15px | 400 | 1.65 |
| Body Small | 14px | 13px | 400 | 1.6 |
| Caption | 12px | 12px | 400 | 1.5 |
| Button | 16px | 15px | 600 | 1 |
| Nav Item | 15px | 15px | 500 | 1 |

---

## Spacing System

Elementor uses a consistent spacing system. Recommended values:

| Name | Value | Usage |
|------|-------|-------|
| XS | 8px | Small gaps, icon spacing |
| SM | 16px | Inner padding, small margins |
| MD | 24px | Standard spacing |
| LG | 40px | Section padding (mobile) |
| XL | 64px | Section padding (desktop) |
| 2XL | 96px | Hero padding |
| 3XL | 128px | Feature section spacing |

---

## Button Styles

### Primary Button

```
Background: Primary brand color
Text: White
Border radius: 6px (or per brand)
Padding: 14px 28px
Font: 16px, SemiBold
Hover: Darken 10%
Focus: 3px offset outline (accessibility)
```

### Secondary Button

```
Background: Transparent
Border: 2px solid Primary color
Text: Primary color
Border radius: 6px
Padding: 12px 26px
Hover: Primary color background, white text
```

### Ghost Button (on dark backgrounds)

```
Background: Transparent
Border: 2px solid White
Text: White
Hover: White background, dark text
```

---

## Image Guidelines

### Photography Style

- Warm, natural lighting
- Authentic moments (not overly staged)
- Diverse representation
- Community settings, not clinical settings
- Positive, empowering imagery
- Avoid: medical equipment imagery, institutional settings

### Required Image Sizes

| Use | Size | Format |
|-----|------|--------|
| Hero/Banner | 1920×1080px min | WebP or JPG |
| Page Banner | 1440×480px | WebP or JPG |
| Team Headshots | 400×400px (1:1 ratio) | WebP or JPG |
| Service Cards | 800×600px (4:3) | WebP or JPG |
| Blog Featured | 1200×630px | WebP or JPG |
| Testimonial | 200×200px | WebP or JPG |
| Logo | Vector SVG preferred | SVG or PNG@2x |

### Image Optimization

- Convert all images to WebP on upload (use Imagify or ShortPixel plugin)
- Maximum file size: 200KB for most images, 500KB for heroes
- Always add descriptive alt text (required for ADA compliance)
- Never use images with text embedded (use HTML text instead)

---

## Iconography

| Style Recommendation | Notes |
|---------------------|-------|
| Outline icons preferred | Lighter, modern feel |
| Solid icons for emphasis | CTAs, key features |
| Icon library | Phosphor Icons (free) or Flaticon (subscription) |
| Icon size consistency | 24px inline, 48px feature icons |
| Icon color | Brand primary or accessible gray |

**Elementor icon library:** Use built-in Font Awesome icons or upload custom SVG icons.

---

## Photography Sources (Until Agency Photos Available)

If real agency photos are not yet available, use:

1. **Unsplash** — Free, no attribution required for most images
   - Search: "home care," "independent living," "community support"
2. **Pexels** — Free stock photography
3. **Shutterstock/Getty** — Paid, higher quality/exclusivity
4. **iStock** — Subscription or per-image

> **Reminder:** Replace ALL stock photos with real agency photos before or shortly after launch.
> Real photos of staff and clients (with consent) dramatically improve trust and conversions.

---

## Brand Voice & Tone

| Dimension | Direction |
|-----------|-----------|
| **Tone** | CONTENT NEEDED — [Warm and professional? Direct and reassuring?] |
| **Voice** | CONTENT NEEDED — [First-person "we"? Second-person "you"?] |
| **Formality** | CONTENT NEEDED — [Conversational? Clinical? Somewhere between?] |
| **Key messages** | CONTENT NEEDED |
| **Words to use** | CONTENT NEEDED |
| **Words to avoid** | CONTENT NEEDED |
| **Audience language** | Person-first language always (e.g., "individual with a disability" not "disabled person") |

---

*Update this file when agency branding materials are received.*
