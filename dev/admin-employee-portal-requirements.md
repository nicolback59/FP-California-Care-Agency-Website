# Admin & Employee Portal Requirements
## California Care Agency — Private Portal Architecture

**Version:** 1.0
**Date:** 2026-06-13
**Platform:** WordPress + ProfilePress + Members plugin

---

## Architecture Overview

```
WordPress User Roles
        │
        ├── Administrator (built-in WP)
        │       └── Full WP Admin + /admin-portal/
        │
        ├── Manager (custom role)
        │       └── /employee-portal/ + limited admin features
        │
        ├── Employee (custom role — default for new registrations)
        │       └── /employee-portal/ only
        │
        └── Subscriber (built-in WP)
                └── No portal access (pending approval state)
```

---

## Login System

### Recommendation: Admin-Created Accounts + Optional Self-Registration with Approval

**Why:**
- Care agencies handle sensitive HR data
- Self-registration with mandatory admin approval provides security without full admin overhead
- Prevents unauthorized access to employee-only resources
- Allows future employees to submit intent to register before onboarding

### Login URLs

| Page | URL | Visibility |
|------|-----|------------|
| Login | `/login/` | Public (not indexed by Google) |
| Register | `/register/` | Public (not indexed by Google) |
| Forgot Password | `/forgot-password/` | Public |
| Employee Portal | `/employee-portal/` | Private — Login Required |
| Admin Portal | `/admin-portal/` | Private — Admin/Manager Only |

### Registration Flow

```
Option A — Admin-Created (Recommended for initial launch):
1. Admin creates user account in WP Admin or /admin-portal/
2. System sends welcome email with login credentials
3. Employee logs in, changes password on first login
4. Employee accesses portal immediately

Option B — Self-Registration with Approval (Phase 2 addition):
1. Employee visits /register/
2. Fills out registration form (name, email, position, start date)
3. Submits form → Account in "Pending" status
4. Admin receives email notification
5. Admin reviews and approves/denies in /admin-portal/
6. If approved: Employee receives email with login link
7. Employee sets password and accesses portal
```

### Password Policy

```
Minimum length: 12 characters
Requirements:
  - At least 1 uppercase letter
  - At least 1 number
  - At least 1 special character
Expiry: None (optional: require change every 90 days)
Reset method: Email link to registered email
Brute force protection: 3 attempts then lockout
```

---

## Employee Portal

### URL: `/employee-portal/`

### Access: Role = Employee, Manager, or Administrator

### Portal Navigation (left sidebar or top nav within portal)

```
Dashboard          /employee-portal/
Onboarding         /employee-portal/onboarding/
Handbook           /employee-portal/handbook/
Training           /employee-portal/training/
Forms & Downloads  /employee-portal/forms/
Announcements      /employee-portal/announcements/
HR Resources       /employee-portal/hr/
Policies           /employee-portal/policies/
My Account         /employee-portal/account/
Logout             [Logout link]
```

### Dashboard Page

```
Welcome message: "Welcome back, [First Name]."

Quick Access Cards:
┌──────────────────┬──────────────────┬──────────────────┐
│  📋 Onboarding   │  📖 Handbook     │  🎓 Training     │
│  Checklist       │                  │  Resources       │
├──────────────────┼──────────────────┼──────────────────┤
│  📄 Forms &      │  📢 Latest       │  🔒 HR           │
│  Downloads       │  Updates         │  Resources       │
└──────────────────┴──────────────────┴──────────────────┘

Recent Announcements:
[3 most recent announcements displayed — link to full list]
```

### Onboarding Section

```
Page: /employee-portal/onboarding/

Content:
- Welcome message from leadership (CONTENT NEEDED)
- Onboarding checklist (progressive — mark items complete)
- Required documents to submit (list with upload instructions)
- First week overview
- Who to contact with questions

Checklist items (CONTENT NEEDED — examples):
□ Complete I-9 (Employment Eligibility)
□ Complete W-4 (Tax Withholding)
□ Complete direct deposit form
□ Submit copy of driver's license
□ Submit proof of auto insurance
□ Submit CPR/First Aid certificate
□ Complete Mandatory Reporter training
□ Review and sign Employee Handbook
□ Complete HIPAA training
□ Complete first day orientation
□ Meet your supervisor
```

### Employee Handbook Section

```
Page: /employee-portal/handbook/

Format: Either PDF download or paginated WordPress pages
Suggested sections:
1. Welcome & Agency Mission
2. Employment Policies
3. Code of Conduct
4. DSP Standards of Practice
5. Client Rights and Dignity
6. Incident Reporting Procedures
7. Time and Attendance
8. Compensation and Benefits
9. Leave Policies
10. Performance Review Process
11. Grievance Procedures
12. Safety Policies
13. HIPAA and Confidentiality
14. Technology Use Policy
15. Social Media Policy
16. At-Will Employment Statement

Acknowledgment: Button or form to record that employee has read and agreed
Implementation: Use WP Document Revisions or PDF with version tracking
```

### Training Resources Section

```
Page: /employee-portal/training/

Content:
- Required training courses (list with status: Required/Complete/Overdue)
- Online training links (external platforms: Relias, DirectCourse, etc.)
- In-house training materials
- Video library (Phase 2 — hosted on Vimeo or YouTube unlisted)
- Training calendar
- Certificates on file (documentation)
```

### Forms & Downloads Section

```
Page: /employee-portal/forms/

Category tabs:
- HR Forms (W-4, direct deposit, PTO request, etc.)
- Operational Forms (incident reports, mileage logs, expense reports)
- Client-Related Forms (notes templates, schedule forms — NON-HIPAA only)
- Onboarding Documents

Implementation: WP Document Revisions
Each document shows:
- Document name
- Last updated date
- Version number
- [Download] button
```

