# Assets Directory
## California Care Agency Website

**Last Updated:** 2026-06-13

---

## Purpose

This directory stores all website assets that are tracked in the repository.

> **Note:** Large binary files (high-resolution images, videos) should NOT be
> committed to git. Use the subdirectory structure below and reference files
> from the staging server or cloud storage instead.

---

## Directory Structure

```
/assets/
├── README.md               ← This file
├── logos/                  ← Agency logo files
├── images/                 ← Web-optimized images
│   ├── hero/               ← Homepage and page hero images
│   ├── team/               ← Staff headshots
│   ├── services/           ← Service page images
│   └── general/            ← General site imagery
├── icons/                  ← Custom SVG icons
├── documents/              ← Downloadable PDFs (public)
│   └── employee-portal/    ← Employee documents (private — NOT committed to git)
├── fonts/                  ← Self-hosted web fonts (if not using Google Fonts)
└── brand/                  ← Brand guidelines, style guide
```

---

## Asset Status

| Asset | Status | Notes |
|-------|--------|-------|
| Primary logo (SVG) | CONTENT NEEDED | |
| Logo — white version | CONTENT NEEDED | |
| Logo — dark version | CONTENT NEEDED | |
| Favicon (ICO/PNG) | CONTENT NEEDED | |
| Apple touch icon | CONTENT NEEDED | |
| Hero image — Home | CONTENT NEEDED | |
| Hero image — About | CONTENT NEEDED | |
| Hero image — Services | CONTENT NEEDED | |
| Hero image — Careers | CONTENT NEEDED | |
| Team headshots | CONTENT NEEDED | Professional photos required |
| Service imagery (x6) | CONTENT NEEDED | |
| Community/activity photos | CONTENT NEEDED | With model releases |
| Capability Statement PDF | CONTENT NEEDED | Downloadable leave-behind |

---

## File Naming Convention

Use lowercase, hyphenated filenames. No spaces or special characters.

```
Good:  agency-logo-primary.svg
Good:  hero-home-1920x1080.webp
Good:  jane-doe-headshot.webp
Bad:   Agency Logo.SVG
Bad:   HeroImage_Final_v2.JPG
Bad:   Staff Photo (1).jpg
```

---

## Image Size Requirements

| Use Case | Dimensions | Format | Max Size |
|----------|-----------|--------|---------|
| Hero images | 1920×1080px | WebP (JPG fallback) | 500KB |
| Page banners | 1440×480px | WebP | 300KB |
| Team headshots | 400×400px | WebP | 100KB |
| Service cards | 800×600px | WebP | 200KB |
| Blog featured | 1200×630px | WebP | 300KB |
| OG/Social preview | 1200×630px | JPG | 200KB |
| Testimonial photos | 200×200px | WebP | 50KB |
| Logo (raster) | 400×200px min | PNG (transparent) | 50KB |

---

## Logo Files Needed From Agency

When the agency provides logo files, store them in `/assets/logos/` and confirm:

```
□ Primary logo (full color) — SVG
□ Primary logo (full color) — PNG with transparent background
□ Logo — white version (for dark backgrounds)
□ Logo — dark/black version (for light backgrounds)
□ Logo — horizontal version
□ Logo — stacked/vertical version (if available)
□ Logomark/icon only (for favicon)
```

---

## Employee Documents

Employee portal documents (handbook, forms, policies) should be stored:

- **During development:** In `/assets/documents/employee-portal/` (LOCAL ONLY — do not commit to public repo)
- **On live server:** In `/wp-content/uploads/employee-documents/` (protected directory)
- **Backup:** In Google Drive or other cloud storage

> **SECURITY WARNING:** Do NOT commit confidential HR documents, employee
> information, or sensitive agency documents to this public GitHub repository.
> Use the WordPress media library or a private file storage service.

---

## Downloadable Public Documents

These documents will be publicly available for download from the website:

| Document | Status | URL |
|----------|--------|-----|
| Capability Statement PDF | CONTENT NEEDED | /documents/capability-statement.pdf |
| Service Overview PDF | CONTENT NEEDED | /documents/services-overview.pdf |
| Referral Packet | CONTENT NEEDED | /documents/referral-packet.pdf |
| Agency Overview (for families) | CONTENT NEEDED | /documents/agency-overview.pdf |

---

## Image Sources (Until Agency Photos Available)

If agency photography is not yet available:

| Source | License | Notes |
|--------|---------|-------|
| Unsplash.com | Free | No attribution required |
| Pexels.com | Free | No attribution required |
| StockSnap.io | Free | CC0 license |
| Pixabay.com | Free | Some require attribution |

Search terms: "home care," "independent living," "community support," "disability inclusion," "caregiver," "independent adult"

**Reminder:** Replace all stock photos with real agency photos as soon as possible. Real photos dramatically improve trust and engagement.

---

*Update this README when new assets are added. Keep the status table current.*
