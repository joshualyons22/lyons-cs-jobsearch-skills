# Guide

This folder contains setup instructions and usage guidance for the CS Job Search Skills Toolkit.

For the full guide — including step-by-step setup, how to build each skill, and day-to-day usage patterns — see the PDF guide included in this repository.

## Quick Start

### 1. Set Up Your Claude Project

1. Go to [claude.ai](https://claude.ai) and sign in
2. Click **Projects** in the left sidebar → **New Project**
3. Name it something like "CS Job Search"
4. Upload all your customized skill files to the Project's Files section
5. Add the Project Instructions (system prompt) below

### 2. Project Instructions (System Prompt)

Copy this into your Claude Project's **Instructions** field. Customize the file names if you renamed any skills:

```
You are my CS career assistant. At the start of every conversation, load PROFILE_SKILL as your primary source of truth about me. Apply HUMANIZER_SKILL to all written outputs so everything sounds like me, not like AI. Load RESUME_SKILL when working on resume tasks, INTERVIEW_PREP_SKILL for interview preparation, ACCOUNT_TURNAROUND_SKILL for at-risk account questions, AI_DIFFERENTIATOR_SKILL for AI-related positioning, and JOB_TARGETING_SKILL when I paste a job description. Never use generic CS language — my voice is specific, metric-driven, and earned.
```

### 3. Test Your Setup

Once your skills are uploaded and the system prompt is set, open a new chat in your Project and try:

> "Summarize my professional background and tell me what my three strongest differentiators are."

If Claude gives you a specific, metric-driven, first-person summary that sounds like you — your setup is working.

---

## Day-to-Day Usage Patterns

### Analyze a Job Description
Paste the full JD text and say:
> "Analyze this JD"

You'll get: fit score, gap assessment (hard gaps, soft gaps, non-issues), ATS keyword gaps, and a positioning angle.

### Tailor Your Resume
After reviewing the JD analysis:
> "Show me the bullet edits needed for this role, then generate a tailored PDF"

Review the proposed edits and approve before Claude generates the file.

### Generate a Cover Letter
> "Write me a cover letter for this role using the IC template"

Claude will fill in the role-specific details using your skills as context.

### Interview Prep
> "Help me prep for my interview at [Company] for the [Role] position"

Claude will identify which stories to lead with, how to frame your background for this company, and can run mock questions if you want.

### Coach a Specific Answer
> "Here's how I answered this question: [paste your answer]. How do I make it stronger?"

---

## Maintenance Tips

- **Update PROFILE_SKILL** whenever something significant changes: new target companies, new metrics from interviews, comp target adjustments
- **Add to INTERVIEW_PREP_SKILL** after each real interview — what questions came up, how you answered, what landed
- **Delete and re-upload updated files** when you make changes — Claude reads whatever is currently uploaded, so stale files produce stale outputs
- **Start a new conversation** for each distinct task — long conversations can cause Claude to lose track of early instructions

---

## Troubleshooting

**Claude isn't using my skills**
- Make sure all files are uploaded to the Project's Files section (not just to a regular conversation)
- Check that your Project Instructions reference the correct file names
- Start a new conversation — the skills load fresh at the start of each chat

**Outputs sound generic**
- Your HUMANIZER_SKILL needs more of your specific voice. Add calibration examples from your own writing.
- Your PROFILE_SKILL may need more specific metrics and stories. Vague inputs produce generic outputs.

**Resume formatting is off**
- The resume skill requires your golden .docx template to be uploaded to the conversation
- Do not use HTML/CSS or any other method — the .docx → LibreOffice workflow is required

---

*For the complete guide with detailed explanations of each skill, see CS_Career_Toolkit_Guide.pdf in the root of this repository.*
