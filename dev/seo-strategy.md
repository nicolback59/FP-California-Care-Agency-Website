# SEO Strategy
## California Care Agency Website

**Version:** 1.0
**Date:** 2026-06-13
**Tool:** Rank Math SEO (free)

---

## Local SEO Focus

This is a **local services business** targeting families, individuals, and service
coordinators in specific California counties. Local SEO is the top priority.

### Primary Keyword Targets

| Keyword | Intent | Page Target |
|---------|--------|-------------|
| Supported Living Services California | Service Seeker | SLS page |
| SLS care agency [county] | Local Service | SLS page + local |
| Independent Living Services California | Service Seeker | ILS page |
| ILS regional center California | Service Seeker | ILS page |
| Care agency [city/county] California | Local Search | Home page |
| Community integration services California | Service Seeker | Community page |
| Respite care developmental disabilities California | Service Seeker | Respite page |
| DDS vendored agency California | Trust/Credential | Home/About/Compliance |
| Direct support professional jobs [county] | Job Seeker | Careers page |
| DSP jobs California | Job Seeker | Careers page |
| Regional center services CONTENT NEEDED | Local/Partner | Home/About |

**Note:** Replace [county] and [city] with actual service areas once confirmed.

---

## URL Structure

All URLs follow:
```
Domain:     https://[yourdomain.com]
Structure:  /%postname%/
Services:   /services/[service-name]/
Blog:       /blog/[post-name]/
```

### Target URLs

| Page | URL |
|------|-----|
| Home | `https://yourdomain.com/` |
| SLS | `https://yourdomain.com/services/supported-living-services/` |
| ILS | `https://yourdomain.com/services/independent-living-services/` |
| Community Integration | `https://yourdomain.com/services/community-integration/` |
| Person-Centered Planning | `https://yourdomain.com/services/person-centered-planning/` |
| Respite Care | `https://yourdomain.com/services/respite-care/` |
| Crisis Support | `https://yourdomain.com/services/crisis-support/` |

---

## Title Tag Structure

Format: `[Page Topic] | [Agency Name] | [City, CA]`

```
Home:        [Agency Name] | Supported Living & Care Services | [City, CA]
SLS Page:    Supported Living Services in [City, CA] | [Agency Name]
ILS Page:    Independent Living Services in [City, CA] | [Agency Name]
About:       About [Agency Name] | DDS Vendored Care Agency | [City, CA]
Careers:     DSP Jobs at [Agency Name] | [City, CA]
Contact:     Contact [Agency Name] | [City, CA] Care Agency
```

**Rules:**
- Maximum 60 characters (avoid truncation in Google)
- Lead with keyword, not agency name (except home page)
- Include city/county where space allows
- Every page must have a unique title

---

## Meta Description Structure

```
Home:
"[Agency Name] provides DDS-funded Supported Living, Independent Living,
and Community Integration services in [County], California. Vendored with
[RC Name]. Call [phone] to start services."
(~155 characters)

SLS Page:
"Our Supported Living Services help adults with developmental disabilities
live in their own homes with personalized support. DDS vendored, serving
[Counties]. Inquire today."
(~160 characters)

Careers:
"Join [Agency Name] as a Direct Support Professional in [City, CA].
Starting at $XX/hr, paid training, flexible schedule. Apply for DSP
positions today."
(~155 characters)
```

**Rules:**
- 140–160 characters (avoid truncation)
- Include target keyword naturally
- Include call to action ("Call," "Learn More," "Apply Today")
- Every page must have a unique meta description

---

## Schema Markup (Structured Data)

Configure via Rank Math on each page type:

### Home Page — LocalBusiness Schema

```json
{
  "@context": "https://schema.org",
  "@type": "LocalBusiness",
  "name": "CONTENT NEEDED",
  "description": "CONTENT NEEDED",
  "url": "https://CONTENT NEEDED",
  "telephone": "CONTENT NEEDED",
  "email": "CONTENT NEEDED",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "CONTENT NEEDED",
    "addressLocality": "CONTENT NEEDED",
    "addressRegion": "CA",
    "postalCode": "CONTENT NEEDED",
    "addressCountry": "US"
  },
  "geo": {
    "@type": "GeoCoordinates",
    "latitude": "CONTENT NEEDED",
    "longitude": "CONTENT NEEDED"
  },
  "openingHours": "CONTENT NEEDED",
  "sameAs": [
    "https://www.linkedin.com/company/CONTENT NEEDED",
    "https://www.facebook.com/CONTENT NEEDED"
  ],
  "areaServed": {
    "@type": "State",
    "name": "California"
  },
  "hasMap": "CONTENT NEEDED (Google Maps URL)"
}
```

### Service Pages — Service Schema

```json
{
  "@context": "https://schema.org",
  "@type": "Service",
  "serviceType": "CONTENT NEEDED (e.g., Supported Living Services)",
  "provider": {
    "@type": "LocalBusiness",
    "name": "CONTENT NEEDED"
  },
  "areaServed": {
    "@type": "State",
    "name": "California"
  },
  "description": "CONTENT NEEDED"
}
```

### FAQ Pages — FAQPage Schema

```json
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "Question text here",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Answer text here"
      }
    }
  ]
}
```

Enable FAQPage schema in Rank Math by adding FAQ blocks with the Rank Math FAQ block in Gutenberg, or by using Rank Math's built-in FAQ widget.

### Job Listings — JobPosting Schema

