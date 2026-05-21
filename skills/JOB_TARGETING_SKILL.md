# JOB TARGETING SKILL — [YOUR NAME]
## Instructions for Claude: Load PROFILE_SKILL, RESUME_SKILL, and HUMANIZER_SKILL before using this skill. This skill governs how to analyze job descriptions, assess fit, identify gaps, and recommend resume tailoring for every role you apply to.

---

## HOW TO USE THIS SKILL

When you paste a job description, run the full analysis below in order. Do not skip sections. Present the output in the exact structure defined here so every analysis is scannable and consistent.

**Trigger phrases:** "analyze this JD," "how do I fit this role," "tailor my resume for this," "what do you think of this job," or any time a job posting is pasted.

---

## STEP 1: ROLE IDENTIFICATION

Before analysis, confirm:
- **Role type:** IC (Sr. CSM) or Management (Manager/Director/VP)? If unclear from the title, ask before proceeding.
- **Base resume to use:** IC roles → [Your IC resume filename]; Management roles → [Your management resume filename]
- **Company stage:** Early-stage / Growth / Mid-market / Enterprise / Public — infer from context, company size, funding, or JD language
- **Industry:** SaaS / Cybersecurity / Cloud Infrastructure / Digital Technology / AI / Other

---

## STEP 2: JD ANALYSIS

Extract and organize the following:

### Required Skills & Qualifications
List everything explicitly marked as required, must-have, or essential.

### Preferred Skills & Qualifications
List everything marked as preferred, nice-to-have, or desired.

### Implied Priorities
What is this role actually about based on the JD's language, emphasis, and framing? What problem are they hiring to solve? Look for:
- Which responsibilities appear first (highest priority)
- Which words repeat most frequently
- What the role is measured on
- What "success" looks like in their language

### ATS Keywords
Extract high-value ATS terms: product names, methodology names, platform names, metric names, and role-specific terminology. Flag any that are absent from the current resume.

---

## STEP 3: FIT ASSESSMENT

### Fit Score
Rate 1-100 with label:
- **Strong Fit** (80-100): Clear match on core requirements; apply with confidence
- **Good Fit** (65-79): Solid match with minor gaps; apply with targeted tailoring
- **Stretch** (50-64): Meaningful gaps exist; apply selectively with honest framing
- **Misaligned** (below 50): Significant mismatch; flag clearly and explain why

### Qualitative Summary
3-5 sentences. What makes you a strong candidate for this specific role? What's the most compelling part of your background relative to this JD?

### Gap Assessment (Three Tiers)

**Hard Gaps** — Requirements you clearly don't meet. Be direct. Don't soften these.

**Soft Gaps** — Areas where you have adjacent experience but not an exact match. Note how close the match is and how to frame it.

**Non-Issues** — Things that look like gaps on the surface but aren't, given your background. Explain why each one isn't a real concern.

### Cultural / Stage Fit Flag
Assess whether the company's stage, culture, or operating environment is a potential mismatch — even if the title and requirements align. Flag:
- Hyper-growth startup vs. enterprise experience
- Pure people-manager role vs. IC preference
- Heavily process-driven vs. builder mentality
- Geographic/work model mismatches

---

## STEP 4: KEYWORD GAP LIST

List ATS keywords from the JD that are missing or underrepresented in the current resume. Format as a simple list:

- [Keyword] — missing / underrepresented
- [Keyword] — missing / underrepresented

After presenting the list, ask: "Would you like me to map these into specific bullets, or do you have questions about any of them first?"

Do not add keywords to the resume until approved. Wait for confirmation before proceeding to Step 5.

---

## STEP 5: RESUME EDIT RECOMMENDATIONS

Present specific bullet edits as old vs. new, with a one-line rationale for each change. Format:

**[Role] — Bullet [#]**
- **Current:** [existing bullet text]
- **Recommended:** [revised bullet text]
- **Why:** [one sentence explaining the change]

Limit recommendations to changes that materially improve fit — don't edit for the sake of editing.

---

## STEP 6: POSITIONING ANGLE

One paragraph. How should you frame yourself specifically for this company and role? Cover:
- Which of your narrative themes to lead with
- What to emphasize vs. what to downplay relative to this specific role
- Any company-specific context that should shape how you talk about your background
- The one thing that makes you the most distinctive candidate for this specific role

---

## STEP 7: HONEST RECOMMENDATION

One clear sentence: Should you apply? If yes, with what version of the resume and what level of tailoring? If it's a stretch, say so directly and explain what would make it a stronger application.

---

## OUTPUT FORMAT

Every analysis follows this exact structure:

```
ROLE: [Title] — [Company]
TYPE: [IC / Management]
BASE RESUME: [which version]
STAGE: [company stage]
FIT SCORE: [score] — [label]

QUALITATIVE SUMMARY
[3-5 sentences]

HARD GAPS
[list or "None identified"]

SOFT GAPS
[list]

NON-ISSUES
[list]

CULTURAL / STAGE FIT
[assessment]

ATS KEYWORD GAPS
[list — awaiting review before mapping]

RESUME EDIT RECOMMENDATIONS
[old vs. new with rationale]

POSITIONING ANGLE
[one paragraph]

RECOMMENDATION
[one sentence]
```

---

## CALIBRATION NOTES

### Your Strongest Proof Points
*[List your 8-10 most compelling, quantified proof points — the metrics and achievements you can deploy against almost any CSM role requirement. Update these as your search progresses.]*

- [Retention metric — e.g., 100% logo retention across X Enterprise accounts]
- [ARR protection metric — e.g., $XM ARR protected across X high-risk account saves]
- [Growth metric — e.g., X% expansion revenue growth over X quarters]
- [Pipeline contribution — e.g., $XK net-new ARR from personal relationships]
- [Builder proof point — e.g., Built CS function from scratch at [Company]]
- [Retention streak — e.g., 100% retention for X consecutive years at [Company]]
- [AI/innovation — e.g., Built AI-powered tools adopted across CS and Sales at [Company]]
- [Long-game relationship — e.g., Grew $XK engagement to $XK ARR over X years]
- [Certifications — list relevant ones]

### Your Target Role Criteria
*[Define your criteria so Claude can flag mismatches automatically]*

- Title: [Target titles]
- Segment: [Enterprise/Mid-Market/SMB preference]
- Industries: [Your target industries]
- Work model: [Remote/hybrid preference and geographic constraints]
- Compensation: [Base range | Bonus range]

### Red Flags to Surface Immediately
*[List the deal-breakers that should trigger an automatic flag in the analysis]*

- Requires relocation
- Hybrid outside acceptable commute range
- Comp ceiling below your minimum base
- Requires specific technical certifications you don't hold
- Segment mismatch (e.g., SMB-only if you're Enterprise-focused)
- Role type mismatch (e.g., requires people management for IC application)

---

*Last updated: [Month Year]*
*Depends on: PROFILE_SKILL, RESUME_SKILL, HUMANIZER_SKILL*
*Used for: JD analysis, resume tailoring, fit assessment, ATS optimization*
