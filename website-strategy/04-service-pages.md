# Service Page Structures
## New California For-Profit Care Agency Website

**Built for: WordPress + Elementor Pro + ACF**

---

## Design Standard for All Service Pages

Every service page follows the same template structure:

1. **Hero** — Page title, brief description, CTA
2. **What It Is** — Plain-language explanation of the service
3. **Who It Serves** — Eligibility / ideal candidate description
4. **What Support Looks Like** — Day-in-the-life or bullet breakdown
5. **Our Approach** — Person-centered / differentiator messaging
6. **FAQ** — 4–6 questions specific to this service
7. **Related Services** — Internal link grid (cross-sell)
8. **CTA Section** — Intake inquiry or referral form

---

## SERVICE PAGE 1 — Supported Living Services (SLS)

**URL:** `/services/supported-living-services/`  
**Target Audience:** Families, individuals, service coordinators  
**SEO Keywords:** "Supported Living Services California," "SLS care agency California"

### Hero
```
Headline: Supported Living Services in California
Subheadline: Personalized, in-home support that helps individuals with
developmental disabilities live in their own homes — on their own terms.

CTA: [Request SLS Services]   [Talk to a Coordinator]
```

### What Are Supported Living Services?
```
SLS helps adults with developmental disabilities live in homes they choose —
with support tailored to their unique needs and goals, funded through DDS/regional centers.

Unlike group homes or facilities, SLS is provided in YOUR home.
```

### What SLS Support Can Include
```
Daily Living           Personal Care           Health & Safety
• Meal planning        • Medication support     • Emergency planning
• Household tasks      • Personal hygiene       • Medical appt support
• Grocery shopping     • Mobility assistance    • Provider communication

Financial              Community               Relationships
• Budgeting skills     • Transportation         • Social connections
• Bill management      • Community activities   • Family communication
• Benefits navigation  • Volunteering           • Advocacy support
```

### FAQ
```
Q: How do I access SLS?
A: Through your regional center. Ask your SC to add SLS to your IPP.

Q: Can I choose my own caregiver?
A: Yes. We match individuals with DSPs based on personality, interests, and schedule.

Q: Is SLS covered by regional center funding?
A: Yes. SLS is a vendored DDS service for eligible individuals with an active IPP.

Q: How is SLS different from a group home?
A: In SLS, you live in a home you choose — not a facility. Support comes to you.
```

### CTA
```
[Request SLS Services — Form]   or call (XXX) XXX-XXXX
```

---

## SERVICE PAGE 2 — Independent Living Services (ILS)

**URL:** `/services/independent-living-services/`  
**SEO Keywords:** "Independent Living Services California," "ILS regional center"

### Hero
```
Headline: Independent Living Services in California
Subheadline: Building the skills, confidence, and connections to live life on your own terms.
CTA: [Explore ILS]   [Get Connected]
```

### What ILS Covers
```
• Money management and budgeting    • Employment readiness
• Cooking and nutrition              • Health and self-care
• Home maintenance and safety        • Communication and social skills
• Using public transportation        • Technology use
• Community navigation               • Self-advocacy
```

### FAQ
```
Q: How is ILS different from SLS?
A: SLS provides ongoing support. ILS builds skills so individuals need less support over time.

Q: Is ILS covered by my regional center?
A: Yes. ILS is a vendored regional center service authorized through your IPP.
```

### CTA
```
[Inquiry Form]   |   (XXX) XXX-XXXX
```

---

## SERVICE PAGE 3 — Community Integration Services

**URL:** `/services/community-integration/`  
**SEO Keywords:** "Community Integration Services California," "community access developmental disabilities"

### Hero
```
Headline: Community Integration Services
Subheadline: Everyone deserves to belong. We help individuals connect,
participate, and thrive in their communities.
CTA: [Learn More]   [Talk to Us]
```

### What Community Integration Includes
```
• Community outings and social activities
• Volunteering and civic participation
• Employment exploration and work readiness
• Recreational programs and classes
• Peer connections and friendship building
• Transportation support to community activities
• Cultural, religious, and spiritual participation
• Shopping, dining, and leisure access
```

---

## SERVICE PAGE 4 — Person-Centered Planning

**URL:** `/services/person-centered-planning/`  
**SEO Keywords:** "Person-centered planning California," "individual program plan support"

### Hero
```
Headline: Person-Centered Planning
Subheadline: Every plan starts with the individual — their strengths, their goals, and their vision.
CTA: [Learn About Our Approach]
```

### How We Build Support Plans
```
Step 1: Listening session — with the individual, family, and/or SC
Step 2: Review of IPP/ISP goals and existing supports
Step 3: Draft support plan built around the individual
Step 4: Review and approval with team
Step 5: Caregiver/DSP matching
Step 6: Regular check-ins and plan adjustments
```

---

## SERVICE PAGE 5 — Respite & Crisis Support

**URL:** `/services/respite-crisis-support/`  
**SEO Keywords:** "Respite care developmental disabilities California"

### Hero
```
Headline: Respite & Crisis Support
Subheadline: When families need relief and individuals need fast support — we're here.
CTA: [Contact Us Now]   (XXX) XXX-XXXX — prominently displayed
```

### Crisis Support
```
When a support situation becomes unstable — a caregiver gap, a behavioral
crisis, a family emergency — we respond quickly and coordinate with
service coordinators and regional center staff to stabilize the situation.

Urgent situations: Call (XXX) XXX-XXXX
```

---

## ACF Field Groups for Service Pages (Developer Reference)

| Field Name | Type | Notes |
|------------|------|-------|
| `service_hero_headline` | Text | |
| `service_hero_subheadline` | Textarea | |
| `service_hero_image` | Image | |
| `service_primary_cta_label` | Text | |
| `service_primary_cta_url` | URL | |
| `service_secondary_cta_label` | Text | |
| `service_secondary_cta_url` | URL | |
| `service_intro_body` | WYSIWYG | "What is this service" section |
| `service_support_items` | Repeater | Label + description pairs |
| `service_faqs` | Repeater | Question + Answer pairs |
| `service_related_services` | Relationship | Links to other service pages |
| `service_inquiry_form_id` | Text | Elementor form ID for CTA form |
