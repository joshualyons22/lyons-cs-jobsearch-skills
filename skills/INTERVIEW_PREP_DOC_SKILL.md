# INTERVIEW PREP DOC SKILL
## Joshua J. Lyons — CS Career Assistant

*This skill governs how interview prep documents are created. It defines structure, format, content decisions, and delivery every time. Load this skill alongside INTERVIEW_PREP_SKILL.md (story bank) and INTERVIEW_INTELLIGENCE.md (company intel) whenever building a prep doc.*

---

## WHY THIS EXISTS

The ServiceNow/Veza prep doc took significant iteration to get right — SAR format, bolded key phrases, scannable bullets, clickable TOC, FRAME FOR INTERVIEWER sections, appendix for evergreen stories, consistent typography. That's institutional knowledge. This skill codifies those decisions so every future prep doc starts from a known baseline without re-litigating format, structure, or content choices.

---

## TRIGGER

Load this skill when Joshua says any of the following:
- "Build me an interview prep doc for [Company]"
- "Create prep for [Interviewer Name]"
- "I have an interview with [Company / Person] — build the prep"
- "Customize the master doc for [interview]"

---

## TWO DOCUMENT TYPES

### Type 1 — Google Doc (default for new opportunities)
Used when: first prep doc for a new company, or when Joshua wants a shareable/editable version.

Delivery: Create via Google Drive HTML upload → Google Doc conversion. Joshua then opens and inserts linked TOC via Insert → Table of Contents → With blue links.

### Type 2 — .docx (for formal interview rounds)
Used when: Joshua is heading into a panel, loop, or multi-interviewer round and needs a polished, downloadable file.

Delivery: Follow INTERVIEW_PREP_SKILL.md Format Spec exactly. Use the docx skill workflow (unpack → modify document.xml → rezip → LibreOffice PDF). Deliver as PDF unless Joshua explicitly requests .docx.

**Default to Type 1 (Google Doc) unless Joshua specifies otherwise or the context clearly calls for .docx.**

---

## PRE-BUILD CHECKLIST

Before writing a single line of the doc, confirm all of the following:

- [ ] **Company and role confirmed** — exact company name, role title
- [ ] **Interviewer name and title confirmed** — if unknown, note it and proceed without
- [ ] **Interview date and time confirmed** — if unknown, note it
- [ ] **JD analysis completed** — has JOB_TARGETING_SKILL been run on this role? If not, do it first or flag it
- [ ] **INTERVIEW_INTELLIGENCE.md checked** — is there existing company intel? Pull it in
- [ ] **Story selection confirmed** — which 2–3 stories go in the curated section? (See story selection rules below)
- [ ] **Narrative angle confirmed** — builder, turnaround artist, or infosec/compliance? (See PROFILE_SKILL)

**Do not build until all confirmed items are locked. Present story selection and narrative angle to Joshua and wait for approval before building.**

---

## STANDARD OPENING STATEMENT

Joshua's standard opening for most interviews. Evergreen — use verbatim unless the narrative angle requires a different lead (see PROFILE_SKILL).

