# INTERVIEW PREP DOC SKILL
## CS Career Assistant — Public Template

*This skill governs how interview prep documents are created. It defines structure, format, content decisions, and delivery every time. Load this skill alongside your story bank skill and company intelligence file whenever building a prep doc.*

*CRITICAL: Read this skill file completely before building anything. Do not make assumptions. Do not skip steps.*

---

## WHY THIS EXISTS

Interview prep docs tend to get rebuilt from scratch every time — different formats, inconsistent structure, forgotten sections. This skill codifies a proven document structure so every future prep doc starts from a known baseline without re-litigating format, content choices, or what to include. The goal is one consistent, scannable document per interview that you can open 30 minutes before a call and be ready.

---

## TRIGGER

Load this skill when the user says any of the following:
- "Build me an interview prep doc for [Company]"
- "Create prep for [Interviewer Name]"
- "I have an interview with [Company / Person] — build the prep"
- "Customize the master doc for [interview]"

---

## DOCUMENT FORMAT — NON-NEGOTIABLE

**All interview prep documents are delivered as .docx files.** There is no Google Doc path. There is no HTML path.

- Build using docx-js, matching the full typography spec in your story bank skill
- Always request the golden master .docx from the user if it has not been uploaded to the conversation
- If the golden master .docx has not been uploaded, STOP and ask for it before proceeding
- Deliver as .docx + PDF unless the user explicitly says otherwise
- Filename format: `[Company]_InterviewPrep_[InterviewerLastName].docx`
  - Example: `Acme_InterviewPrep_RecruiterScreen_Jan15.docx`

---

## MANDATORY PRE-BUILD STEPS — IN ORDER

Do not skip any step. Do not build until all steps are complete.

### Step 1 — Ask clarifying questions
Before doing anything else, ask the user any questions needed to proceed. Use judgment — ask what's missing or ambiguous. Common gaps:
- Interviewer name and title (if not provided)
- Interview round (recruiter screen, hiring manager, peer, panel, final)
- Date and time
- Whether JD has been analyzed yet

### Step 2 — Pre-build checklist
Confirm all of the following before writing a single line:

- [ ] **Company and role confirmed** — exact company name, role title
- [ ] **Interviewer name and title confirmed** — if unknown, note it and flag it
- [ ] **Interview date and time confirmed** — if unknown, note it
- [ ] **Interview round confirmed** — determines question selection (culture questions: peer/final only)
- [ ] **Golden master .docx uploaded** — if not, STOP and ask the user to upload it
- [ ] **JD analysis completed** — has the JD targeting skill been run? If not, do it first or flag it
- [ ] **Company intelligence file checked** — is there existing company intel? Pull it in
- [ ] **Story selection confirmed** — which 2–3 stories go in the curated section?
- [ ] **Narrative angle confirmed** — what is the primary positioning angle for this company/role?

### Step 3 — Pre-build confirmation gate
Present the following to the user and wait for explicit approval before building:

> "Here's what I'm planning for the [Company] prep doc:
>
> **Narrative angle:** [primary positioning angle]
> **Curated stories:** [Story 1], [Story 2], [Story 3]
> **Reason for each:** [1-line rationale per story]
> **Questions:** [Category 1], [Category 2], [Category 3] + [1 company-specific]
> **Landmines:** [List]
>
> Confirm and I'll build."

**Do not build until the user says yes.**

---

## DOCUMENT STRUCTURE

Every prep doc follows this structure in this exact order:

1. **Document header / title block**
   - Company name + role
   - Interviewer name, title (if known)
   - Date and time (if known)

2. **Table of Contents**
   - Auto-generated via `TableOfContents` with `hyperlink: true`, Heading 1 and 2 levels only

3. **Company Summary** *(always include)*
   - Two versions of a 2–3 sentence summary of what the company does
   - Both are interview-ready and deliverable — not just reference material
   - **Version A — Standard:** Clean, credible, conversational. The default answer when asked "what does [Company] do?" in an interview. Key phrases bolded. Bullet format.
   - **Version B — Simple Analogy:** Simpler language, accessible analogy. Pull this out when you want to demonstrate the ability to take a complex topic and make it simple — signals intellectual range. Key phrases bolded. Bullet format.
   - Source: web search the company before building. Do not rely on memory.

4. **Interviewer Intel**
   - Background on the interviewer (LinkedIn, prior companies, public posts)
   - What their background signals about what they'll probe
   - What will land vs. what to avoid with this specific person

5. **Opening Statement**
   - [PLACEHOLDER: Insert your standard opening statement here]
   - Note any company-specific framing adjustments inline if the narrative angle requires it

6. **Curated Stories** (2–3 stories, selected for this interviewer)
   - Full SAR format — see story format rules below
   - USE FOR, S, A, R, KEY LINE, FRAME FOR INTERVIEWER sections

7. **Questions to Ask**
   - 4–5 pulled from the Question Bank in the master .docx
   - Any company-specific questions added based on intel

8. **Landmines**
   - Pulled from your story bank skill landmine section
   - Only include landmines relevant to this company/interviewer
   - Add any new landmines specific to this opportunity

9. **Appendix — Full Story Bank**
   - All stories NOT in the curated section
   - Same full SAR format
   - Page break before appendix
   - Label: *"All remaining stories from the golden doc."*

---

## STORY SELECTION RULES

Select 2–3 stories for the curated section based on this priority order:

