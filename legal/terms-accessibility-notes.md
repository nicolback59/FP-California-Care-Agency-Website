# Terms of Use & Accessibility Statement Notes
## California Care Agency Website

**Version:** 1.0 (Planning Notes — NOT final legal documents)
**Date:** 2026-06-13

> **IMPORTANT DISCLAIMER:**
> These are planning notes only. The Terms of Use must be reviewed by
> a licensed attorney. The Accessibility Statement is a commitment
> document — ensure you can actually fulfill what it states.

---

## PART 1: TERMS OF USE

### Why a Terms of Use is Needed

- Protects the agency from liability for website use
- Sets rules for how visitors may use site content
- Addresses intellectual property (content ownership)
- Limits agency liability for information accuracy
- Required by best practices for professional websites
- Regional center partners may review terms

---

### Terms of Use Required Sections

**1. Acceptance of Terms**
```
By accessing this website, visitors agree to these terms.
If they don't agree, they should not use the site.
```

**2. Use of Site**
```
Permitted uses:
- Personal, non-commercial use
- Viewing agency information
- Submitting inquiries

Prohibited uses:
- Scraping or harvesting data
- Spam or abuse of contact forms
- Impersonating agency staff
- Republishing site content without permission
- Using site to distribute malware
- Attempting to access unauthorized areas
```

**3. Intellectual Property**
```
All site content owned by [Agency Name]:
- Text content
- Logo and branding
- Photography (ensure photographer releases are on file)
- Layout and design

Exception: Third-party content used with license or permission
```

**4. Disclaimer of Warranties**
```
Website provided "as is" — no warranties of accuracy or completeness.
Information on site is for general informational purposes only.
Not a substitute for professional medical, legal, or financial advice.
```

**5. Limitation of Liability**
```
Agency not liable for:
- Errors or omissions in website content
- Damages from use or inability to use the site
- Third-party linked content
- Technical issues or downtime
```

**6. Medical/Care Disclaimer**
```
IMPORTANT FOR CARE AGENCIES:
"The information provided on this website is for general informational
purposes only and does not constitute medical advice, clinical treatment,
or a doctor-patient relationship. Specific care plans are developed
individually in coordination with regional centers, service coordinators,
and the individuals we serve."
```

**7. Third-Party Links**
```
Site may link to third-party sites.
Agency is not responsible for third-party content or policies.
```

**8. Privacy Policy**
```
Link to and reference Privacy Policy as a separate document.
```

**9. Employee Portal Terms**
```
Employee portal access:
- For authorized employees only
- Login credentials are personal and confidential
- Sharing login credentials is prohibited
- Agency may monitor portal usage for security
- Unauthorized access may result in disciplinary action and legal consequences
```

**10. Modifications**
```
Agency reserves right to modify terms at any time.
Continued use after modification = acceptance.
```

**11. Governing Law**
```
These terms governed by laws of the State of California.
Disputes subject to jurisdiction of [County] County, California courts.
```

**12. Contact Information**
```
Questions about Terms: [email address]
```

**13. Effective Date**
```
[Date]
```

---

### Attorney Checklist for Terms of Use

```
□ Agency legal name confirmed throughout
□ Care-specific disclaimers reviewed
□ Employee portal section reviewed for employment law compliance
□ California law governing clause confirmed
□ Limitation of liability reviewed for enforceability in CA
□ Medical disclaimer reviewed
□ HIPAA considerations confirmed
□ Intellectual property ownership confirmed (any stock photos licensed?)
```

---

## PART 2: ACCESSIBILITY STATEMENT

### Purpose of an Accessibility Statement

1. Demonstrates commitment to ADA/Section 508/WCAG compliance
2. Expected by regional center partners (some require it for vendored agencies)
3. Protects against ADA compliance complaints
4. Provides a contact mechanism for accessibility issues
5. Signals to users with disabilities that the site is designed for them

---

### WCAG Standard

**Target standard:** WCAG 2.1 Level AA

```
WCAG 2.1 Level A:    Minimum — basic accessibility
WCAG 2.1 Level AA:   Standard — required for most legal compliance
WCAG 2.1 Level AAA:  Enhanced — above and beyond

For a care agency serving individuals with disabilities, AA minimum is expected.
```

---

### Accessibility Statement Template

**URL:** `/accessibility/`

