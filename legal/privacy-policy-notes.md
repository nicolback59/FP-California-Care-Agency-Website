# Privacy Policy Notes
## California Care Agency Website

**Version:** 1.0 (Planning Notes — NOT a final Privacy Policy)
**Date:** 2026-06-13

> **IMPORTANT DISCLAIMER:**
> This document contains planning notes and a content framework only.
> It is NOT a legal document and should NOT be published as-is.
> The final Privacy Policy must be drafted or reviewed by a licensed attorney
> familiar with California law (CCPA/CPRA), HIPAA considerations, and
> applicable state regulations for care agencies.

---

## Why a Privacy Policy is Required

1. **Legal requirement** — California requires a privacy policy for any website that collects personal information from California residents (California Online Privacy Protection Act — CalOPPA)
2. **CCPA/CPRA compliance** — California Consumer Privacy Act applies to many businesses operating in California
3. **Trust signal** — Regional centers and families expect to see a privacy policy
4. **Form data** — Contact forms, referral forms, and registration forms collect personal data
5. **Analytics** — Google Analytics collects visitor data, requiring disclosure
6. **Employee portal** — Collecting personal information from employees requires disclosure

---

## Data Your Website Will Collect

### From Public Visitors (Forms)

| Data Type | Collection Point | Purpose |
|-----------|-----------------|---------|
| Full name | Contact form | Responding to inquiry |
| Email address | Contact/referral/apply forms | Communication |
| Phone number | Contact/referral forms | Communication |
| Message content | Contact form | Understanding inquiry |
| IP address | Automatic (server logs) | Security, analytics |
| Browser/device type | Automatic (analytics) | Analytics |
| Pages visited | GA4 tracking | Analytics |
| Geographic region (city level) | GA4 | Analytics |

### From Referral Sources (Service Coordinators)

| Data Type | Collection Point | Notes |
|-----------|-----------------|-------|
| SC name and contact info | Referral form | |
| Agency/organization name | Referral form | |
| Individual's first name only | Referral form | No full name, DOB, or identifying info in form |
| Services requested | Referral form | |

**NOTE:** Never collect full name + DOB + SSN + diagnosis + medical info in a public web form. These are HIPAA-sensitive. Collect only what is needed to initiate contact.

### From Job Applicants

| Data Type | Collection Point | Notes |
|-----------|-----------------|-------|
| Full name | Application form | |
| Email | Application form | |
| Phone | Application form | |
| Resume/cover letter | Application form | |
| Work history summary | Application form | |

**NOTE:** Do not collect SSN, driver's license number, or DOB in web forms. Collect these through secure onboarding process off the website.

### From Employees (Portal)

| Data Type | Collection Point | Notes |
|-----------|-----------------|-------|
| Name | Registration | |
| Email | Registration | |
| Password (hashed) | WordPress | Never stored in plain text |
| Login history | WordPress/Wordfence | Security |
| Documents downloaded | Portal | Audit trail |

---

## Required Privacy Policy Sections

The attorney-drafted policy should include at minimum:

1. **Introduction** — Who is collecting data, contact information
2. **What information we collect** — Explicit list
3. **How we collect it** — Forms, cookies, analytics
4. **Why we collect it (purpose)** — Communication, analytics, employment
5. **How we use it** — Not sold, not shared with third parties except service providers
6. **Who we share it with** — List any third parties (Google Analytics, email provider, etc.)
7. **Cookies and tracking** — What cookies are used, how to opt out
8. **California resident rights (CCPA/CPRA)** — Right to know, delete, opt-out
9. **HIPAA notice** — Clarify that the website is not a HIPAA-covered transaction but link to HIPAA Notice of Privacy Practices for services
10. **Children's privacy** — Not directed to individuals under 13
11. **Data security** — How you protect data
12. **Data retention** — How long you keep data
13. **Contact information** — Who to contact with privacy questions
14. **Changes to this policy** — How you notify users of updates
15. **Effective date** — Clear date

---

## CCPA/CPRA Key Requirements (California)

```
Under California law, California residents have the right to:
- Know what personal information is being collected
- Know whether personal information is sold or disclosed and to whom
- Say no to the sale of personal information
- Access their personal information
- Equal service and price, even if they exercise their privacy rights
- Correct inaccurate personal information
- Limit use and disclosure of sensitive personal information

For most small care agencies that do NOT sell data:
- Provide a clear privacy policy (required)
- Respond to "Do Not Sell My Personal Information" requests (required if selling data)
- Respond to data access/deletion requests within 45 days
- Do not discriminate against users who exercise their rights
```

---

## Google Analytics Disclosure

The site uses GA4 (Google Analytics 4). The privacy policy must disclose:

```
- We use Google Analytics to collect anonymized website usage data
- GA4 may set cookies on visitor devices
- Data is processed by Google in accordance with Google's privacy policy
- Visitors can opt out using the Google Analytics opt-out browser add-on
- We have enabled IP anonymization in GA4
```

**GA4 Setup for Privacy:**
- Enable IP anonymization (GA4 does this by default)
- Disable advertising personalization signals
- Set data retention to minimum (2 months)
- Update data sharing settings to limit sharing with Google

---

## Cookie Consent

The CookieYes plugin provides a cookie consent banner.

Configure categories:
```
Necessary cookies:     Always active (cannot opt out) — session, login cookies
Analytics cookies:     Opt-in required (GA4)
Marketing cookies:     Opt-in required (if any advertising pixels added)
Functional cookies:    Opt-in — enhanced features
```

---

## HIPAA Considerations for Care Agencies

**The website itself is NOT a HIPAA-covered transaction** if it only:
- Collects initial contact/inquiry information
- Does not store or transmit Protected Health Information (PHI)
- Does not process service authorizations or medical records

**However:**
- If referral forms collect diagnosis, treatment history, or medication information → HIPAA considerations apply
- Employee portal with clinical notes → HIPAA applies
- Any integration with EHR/health records → HIPAA applies

**Recommendation:**
- Keep referral forms to: name (first only), contact info, services needed, urgency
- Do NOT collect diagnosis, diagnosis codes, medications, treatment history, or full DOB in web forms
- Publish a separate HIPAA Notice of Privacy Practices (HIPAA NPP) linked from the privacy policy
- Consult HIPAA compliance officer before adding any clinical functionality to the site

---

## Attorney Notes Needed

Before finalizing the privacy policy, gather answers to these questions for the attorney:

```
□ Does the agency sell any personal information to third parties? (Answer: No, almost certainly)
□ Does the agency use any advertising pixels (Meta Pixel, Google Ads)? 
□ Does the agency have employees in other states?
□ What analytics tools are used? (GA4 confirmed)
□ What email marketing platform is used? (if any)
□ Does the site use a CRM that stores client/referral info?
□ What third-party plugins handle form data? (Fluent Forms)
□ What is the agency's official legal name?
□ Who is the privacy contact (name and email)?
□ What is the effective date?
□ Does the agency operate under any government contracts with additional privacy requirements?
```

---

## Privacy Policy URL

**Recommended:** `/privacy-policy/`

Link from:
- Footer (every page)
- All data-collection forms (checkbox: "I have read and agree to the Privacy Policy")
- Registration form
- Cookie consent banner

---

*This document is a planning reference only. Do not publish without attorney review.*