1. **Match to JD language** — which stories map directly to phrases in the JD? (e.g., "cross-functional orchestration" → your orchestration story; "extreme ownership" → your crisis management story)
2. **Match to interviewer background** — what will resonate with this specific person?
3. **Cover different competency areas** — don't select two stories that prove the same thing
4. **Always include your differentiator story** if the JD or company signals interest in innovation, efficiency, or AI adoption

**Primary story bank categories (adapt to your own stories):**
- Risk & Executive Confidence (renewal, crisis management, executive relationships)
- Cross-Functional Orchestration (internal influence, hard deadlines, engineering escalation)
- At-Risk Account Save (churn prevention, trust rebuilding, retention)
- Delivering Difficult News (expectation management, empathy, agency)
- Building from Scratch (builder narrative, process improvement, founding role)
- CS/Sales Partnership (expansion, proactive data, Sales alignment)
- Long-Game Relationship (trust, retention philosophy, compliance background)
- Influencing Without Authority (PM relationship, internal roadblocks)
- Innovation/AI Differentiator (tools built, adoption, cross-team impact)

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

## HEADING HIERARCHY (.docx only)

- H1 → 13pt bold blue (#1F4E78) with bottom border
- H2 (story titles) → 20pt bold blue
- S/A/R labels → 10pt bold + underline (NOT H3 — plain paragraph)
- Body → 12pt Calibri
- USE FOR / KEY LINE / notes → 9pt italic

---

## INTERVIEWER INTEL SECTION

Always include. Pull from:
1. **Company intelligence file** — check first; intel may already be captured
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

Pull 4–5 questions from the Question Bank in the master .docx. Selection criteria:

- **Match to company stage** — Series B/C startup: ask about playbook maturity, team size, what's being built. Enterprise/public: ask about CS motion, renewal ownership, exec engagement
- **Match to interviewer role** — CS Director/VP: ask about team structure, success definition, onboarding. Recruiter: ask about role scope, team, timeline. Peer CSM: ask about day-to-day, tech stack, culture
- **Always include** "What would make someone in this role clearly successful at 12 months — beyond the metrics?"
- **Always include for Hiring Managers and Senior CS Leaders** — "How do CSMs currently work with customers to verify outcomes and quantify ROI — is there a formal method/playbook in place, or is that a gap that needs to be developed?"
- **Culture questions** — reserve for peer interviews and final rounds only. If the interviewer's round is unknown, ask before including or excluding culture questions.
- **Add 1–2 company-specific questions** based on what's known about their CS motion, recent news, or product focus

---

## LANDMINE SELECTION RULES

Pull relevant landmines from your story bank skill. Include only those that apply to this company and interviewer. Customize this list to your own situation:

- **[PLACEHOLDER: Your departure/gap explanation]** — always; every interview
- **[PLACEHOLDER: Any domain knowledge currency concern]** — for domain-specific companies
- **[PLACEHOLDER: Company/account size credibility]** — for interviewers who may question scale
- **[PLACEHOLDER: Any role/motion clarification needed]** — for any role where your CS motion needs framing

Add new landmines if the JD or company context surfaces new risk areas.

---

## MASTER DOCUMENT REFERENCE

**Golden master .docx:** [PLACEHOLDER: Your master document filename] — upload this to the conversation when requesting a prep doc.
- Contains: all stories in full SAR format, complete question bank, opening statement, FRAME FOR INTERVIEWER sections
- This is the source of truth for evergreen content
- Every prep doc is built FROM this file — unpack → modify → repack
- Never rebuilt from scratch
- If not uploaded, STOP and ask before proceeding

**When to update the master doc:**
- New story approved and finalized → add to master + to story bank skill
- Question bank expanded → add to master
- FRAME FOR INTERVIEWER updated → update master
- Do NOT add company-specific content to the master doc

---

## SESSION WORKFLOW SUMMARY

1. User says "build prep for [Company/Interviewer]"
2. Load this skill file completely — do not skip sections or make assumptions
3. Load your story bank skill + company intelligence file
4. Ask clarifying questions (Step 1 above)
5. Confirm golden master .docx is uploaded — if not, ask for it
6. Run JD targeting skill on the JD if not already done
7. Run pre-build checklist (Step 2 above)
8. Present pre-build confirmation to the user — wait for approval (Step 3 above)
9. Build the .docx using docx-js, matching full typography spec from the story bank skill
10. Deliver .docx + PDF

---

## CUSTOMIZATION NOTES FOR YOUR OWN USE

This skill is designed as a template. To adapt it to your job search:

1. Replace all `[PLACEHOLDER]` fields with your own content
2. Update the story bank categories to match your actual stories
3. Add your own opening statement in the Opening Statement section
4. Customize landmine categories to your specific background and gaps
5. Update the golden master .docx filename to your actual file
6. Adjust the heading/typography spec if your preferred format differs

The core workflow (pre-build checklist, confirmation gate, document structure, story format standard) is evergreen and should be kept as-is.

---

*Last updated: June 2026*
*Depends on: your profile skill, voice/humanizer skill, story bank skill, company intelligence file*
*Used for: building .docx interview prep documents per interview*
*Original author: Joshua J. Lyons — github.com/joshualyons22/lyons-cs-jobsearch-skills*
*License: See LICENSE.md — personal use permitted; commercial resale/repackaging prohibited*