```
---
ACCESSIBILITY STATEMENT

[Agency Name] is committed to ensuring digital accessibility for people
with disabilities. We continually improve the user experience for everyone
and apply relevant accessibility standards.

CONFORMANCE STATUS

We aim to conform to the Web Content Accessibility Guidelines (WCAG) 2.1
Level AA. These guidelines explain how to make web content more accessible
to people with disabilities.

CURRENT STATUS

[Agency Name] is in the process of reviewing and improving accessibility
across our website. We are working to identify and address any accessibility
issues.

KNOWN LIMITATIONS

If you encounter any accessibility barriers on our site, please let us know.

TECHNICAL SPECIFICATIONS

Our website relies on the following technologies:
- HTML
- CSS
- JavaScript
- WordPress
- Elementor

ASSESSMENT APPROACH

[Agency Name] assesses the accessibility of our website by:
- Self-evaluation
- Use of automated accessibility testing tools
- User feedback

FEEDBACK AND CONTACT

If you experience accessibility barriers on our website, or if you need
information in an alternative format, please contact us:

Email:   CONTENT NEEDED
Phone:   CONTENT NEEDED
Address: CONTENT NEEDED

We aim to respond to accessibility feedback within 5 business days.

FORMAL COMPLAINTS

If you are not satisfied with our response, you may contact the California
Department of Rehabilitation or file a complaint with the U.S. Department
of Justice Civil Rights Division.

EFFECTIVE DATE: [Date]
LAST REVIEWED: [Date]
---
```

---

### Accessibility Implementation Requirements

#### Developer Checklist

```
HTML Structure:
□ Semantic HTML5 elements (nav, main, header, footer, article, section)
□ Logical heading hierarchy (H1 → H2 → H3, no skipped levels)
□ html lang="en" attribute on root element
□ Page title changes with each page

Images:
□ All informative images: descriptive alt text
□ Decorative images: alt="" (empty alt attribute)
□ Complex images (charts, graphs): long description provided
□ No text embedded in images

Color & Contrast:
□ Normal text: minimum 4.5:1 contrast ratio against background
□ Large text (18pt+ or 14pt bold): minimum 3:1 contrast ratio
□ UI components (buttons, form borders): minimum 3:1 contrast
□ Not conveying information by color alone

Keyboard Navigation:
□ All functionality accessible via keyboard
□ Focus order is logical (top-to-bottom, left-to-right)
□ Focus indicator visible on all interactive elements
□ No keyboard traps
□ Skip navigation link as first focusable element

Forms:
□ All form inputs have associated labels (for/id matching)
□ Required fields indicated (aria-required="true")
□ Error messages: descriptive and linked to specific field
□ No timeout on forms (or user can extend)
□ Submit button has descriptive text (not just "Submit")

Links:
□ Link text is descriptive (no "click here" or "read more" alone)
□ Links visually distinguishable from surrounding text
□ External links indicate they open in new tab (aria-label)
□ PDF links indicate file type and size

Video & Audio (if used):
□ Captions on all videos (auto-captions reviewed for accuracy)
□ Audio descriptions for visual content
□ No autoplay audio
□ Volume control available

Interactive Elements:
□ ARIA labels on icon-only buttons
□ Expanded/collapsed state announced for accordions (aria-expanded)
□ Modal dialogs: focus managed, close with Escape key
□ Carousels: pause button available, keyboard controllable
```

#### Testing Tools

```
Automated Testing (catches ~30-40% of issues):
- WAVE: wave.webaim.org — browser extension or web tool
- axe DevTools: browser extension (Deque)
- Google Lighthouse: built into Chrome DevTools

Manual Testing:
- Tab through every page with keyboard only
- Use with screen reader:
  - NVDA + Firefox (Windows — free)
  - VoiceOver + Safari (Mac/iOS — built-in)
  - JAWS + Chrome (Windows — most common AT for enterprise)

Color Contrast Testing:
- WebAIM Contrast Checker: webaim.org/resources/contrastchecker
- Colour Contrast Analyser (desktop app — free from TPGi)
```

---

### ADA Risk for Care Agencies

Care agencies that serve individuals with disabilities face heightened
scrutiny for website accessibility. Consider:

- Regional centers may check your website before finalizing vendor agreements
- Individuals with visual impairments are in your service population
- The Department of Justice has issued guidance that websites must comply with ADA
- California's Unruh Civil Rights Act provides additional protections

**Minimum actions before launch:**
1. Run WAVE tool on every public page — fix all errors
2. Ensure all forms are keyboard navigable
3. Ensure all images have alt text
4. Publish Accessibility Statement
5. Provide accessible contact method (phone alternative to form)

---

*These notes are for planning purposes. Have an attorney review the Terms of Use before publishing. Have an accessibility professional review the site before publishing the Accessibility Statement.*
