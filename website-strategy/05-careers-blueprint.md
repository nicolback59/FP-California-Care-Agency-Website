# Careers & Recruitment Blueprint
## New California For-Profit Care Agency Website

**Built for: WordPress + Elementor Pro + ACF**

---

## Recruitment Strategy Overview

Caregiver and DSP recruitment is one of the most critical functions of any care agency. The website must work as an active recruiting tool.

**Website recruitment goals:**
1. Attract mission-aligned candidates who will stay
2. Answer compensation questions before they have to ask
3. Make the application process feel fast and human
4. Build confidence in the agency as a stable, caring employer

---

## Careers Section Architecture

```
/careers/
├── why-work-with-us/      ← Top of funnel, brand/culture page
├── benefits-and-pay/      ← Answers the #1 question
├── hiring-process/        ← Sets expectations, reduces drop-off
├── open-positions/        ← Dynamic job listings via ACF
└── apply-now/             ← Application form
```

---

## PAGE 1 — Why Work With Us

**URL:** `/careers/why-work-with-us/`

### Hero
```
Headline: More Than a Job. A Mission.
Subheadline: Join a team of compassionate caregivers making a real difference
in the lives of individuals with developmental disabilities across California.
CTA: [See Open Positions]   [Apply Now]
```

### Why Caregivers Choose Us

| Icon | Headline | Body |
|------|----------|------|
| 💰 | Competitive Pay | Honest, competitive wages with regular review. We share our pay ranges upfront. |
| 📅 | Flexible Scheduling | Part-time, full-time, and weekends available. We work around YOUR life. |
| 📚 | Paid Training | We invest in your professional development from day one. |
| 🤝 | Intentional Matching | We match you with individuals whose personalities and goals align with yours. |
| 📈 | Room to Grow | From DSP to Lead to Coordinator — we promote from within. |
| ❤️ | Mission-Driven Work | This is work that matters. You'll see the impact every single day. |

---

## PAGE 2 — Benefits & Pay

**URL:** `/careers/benefits-and-pay/`

### Compensation Section
```
Role                         | Starting Pay Range
Direct Support Professional  | $XX.XX – $XX.XX/hr
Lead DSP / Senior Caregiver  | $XX.XX – $XX.XX/hr
ILS Specialist               | $XX.XX – $XX.XX/hr
Office / Administrative      | Competitive — contact us
```

### Benefits
```
✅ Flexible Scheduling
✅ Mileage Reimbursement (IRS rate)
✅ Paid Orientation & Training
✅ Ongoing Professional Development
✅ Paid Sick Leave (California law)
✅ Career Advancement — promote from within
✅ Supportive Supervision
[Add any health/dental/vision if offered]
```

---

## PAGE 3 — Hiring Process

**URL:** `/careers/hiring-process/`

```
STEP 1 — Submit Your Application (10 minutes)
STEP 2 — Phone Screen (15–20 minutes)
STEP 3 — In-Person or Video Interview
STEP 4 — Background Check & References ([X–X] days)
STEP 5 — Offer & Paperwork (completed online)
STEP 6 — Paid Orientation & Training
STEP 7 — Your First Day (matched with client, supervised start)

Total timeline: approximately [X–X] weeks from application to first day.
```

### Requirements
```
• Valid California driver's license and reliable transportation
• Proof of auto insurance
• Ability to pass a background check (criminal and DMV)
• CPR/First Aid certification (or willingness to obtain)
• Genuine commitment to person-centered, respectful care

No prior DSP experience required for entry-level positions — we train.
```

---

## PAGE 4 — Open Positions

**URL:** `/careers/open-positions/`  
**ACF Implementation:** Custom Post Type `job_listing` with taxonomy `job_category`

### ACF Fields for Job Listings

| Field | Type | Notes |
|-------|------|-------|
| `job_title` | Text | |
| `job_type` | Select | Full-Time, Part-Time, Per Diem |
| `job_location` | Text | City or County |
| `job_pay_range` | Text | e.g., "$18–$21/hr" |
| `job_description` | WYSIWYG | Full job description |
| `job_requirements` | Textarea | Bullet list |
| `job_category` | Taxonomy | DSP, ILS, Admin, Lead, etc. |
| `job_posted_date` | Date | |
| `job_status` | Select | Active, Filled, Paused |

**Developer note:** Show only `job_status = Active`. When no openings, show general interest form.

---

## PAGE 5 — Apply Now

**URL:** `/careers/apply-now/`

### Form Fields

```
Section 1: About You
• First Name *  •  Last Name *  •  Email *  •  Phone *  •  City/County *

Section 2: Experience
• Position(s) interested in (checkboxes)
• Prior DSP/caregiver experience? (Yes / No / Currently working in care)
• If yes, brief description (textarea)
• CPR/First Aid certified? (Yes / No / Willing to get certified)

Section 3: Availability
• Available start date
• Desired hours (Full-Time / Part-Time / Either)
• Days available (Mon–Sun checkboxes)
• Shift preference (Morning / Afternoon / Evening / Overnight / Flexible)

Section 4: Additional
• Valid CA driver's license + reliable transportation? (Yes / No)
• How did you hear about us? (dropdown)
• Upload Resume (optional)
• Anything you'd like us to know? (textarea, optional)

[Submit Application →]
```

### Post-Submission Message
```
Thank you! Your application has been received.
A member of our team will contact you within [X] business days.
Questions? Call (XXX) XXX-XXXX
```

**Developer:** Send email notification to HR/admin on submission. Send auto-reply to applicant.

---

## DSP-Specific Messaging Principles

- **Lead with mission** — DSPs who stay are motivated by purpose, not just pay
- **Be honest about difficulty** — builds trust
- **Normalize inexperience** — many great DSPs came from unrelated fields
- **Show flexibility** — scheduling anxiety is a top drop-off reason
- **Use plain language** — avoid unexplained acronyms (ISP, IPP, RC, DDS)
- **Show real faces** — authentic photos outperform stock photography 10:1