### Announcements Section

```
Page: /employee-portal/announcements/

Display:
- Pinned/urgent announcements at top (highlighted)
- Chronological list of all announcements
- Filter by: All | Important | My Department

Each announcement shows:
- Title
- Date posted
- Content
- Priority badge (Normal / Important / Urgent)

Implementation: Announcements custom post type (restricted to portal users)
```

### HR Resources Section

```
Page: /employee-portal/hr/

Content:
- Benefits overview (CONTENT NEEDED)
- Health insurance enrollment information
- PTO balance request process
- Payroll schedule
- Payroll contact information
- HR contact information
- Workers comp information
- Emergency contacts and procedures

Note: Sensitive HR data (pay stubs, SSN, detailed personal info) should
NEVER be stored in WordPress. Use Gusto, ADP, or other HR software instead.
```

### Policies Section

```
Page: /employee-portal/policies/

Policy Documents:
- Employee Code of Conduct
- Client Rights Policy
- Incident Reporting Policy
- Confidentiality and HIPAA Policy
- Technology and Social Media Policy
- Vehicle and Transportation Policy
- Background Check Policy
- Drug-Free Workplace Policy
- Anti-Harassment Policy
- Progressive Discipline Policy

Format: PDF downloads via WP Document Revisions
Version tracking: Each policy shows effective date and version
```

---

## Admin Portal

### URL: `/admin-portal/`

### Access: Role = Administrator only (or Manager for limited features)

### Admin Portal Navigation

```
Dashboard            /admin-portal/
Employee Accounts    /admin-portal/accounts/
Content Manager      /admin-portal/content/
Documents            /admin-portal/documents/
Announcements        /admin-portal/announcements/
Pending Approvals    /admin-portal/approvals/
Reports              /admin-portal/reports/
```

### Dashboard

```
Summary widgets:
- Total active employees: [count]
- Pending account approvals: [count] [Review Now →]
- Published announcements: [count]
- Documents uploaded this month: [count]
- Last backup: [date]
```

### Employee Account Management

```
Page: /admin-portal/accounts/

Admin can:
✅ Create new employee accounts
✅ Edit employee accounts (name, email, role, status)
✅ Deactivate/delete accounts
✅ Reset passwords
✅ Assign/change user roles
✅ View employee last login date
✅ Review and approve pending registrations
✅ Bulk update employee status

Implementation:
- ProfilePress user management dashboard
- Or: Direct access to WP Admin > Users (for Administrators)
```

### Document Management

```
Page: /admin-portal/documents/

Admin can:
✅ Upload new documents
✅ Set document category
✅ Set visibility (All / Manager / Admin only)
✅ Update existing documents (version tracking)
✅ Archive/remove documents
✅ See download statistics (how many times downloaded)

Implementation: WP Document Revisions
```

### Announcement Management

```
Page: /admin-portal/announcements/

Admin can:
✅ Create announcements
✅ Set priority (Normal / Important / Urgent)
✅ Set target audience
✅ Pin announcements
✅ Set expiry date
✅ Archive/delete past announcements

Implementation: Custom announcements CPT (admin-only editing)
```

---

## Security Requirements for Portals

```
Portal pages must:
✅ Require active WordPress session to view
✅ Redirect unauthenticated visitors to /login/
✅ Use role-based access control (Members plugin)
✅ Be excluded from XML sitemap
✅ Have X-Robots-Tag: noindex, nofollow HTTP header
✅ Not be accessible via search engines (robots.txt: Disallow)
✅ Not display any content on failed auth (redirect only)
✅ Log all login attempts (Wordfence)
✅ Rate-limit login attempts
✅ Force HTTPS

Portal files (documents) must:
✅ Be stored in protected upload directory
✅ Not be accessible by direct URL without authentication
✅ Use WordPress file serve (via PHP, not direct server path)
✅ Never be indexed by search engines
```

### .htaccess Protection for Upload Directory

```apache
# Add to /wp-content/uploads/employee-docs/.htaccess
# (or use a protected directory outside webroot)
Options -Indexes
<FilesMatch "\.(?:pdf|doc|docx|xls|xlsx)$">
  Order allow,deny
  Deny from all
</FilesMatch>
```

**Note:** Serving files through WordPress PHP (via WP Document Revisions) is more secure than .htaccess alone — use both approaches.

---

## Email Notifications

Configure the following automated email notifications:

| Trigger | Recipients | Email Content |
|---------|-----------|---------------|
| New employee registration | Admin | "New portal registration pending approval: [Name]" |
| Account approved | Employee | "Your portal account has been approved. Login here." |
| Account denied | Employee | "Your registration requires additional information..." |
| Password reset requested | Employee | "Click here to reset your password." |
| New announcement posted (Urgent) | All employees | Announcement summary + login link |
| New document uploaded | All employees (optional) | "New document available: [Title]" |

All emails sent via WP Mail SMTP (configured with agency SMTP/Google Workspace).

---

## Implementation Notes for Developer

1. Install ProfilePress first, create custom roles before building portal pages
2. Install Members plugin, configure content restriction for all portal pages
3. Build Employee Portal pages in Elementor with role restriction on each page
4. Build Admin Portal pages — note: most admin functions use WP Admin, not custom pages
5. Configure ProfilePress login/registration forms and style with Elementor
6. Install WP Document Revisions and configure upload categories
7. Test all roles: subscriber → employee → manager → admin
8. Test the full registration and approval workflow end-to-end
9. Verify all portal URLs return 302 redirect (not 403/404) for unauthenticated users
10. Test all document downloads for each role

---

*Document updated as portal architecture evolves. Developer confirms implementation against this spec.*
