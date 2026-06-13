# Employee Portal Planning
## Future-Proofing the Website Architecture

**Built for: WordPress + Elementor Pro + ACF | SiteGround Hosting**

---

## Overview

The admin and employee portal/dashboards are **developer scope** — this document gives the developer the full spec so they can build it correctly from the start.

---

## Portal Vision: Who It Serves

| User Type | Role in WordPress | What They Need |
|-----------|------------------|----------------|
| Administrator | `Administrator` role | Full WP admin access + agency dashboard |
| Manager / Lead | Custom `Manager` role | Employee content + limited admin |
| DSP / Caregiver | Custom `Employee` role | Portal dashboard only — no WP admin |
| New Hire | Custom `Employee` role | Onboarding checklist + handbook |

---

## URL Structure to Build

```
/employee-portal/              ← Public-facing login redirect
/employee-portal/login/        ← Login page (ProfilePress or WP native)
/employee-portal/dashboard/    ← Employee dashboard (post-login)
/employee-portal/onboarding/   ← Onboarding checklist
/employee-portal/training/     ← Training library
/employee-portal/forms/        ← Forms & downloads
/employee-portal/handbook/     ← Employee handbook
/employee-portal/announcements/ ← Announcements feed
```

**Admin dashboard:** Use native WordPress `/wp-admin/` — no need to rebuild this.

---

## Recommended Plugin Stack for Developer

| Need | Recommended Plugin | License |
|------|--------------------|--------|
| User login & registration | **ProfilePress** | Free/Paid |
| Role-based access control | **Members** (by MemberPress) | Free |
| Protected content | Role-gating via Members plugin | Free |
| Forms & file uploads | **WPForms** | Free/Paid |
| Document library | **WP Document Revisions** | Free |
| Onboarding steps | Custom Elementor page flow | No extra plugin |
| Announcements | WordPress native Posts + role-gate | No extra plugin |
| LMS (if needed later) | **Tutor LMS** (free tier) or **LearnDash** | Free/Paid |

**Recommended base stack:** ProfilePress + Members + WPForms. Lightweight, Elementor-compatible, SiteGround-friendly.

---

## Employee Dashboard (Post-Login)

```
Welcome, [First Name]

Quick Links:
→ My Onboarding Checklist
→ Training Resources
→ Submit a Form
→ Read the Handbook
→ View Announcements

Recent Announcements:
[Last 3 posts from Employee Announcements category]
```

**Implementation:** Elementor page, role-gated via Members. Dynamic name via ProfilePress shortcode.

---

## Onboarding Checklist

Step-based page flow — NOT a full LMS.

```
Step 1: Welcome to the Team         [Complete ✓]
Step 2: Your New Hire Paperwork     [Complete ✓]
Step 3: Watch Orientation Overview  [In Progress]
Step 4: Read the Employee Handbook  [Not Started]
Step 5: Complete Required Training  [Not Started]
Step 6: Meet Your Supervisor        [Not Started]
Step 7: You're Ready to Start!      [Not Started]
```

Each step = one Elementor page with content + WPForms "Mark Complete" submission + next step link.

**Checklist items:**
```
□ Read and sign Employee Handbook
□ Complete I-9, W-4, direct deposit
□ Review Emergency Procedures
□ Upload CPR/First Aid certificate
□ Sign Client Confidentiality Agreement
□ Watch Orientation Video
□ Schedule 1:1 with Supervisor
□ Complete required DSP training module
```

---

## Forms & Downloads

```
Timesheets & Payroll
• Weekly Timesheet (PDF)
• Mileage Log (PDF)
• Direct Deposit Change Form (PDF)

HR Forms
• PTO Request Form
• Incident Report Form
• Change of Availability Form

Training & Certification
• CPR Certificate Upload
• Training Completion Log
```

**Developer note:** Store in role-gated Media Library or WP Document Revisions. No PHI ever.

---

## Employee Handbook

Single protected page, anchor-linked table of contents:

```
1. Welcome Message
2. Mission & Values
3. Code of Conduct
4. Attendance & Scheduling
5. Compensation & Pay
6. Time Off & Leave
7. Training Requirements
8. Client Rights & Confidentiality
9. Incident Reporting
10. Technology & Social Media Policy
11. Discipline & Termination
12. Acknowledgment Form (link to WPForms form)
```

---

## Training Video Library

Embed YouTube unlisted or Vimeo private links in protected pages. Do NOT host video files on SiteGround.

```
Required Training (All Staff)
• DSP Orientation (Video, ~45 min)
• Client Rights & HIPAA (~20 min)
• Emergency & Safety Procedures (~30 min)
• Abuse & Neglect Reporting (~25 min)

Role-Specific
• SLS Support Techniques
• ILS Skill-Building Methods
• Community Integration Best Practices
• Crisis De-escalation
```

---

## Security Requirements

- [ ] All portal pages require WordPress login — no exceptions
- [ ] SSL certificate active (HTTPS enforced)
- [ ] Role-based access: employees cannot see admin content
- [ ] No PHI stored on the website — ever
- [ ] File uploads stored outside public webroot OR protected by .htaccess
- [ ] Strong password enforcement on all accounts
- [ ] Two-factor authentication for admin accounts
- [ ] Regular backups via SiteGround

---

## What NOT to Build in the Portal

| Feature | Use Instead |
|---------|-------------|
| Clinical records / PHI | Dedicated EHR (Therap, etc.) |
| Payroll processing | Gusto, ADP, or similar |
| Scheduling system | CareSmartz360, Therap, or similar |
| Time clock / clock-in | Dedicated time tracking app |
| Performance reviews | HR platform or Google Forms |

The portal is a **communications and resources hub** — not an HR system.
