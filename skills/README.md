# Skills

These are the core instruction files for your Claude-powered CS job search assistant. Each file is a structured Markdown document that tells Claude something specific about you or instructs Claude to behave in a particular way for a specific task.

## How Skills Work

Upload these files to your Claude Project's Files section. Claude reads all uploaded files at the start of every conversation — so it automatically knows your background, voice, resume content, and interview stories without you having to re-explain anything.

## Build Order

**Build these in order.** Each skill references the ones before it.

### 1. PROFILE_SKILL.md — Build First
The authoritative source of truth about you. Contains your career history, key metrics, target role criteria, compensation targets, core competencies, and signature narrative themes. If you only build one skill, build this one.

**Customization required:** Replace every `[PLACEHOLDER]` with your actual information. This file requires the most work — budget 60-90 minutes.

### 2. HUMANIZER_SKILL.md — Build Second
Governs how Claude writes on your behalf. Defines your voice fingerprint — how you sound, what phrases to avoid, what writing mechanics to follow. Without this, Claude's outputs sound like AI-generated content. With it, everything sounds like you.

**Customization required:** Review the banned phrase list and voice fingerprint. Adjust to match how you actually communicate.

### 3. RESUME_SKILL.md — Build Third
Contains your complete master resume content — every role, every bullet, every metric. Includes tailoring rules for different role types and ATS optimization guidance.

**Customization required:** Replace all placeholder career content with your actual history. Budget 45-60 minutes.

### 4. INTERVIEW_PREP_SKILL.md — Build Fourth
A bank of SAR (Situation, Action, Result) stories drawn from your actual experience, mapped to the interview questions you'll most commonly face. The richer your stories, the more useful this skill becomes.

**Customization required:** Replace the example SAR stories with your own. Budget 90-120 minutes.

### 5. ACCOUNT_TURNAROUND_SKILL.md — Build Fifth
Codifies your at-risk account recovery methodology. Useful for interview prep and as an actual working playbook in your next role. This skill is largely methodology — lighter customization needed.

**Customization required:** Light — adjust the philosophy and approach sections to match your actual methodology.

### 6. AI_DIFFERENTIATOR_SKILL.md — Build Sixth
Frames your AI experience for different audiences — technical hiring managers, non-technical VPs, skeptics. Only relevant if you've built or deployed AI tools in your CS work.

**Customization required:** Replace the example tools with your actual AI work. If you haven't built AI tools yet, skip this skill or adapt it to describe how you use AI in your workflow.

### 7. JOB_TARGETING_SKILL.md — Build Before Applying
Governs how Claude analyzes job descriptions. When you paste a JD, this skill produces a structured analysis: fit score, gap assessment, ATS keyword gaps, resume edit recommendations, and a positioning angle.

**Customization required:** Update the calibration notes section with your actual proof points and target criteria.

## Usage Examples

**Analyze a job description:**
> Paste the full JD text and say: "Analyze this JD"

**Tailor your resume:**
> "Show me the bullet edits needed for this role, then generate a tailored resume PDF"

**Interview prep:**
> "Help me prep for my interview at [Company] for the [Role] position"

**Cover letter:**
> "Write me a cover letter for this role using the IC template"

## Tips

- Start a new conversation for each distinct task
- Update your Profile Skill whenever something significant changes (new metrics, new target companies)
- The Interview Prep Skill gets better over time — add new stories after each real interview