**Formatting rules:**
- Bold phrases as marked
- "turning them into referencable partners that grow" → bold AND blue (#1F4E78)
- Phrases marked `[expand live]` are intentional trailing prompts — Joshua fills these in from memory; do not complete them in the doc
- No italics anywhere in the opening

---

I've spent over 25 years focused on **complex customer accounts in cybersecurity** and cloud infrastructure — many that had been damaged, churned through multiple CSMs, or **were sitting at risk ahead of renewal**.

My track record is taking those accounts and **turning them into referencable partners that grow**.

At Cloudflare I had an Enterprise book of 20 customers at an ARR between $12–14M beginning to end.

**I protected about $4M in at-risk ARR across six accounts that were flagged when I picked them up, and grew my book 20% over five quarters.**

My first two decades in this business were primarily in Sales roles. I know from experience what AEs… *[expand live]*

I also want to mention my philosophy about the **2 types of customers** and how it relates to CSMs and AEs — I view **External customers** and **Internal customers** — **building this relationship**… *[expand live]*

Good CSMs treat the AE relationship as a partnership, not a handoff. I don't surface expansion signals and sit on them — I take them to the account team and we build the play together.

---

## DOCUMENT STRUCTURE

Every prep doc — Google Doc or .docx — follows this structure in this order:

1. **Document header / title block**
   - Company name + role
   - Interviewer name, title (if known)
   - Date and time (if known)

2. **Table of Contents**
   - Google Doc: placeholder text with instruction to insert via Google Docs UI
   - .docx: auto-generated via `TableOfContents` with `hyperlink: true`, Heading 1 and 2 levels only

3. **Interviewer Intel**
   - Background on the interviewer (LinkedIn, prior companies, public posts)
   - What their background signals about what they'll probe
   - What will land vs. what to avoid with this specific person

4. **Opening Statement**
   - Use the Standard Opening Statement above verbatim
   - Note any company-specific framing adjustments inline if the narrative angle requires it

5. **Curated Stories** (2–3 stories, selected for this interviewer)
   - Full SAR format — see story format rules below
   - USE FOR, S, A, R, KEY LINE, FRAME FOR INTERVIEWER sections

6. **Questions to Ask**
   - 4–5 pulled from the Question Bank in the master doc
   - Any company-specific questions added based on intel

7. **Landmines**
   - Pulled from INTERVIEW_PREP_SKILL.md landmine section
   - Only include landmines relevant to this company/interviewer
   - Add any new landmines specific to this opportunity

8. **Appendix — Full Story Bank**
   - All stories NOT in the curated section
   - Same full SAR format
   - Page break before appendix
   - Label: *"All remaining stories from the golden doc."*

---

## STORY SELECTION RULES

Select 2–3 stories for the curated section based on this priority order:

1. **Match to JD language** — which stories map directly to phrases in the JD? (e.g., "extreme ownership" → LNRS; "cross-functional orchestration" → Fanatics)
2. **Match to interviewer background** — what will resonate with this specific person? (e.g., Splunk background → LNRS renewal story; Sales leader → FBG expansion story)
3. **Cover different competency areas** — don't select two stories that prove the same thing
4. **Always include AI Differentiator** if the JD or company signals interest in innovation, efficiency, or AI adoption

**Primary story bank (from INTERVIEW_PREP_SKILL.md):**
- LNRS — Risk & Executive Confidence (renewal, crisis management, executive relationships)
- Fanatics Collectibles — Cross-Functional Orchestration (internal influence, hard deadlines, engineering escalation)
- Carrier — Multi-CSM Account Save (at-risk accounts, trust rebuilding, retention)
- Convergys (Bad News) — Delivering Difficult News (expectation management, empathy, agency)
- Infolock — Building from Scratch (builder narrative, process improvement, founding CSM)
- FBG — CS/Sales Partnership (expansion, proactive data, Sales alignment)
- Convergys (Long-Game) — 12-Year Relationship (trust, retention philosophy, compliance background)
- Carrier/SSL.com — Influencing Without Authority (PM relationship, internal roadblocks)
- AI Differentiator — Innovation story (tools built, adoption, GCS AI Task Force)

---

## STORY FORMAT STANDARD

Every story — curated or appendix — uses this exact structure:

```
[STORY TITLE] — [COMPANY/CONTEXT]

USE FOR
• "[Question type 1]"
• "[Question type 2]"
• "[Question type 3]"

S — SITUATION
• [Bullet 1 — setup, context, stakes]
• [Bullet 2 — what made it hard or high-stakes]
• [Bullet 3 — the moment everything was at risk, if applicable]

A — ACTION
• [Bullet 1 — first move, with bolded key phrase]
• [Bullet 2 — key decision or escalation, with bolded key phrase]
• [Bullet 3 — how you managed both internal and external simultaneously]
• [Bullet 4 — what you did proactively before being asked]

R — RESULT
• [Quantified outcome — ARR, %, retention, timeline]
• [Relationship or trust outcome]
• [Any downstream or secondary impact]

KEY LINE
"[The one sentence that lands the whole story. Deliver this slowly.]"

FRAME FOR INTERVIEWER
[2–3 sentences of general guidance on how this story lands, what type of interviewer
it resonates with, which part to emphasize, what not to skip. Bold the key phrases
the interviewer should notice.]
```

**Formatting rules inside stories:**
- Bullets are 1–2 sentences max — scannable, not prose
- **Bold key phrases** that should land when spoken — these are the words to slow down on
- S — SITUATION: 2–3 bullets max; stakes and problem only; no padding
- A — ACTION: carries the story; this section is longest
- R — RESULT: always quantified where possible
- KEY LINE: italicized; delivered as a standalone statement, not buried in a bullet
- FRAME FOR INTERVIEWER: general guidance, not person-specific; bold the key phrases

---

## HEADING HIERARCHY

### Google Doc
| Element | Heading Level | Notes |
|---|---|---|
| Section headers (Interviewer Intel, Opening, Stories, Questions, Landmines, Appendix) | H1 | Generates top-level TOC entries |
| Story titles | H2 | Generates second-level TOC entries |
| USE FOR / S / A / R / KEY LINE / FRAME FOR INTERVIEWER | H3 | Third-level TOC entries |
| Body content | Normal | Bullets, prose |

### .docx
Follows INTERVIEW_PREP_SKILL.md Format Spec exactly:
- H1 → 13pt bold blue (#1F4E78) with bottom border
- H2 (story titles) → 20pt bold blue
- S/A/R labels → 10pt bold + underline (NOT H3 — plain paragraph)
- Body → 12pt Calibri
- USE FOR / KEY LINE / notes → 9pt italic

---

## INTERVIEWER INTEL SECTION

Always include. Pull from:
1. **INTERVIEW_INTELLIGENCE.md** — check first; intel may already be captured
2. **LinkedIn** — current role, prior companies, tenure, posts, shared connections
3. **Web search** — public talks, articles, conference appearances

Structure the intel section as:
- **Background** — 3–5 bullets on their career history and current role
- **What their background signals** — what will they probe? What do they care about?
- **What will land** — which of your stories/narratives resonates with their background
- **What to watch for** — any potential friction points or areas to handle carefully

If interviewer is unknown: note it, leave the section as a placeholder, and proceed with the rest of the doc.

---

## QUESTION SELECTION RULES

Pull 4–5 questions from the Question Bank in the master Google Doc. Selection criteria:

- **Match to company stage** — Series B/C startup: ask about playbook maturity, team size, what's being built. Enterprise/public: ask about CS motion, renewal ownership, exec engagement
- **Match to interviewer role** — CS Director/VP: ask about team structure, success definition, onboarding. Recruiter: ask about role scope, team, timeline. Peer CSM: ask about day-to-day, tech stack, culture
- **Always include** "What would make someone in this role clearly successful at 12 months — beyond the metrics?"
- **Always include for Hiring Managers and Senior CS Leaders** — "How do CSMs currently work with customers to verify outcomes and quantify ROI — is there a formal method/playbook in place, or is that a gap that needs to be developed?"
- **Culture questions** — reserve for peer interviews and final rounds only. If the interviewer's round is unknown when building the doc, ask Joshua before including or excluding culture questions.
- **Add 1–2 company-specific questions** based on what's known about their CS motion, recent news, or product focus

---

## LANDMINE SELECTION RULES

Pull relevant landmines from INTERVIEW_PREP_SKILL.md. Include only those that apply to this company and interviewer. Always include:

- **Cloudflare RIF** — always; every interview
- **Compliance knowledge currency** — for infosec/compliance companies (SailPoint, Drata, Proofpoint)
- **Infolock scale** — for interviewers who may question enterprise credibility
- **Channel partner confusion** — for any role where the Cloudflare CS motion needs clarification

Add new landmines if the JD or company context surfaces new risk areas.

---

## CONTENT THAT STAYS IN THE MASTER DOC (NOT IN EVERY PREP DOC)

The following live in the master Google Doc and are pulled from it — they are NOT rebuilt from scratch each time:
- Full story bank (all 9 stories in SAR format)
- Complete question bank (all 6 categories)
- Opening statement (evergreen)
- FRAME FOR INTERVIEWER sections (general guidance)

The prep doc contains:
- Company/interviewer-specific framing
- Curated story selection (2–3 from the bank)
- Selected questions (4–5 from the bank)
- Relevant landmines only
- Full story bank in appendix (copied from master)

---

## WHAT TO CONFIRM BEFORE BUILDING

Present this to Joshua and wait for explicit approval before building:

> "Here's what I'm planning for the [Company] prep doc:
>
> **Narrative angle:** [builder / turnaround artist / infosec-compliance]
> **Curated stories:** [Story 1], [Story 2], [Story 3]
> **Reason for each:** [1-line rationale per story]
> **Questions:** [Category 1], [Category 2], [Category 3] + [1 company-specific]
> **Landmines:** [List]
>
> Confirm and I'll build."

Do not build until Joshua says yes.

---

## DELIVERY

### Google Doc
1. Build full HTML content with proper H1/H2/H3 structure
2. Upload to Google Drive via `create_file` with `contentMimeType: text/html`
3. Title format: `[Company] — Interview Prep — [Interviewer First Name] [Date]`
   - Example: `Drata — Interview Prep — Recruiter Screen — May 28`
4. Share the file link with Joshua
5. Note: *"Open → Open with Google Docs → Insert → Table of Contents → With blue links"*

### .docx
1. Follow INTERVIEW_PREP_SKILL.md Format Spec
2. Use docx skill workflow: golden template → unpack → modify document.xml → rezip → LibreOffice PDF
3. Filename: `[Company]_InterviewPrep_[InterviewerLastName].docx`
4. Deliver as PDF unless Joshua asks for .docx

---

## MASTER DOCUMENT REFERENCE

**Golden master doc:** Interview Prep — Master Document (Google Drive)
- Contains: all 9 stories in full SAR format, complete question bank, opening statement, FRAME FOR INTERVIEWER sections
- This is the source of truth for evergreen content
- Every prep doc pulls from this; it is never rebuilt from scratch
- Update the master doc when: new stories are added, existing stories are revised, question bank is expanded

**When to update the master doc:**
- New story approved and finalized → add to master + to INTERVIEW_PREP_SKILL.md
- Question bank expanded → add to master
- FRAME FOR INTERVIEWER updated → update master
- Do NOT add company-specific content to the master doc

---

## SESSION WORKFLOW SUMMARY

1. Joshua says "build prep for [Company/Interviewer]"
2. Load this skill + INTERVIEW_PREP_SKILL.md + INTERVIEW_INTELLIGENCE.md
3. Run JOB_TARGETING_SKILL on the JD if not already done
4. Confirm pre-build checklist (company, interviewer, date, JD analysis, intel)
5. Select stories + narrative angle → present to Joshua → wait for approval
6. Build the doc (Google Doc default; .docx if specified)
7. Deliver with link or file + TOC instruction

---

*Last updated: June 2, 2026 — updated: standard opening statement added with bold/blue formatting rules (blue on "turning them into referencable partners that grow"); ROI/outcome verification question added for HMs/Sr CS Leaders; culture question reserved for peer/final rounds; interviewer role clarification prompt added*
*Depends on: PROFILE_SKILL, HUMANIZER_SKILL, INTERVIEW_PREP_SKILL, INTERVIEW_INTELLIGENCE*
*Used for: building Google Doc and .docx interview prep documents per-interview*