```json
{
  "@context": "https://schema.org",
  "@type": "JobPosting",
  "title": "Direct Support Professional",
  "description": "CONTENT NEEDED",
  "datePosted": "CONTENT NEEDED",
  "hiringOrganization": {
    "@type": "Organization",
    "name": "CONTENT NEEDED",
    "sameAs": "CONTENT NEEDED"
  },
  "jobLocation": {
    "@type": "Place",
    "address": {
      "@type": "PostalAddress",
      "addressLocality": "CONTENT NEEDED",
      "addressRegion": "CA",
      "addressCountry": "US"
    }
  },
  "baseSalary": {
    "@type": "MonetaryAmount",
    "currency": "USD",
    "value": {
      "@type": "QuantitativeValue",
      "minValue": "CONTENT NEEDED",
      "maxValue": "CONTENT NEEDED",
      "unitText": "HOUR"
    }
  },
  "employmentType": "FULL_TIME"
}
```

---

## Google Business Profile

### Setup Checklist

```
□ Claim or create Google Business Profile at business.google.com
□ Business name: Exact legal name (consistent with website)
□ Category: "Care Agency" or "Social Services Organization" or "Home Health Agency"
□ Address: Verified physical address
□ Service area: Add all counties served (if you go to clients)
□ Phone number: Consistent with website
□ Website URL: https://yourdomain.com
□ Business hours: Accurate
□ Description: 750-character keyword-rich description of services
□ Services: List all DDS-funded services offered
□ Photos: Upload 10+ photos (office, team, community — no client photos without consent)
□ Attributes: Set relevant accessibility and service attributes
□ Q&A: Pre-populate with common questions and answers
□ Posts: Set up regular Google Posts (announcements, offers, events)
```

### Review Strategy

```
Who to ask for reviews:
- Satisfied service coordinators (most valuable)
- Family members (with permission, ensure no HIPAA issues)
- Employees (for employer reputation)
- Community partners

When to ask:
- After successful service onboarding
- After a positive interaction
- After resolving a challenge well
- At annual check-in

How to ask:
- Direct link to your review page (shortcut from business.google.com)
- QR code in office
- Email follow-up after positive interaction
- NEVER incentivize reviews (violates Google's terms)

Response policy:
- Respond to ALL reviews (positive and negative)
- Positive: Thank them, mention specific service if possible
- Negative: Apologize, offer to discuss offline (do NOT include PHI in response)
```

---

## Sitemap & Indexing

### XML Sitemap Configuration (Rank Math)

```
Include in sitemap:
✅ All public pages
✅ Service pages
✅ Blog posts
✅ Job listing pages
✅ Team member pages

Exclude from sitemap:
❌ /employee-portal/ and all sub-pages
❌ /admin-portal/ and all sub-pages
❌ /login/
❌ /register/
❌ /forgot-password/
❌ Any page set to noindex
```

Submit sitemap to:
- Google Search Console: `https://yourdomain.com/sitemap.xml`
- Bing Webmaster Tools: same URL

### robots.txt

```
User-agent: *
Allow: /
Disallow: /employee-portal/
Disallow: /admin-portal/
Disallow: /login/
Disallow: /register/
Disallow: /forgot-password/
Disallow: /wp-admin/
Disallow: /wp-login.php

Sitemap: https://yourdomain.com/sitemap.xml
```

---

## Content SEO Strategy

### Priority Content to Create at Launch

1. **Home page** — Target: brand name + city + care agency
2. **SLS page** — Target: "supported living services [county] california"
3. **ILS page** — Target: "independent living services california regional center"
4. **Careers page** — Target: "DSP jobs [county]" + "direct support professional hiring"

### Phase 2 Content (30–90 Days Post-Launch)

1. **Blog post:** "What is Supported Living Services? A Family Guide"
2. **Blog post:** "How to Request Services Through Your Regional Center"
3. **Blog post:** "What DSPs Do: A Day in the Life"
4. **Resource page:** "California Regional Center Guide"
5. **Service area pages** (if multiple counties): `/services/supported-living-services-[county]/`

### Internal Linking Strategy

```
Every service page → links to:
  - Related services (bottom of page)
  - Contact page (multiple CTAs)
  - For Families: How It Works

For Families pages → links to:
  - All service pages
  - Contact/referral

Careers page → links to:
  - About Us (culture)
  - Contact (general)

Blog posts → links to:
  - Relevant service pages
  - Contact/referral CTA
  - Other related blog posts
```

---

## Performance SEO (Core Web Vitals)

Google uses Core Web Vitals as a ranking factor. Target:

| Metric | Target | What It Measures |
|--------|--------|-----------------|
| LCP (Largest Contentful Paint) | < 2.5 seconds | How fast main content loads |
| FID (First Input Delay) | < 100ms | How fast page responds to clicks |
| CLS (Cumulative Layout Shift) | < 0.1 | How much page moves while loading |

**Improvements:**
- Compress and convert all images to WebP
- Enable caching (SiteGround Optimizer or WP Rocket)
- Minimize CSS/JS (Elementor Asset Optimization)
- Use a CDN (Cloudflare free plan)
- Choose fast hosting (SiteGround, WP Engine, Kinsta)

---

## Monthly SEO Maintenance

```
Monthly tasks:
□ Review Google Search Console for errors
□ Check for new 404 errors and set up redirects
□ Review top-performing pages and update if needed
□ Publish 1-2 blog posts
□ Respond to any new Google Business reviews
□ Post 2-4 Google Business Profile posts
□ Check page speed (run PageSpeed Insights on home + 1 service page)

Quarterly tasks:
□ Review keyword rankings for target terms
□ Review competitor sites for new content opportunities
□ Update any outdated service information or staff changes
□ Review and update meta descriptions for low-performing pages
□ Check for broken internal/external links
□ Review Google Analytics: top pages, bounce rates, conversions
```

---

*SEO is a long-term investment. Expect 3–6 months before significant organic traffic from new keyword targets. Local SEO (Google Business Profile) produces faster results.*
