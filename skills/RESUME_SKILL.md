# RESUME SKILL — [YOUR NAME]
## Instructions for Claude: Load PROFILE_SKILL and HUMANIZER_SKILL before using this skill.

---

## OVERVIEW

This skill governs how to tailor and produce your resume as a PDF. The golden .docx files are the authoritative source for formatting. Claude modifies the XML inside a copy of the golden .docx, then converts to PDF using LibreOffice.

**Two versions exist (if applicable):**
| Version | Use For | Most Recent Title |
|---|---|---|
| IC (Sr. CSM) | Individual contributor roles | [Your IC title — e.g., Sr. Customer Success Manager] |
| Management | Manager, Director, VP roles | [Your management title — e.g., Sr. Director, Customer Success] |

*If you're only targeting one track, you only need one version.*

**If role type is unclear from the JD title, ask before proceeding.**

---

## OUTPUT FORMAT

- **Default output: PDF only.** Never produce .docx unless explicitly requested.
- .docx is only for ATS submissions where the portal requires file upload.
- Name tailored files: `[YourName]_Resume_[IC/Dir_CS]_[Company].pdf`

---

## WORKFLOW — EVERY RESUME REQUEST

### Step 1: Confirm inputs
- Identify role type: IC or Management
- Confirm the correct golden .docx has been uploaded to the conversation
- If the .docx has NOT been uploaded, stop and ask before proceeding.

### Step 2: Determine tailoring needed
- Standard (no JD): use baseline content from this skill as-is.
- Tailored (JD provided): follow TAILORING RULES below. Show edits first, get approval, then generate.

### Step 3: Generate the PDF
```bash
cp /mnt/user-data/uploads/[YourResume].docx /home/claude/resume_work.docx
mkdir -p /home/claude/resume_extracted
cd /home/claude/resume_extracted
unzip -q /home/claude/resume_work.docx
python3 /home/claude/modify_resume.py
cd /home/claude/resume_extracted
zip -r -q /home/claude/resume_output.docx .
soffice --headless --convert-to pdf /home/claude/resume_output.docx --outdir /mnt/user-data/outputs/
```

### Step 4: Present for approval
- Use `present_files` to show the PDF.
- Do not finalize until confirmed correct.

---

## XML MODIFICATION RULES (CRITICAL)

When editing `word/document.xml`:

- **ONLY change text content** inside `<w:t>` tags.
- **NEVER add, remove, or modify** any formatting tags.
- **NEVER change** the `<w:numId>` values — these control bullet formatting.
- Use Python's `xml.etree.ElementTree` for all XML modifications. Never use string replacement on XML.
- Escape special characters properly: `&` → `&amp;`, `<` → `&lt;`, `>` → `&gt;`

---

## TAILORING RULES

When tailoring for a specific JD:

1. **Run JD analysis first** (per JOB_TARGETING_SKILL) — identify keyword gaps and priority emphasis.
2. **Show proposed edits** as old vs. new bullet text with one-line rationale each. Wait for approval before generating.
3. **Modify bullet text only** — mirror JD language where it improves fit. Never fabricate experience.
4. **Reorder bullets within a role** to surface the most JD-relevant bullet first.
5. **Modify the summary paragraph** to reflect JD priorities if warranted.
6. **Never add bullets that don't exist** in the baseline unless explicitly approved.
7. **Keep earliest company content stable** — tailor most recent roles first.

---

## BASELINE CONTENT — IC RESUME

**File:** `[YourName]_Resume_[IC version].docx`

### Summary
"[Paste your IC resume summary here. This is what Claude uses as the baseline — tailor from this.]"

*Bold phrases to emphasize: [list which phrases should be bold in your summary]*

### [Most Recent Company] — [Title] | [Dates] | [Location]
*[RIF/departure note if applicable]*

1. [Bullet 1 — paste exact text from your resume]
2. [Bullet 2]
3. [Bullet 3]
4. [Bullet 4]
5. [Bullet 5]

### [Previous Company] — [Title] | [Dates] | [Location]
*[Promotion note if applicable]*

1. [Bullet 1]
2. [Bullet 2]
3. [Bullet 3]
4. [Bullet 4]
5. [Bullet 5]
6. [Bullet 6]
7. [Bullet 7]

### [Earlier Company] — [Title] | [Dates] | [Location]

Main bullets:
1. [Bullet 1]
2. [Bullet 2]
3. [Bullet 3]
4. [Bullet 4]

Sub-role — [Sub-title] | [Dates] | [Location]
1. [Bullet 1]
2. [Bullet 2]

### Certifications
[Cert 1] • [Cert 2] • [Cert 3] • [Cert 4]

---

## BASELINE CONTENT — MANAGEMENT RESUME

**File:** `[YourName]_Resume_[Management version].docx`

### Summary
"[Paste your management resume summary here.]"

### [Most Recent Company] — [Title] | [Dates] | [Location]
*[RIF/departure note if applicable]*

1. [Bullet 1]
2. [Bullet 2]
3. [Bullet 3]
4. [Bullet 4]
5. [Bullet 5]

### [Previous Company] — [Title] | [Dates] | [Location]
*[Promotion note if applicable]*

1. [Bullet 1 — management-focused version]
2. [Bullet 2]
3. [Bullet 3]
4. [Bullet 4]
5. [Bullet 5]
6. [Bullet 6]
7. [Bullet 7]

### [Earlier Company] — [Title] | [Dates] | [Location]

Main bullets:
1. [Bullet 1]
2. [Bullet 2]

Sub-role — [Sub-title] | [Dates] | [Location]
1. [Bullet 1]
2. [Bullet 2]

### Certifications
[Cert 1] • [Cert 2] • [Cert 3] • [Cert 4]

---

## OPTIONAL BULLETS

These bullets are available for tailoring but are NOT in the baseline resumes. Only add with explicit approval.

**[Role/Company] — [Use case] (add as bullet #X):**
"[Optional bullet text]"
*Confirm this reflects actual experience before adding.*

---

## ATS VERSION

When an ATS version is explicitly requested:
- Output format: .docx (not PDF)
- Remove all color formatting — everything becomes black
- Remove all bold formatting
- Remove all hyperlink wrappers (keep link text as plain text)
- Replace em dashes (—) with double hyphens (--)
- Name: `[YourName]_Resume_[IC/Dir_CS]_ATS.docx`

---

## BULLET QUALITY STANDARDS

Every tailored or new bullet must meet all five criteria:
1. **Quantified** — at least one number ($, %, #, or timeframe)
2. **Action-led** — strong opening verb; never "responsible for," "helped," "assisted"
3. **Specific** — names products, platforms, or methodologies
4. **Non-redundant** — no two bullets in the same role make the same point
5. **Earned** — defensible with a specific story in an interview

---

## WHAT NOT TO DO

- Do not generate resumes from scratch or from memory
- Do not use wkhtmltopdf or HTML/CSS for resume generation
- Do not modify any formatting XML — content text only
- Do not deliver .docx unless explicitly asked for or it's an ATS version
- Do not add bullets that don't exist in the baseline without approval
- Do not fabricate experience to match a JD

---

*Last updated: [Month Year]*
*Depends on: PROFILE_SKILL, HUMANIZER_SKILL*
*Golden files: [YourName]_Resume_IC.docx, [YourName]_Resume_Management.docx*
