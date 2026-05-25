# CS Job Search Skills Toolkit

A collection of structured AI skill files for Customer Success professionals navigating a job search. Built for use with Claude (Anthropic), these skills turn Claude into a personalized career assistant that knows your background, voice, target roles, and differentiators.

## What This Is

These are Markdown instruction files — called "skills" — that you upload to a Claude Project. Once uploaded, Claude references them automatically in every conversation, so you're not starting from scratch each time you need help with a resume, cover letter, interview prep, or job description analysis.

**The result:** Most job search tasks that used to take hours take minutes.

## Who This Is For

Customer Success professionals at the Senior CSM or Manager/Director level who are:

- Actively job searching or preparing to search
- Targeting Enterprise SaaS, Cybersecurity, Cloud Infrastructure, or adjacent industries
- Willing to invest 3-5 hours upfront to build a system that pays dividends throughout the search

## What's Included

### `/skills` — The Core System

Eight interconnected skill files that form the foundation of your Claude-powered job search assistant. Build these in order — each one depends on the ones before it.

| File | Purpose | Build Order |
|---|---|---|
| `PROFILE_SKILL.md` | Your career identity, metrics, target roles, and narrative themes | 1st |
| `HUMANIZER_SKILL.md` | Your writing voice — makes all outputs sound like you, not AI | 2nd |
| `RESUME_SKILL.md` | Your complete resume content and tailoring rules | 3rd |
| `INTERVIEW_PREP_SKILL.md` | SAR story bank and coaching for behavioral interviews | 4th |
| `ACCOUNT_TURNAROUND_SKILL.md` | At-risk account recovery methodology | 5th |
| `AI_DIFFERENTIATOR_SKILL.md` | How to position AI work for different audiences | 6th |
| `JOB_TARGETING_SKILL.md` | JD analysis framework — fit score, gaps, ATS keywords | 7th |
| `HANDOFF_SKILL.md` | Context management — how to end sessions cleanly and start fresh without losing critical state | 8th |

### `/templates` — Ready-to-Use Formats

- `Cover_Letter_Template_Sr_CSM.md` — Cover letter template for IC Sr. CSM roles

### `/guide` — How to Use This System

See the `/guide` folder for setup instructions and day-to-day usage patterns.

## How to Use These Files

### Step 1 — Customize PROFILE_SKILL first

Every `[PLACEHOLDER]` in PROFILE_SKILL needs to be replaced with your actual information. This is the most important file in the system — everything else references it.

### Step 2 — Review HUMANIZER_SKILL

Adjust the voice fingerprint, banned phrases, and writing mechanics to match how *you* actually communicate. Remove anything that doesn't fit.

### Step 3 — Build your RESUME_SKILL

Replace all placeholder content with your actual career history, metrics, and bullet points.

### Step 4 — Upload to a Claude Project

In Claude.ai, create a Project, upload all your customized skill files, and add the Project Instructions (see `/guide` for the exact system prompt to use).

### Step 5 — Start using it

Paste a job description and say "analyze this JD." Ask for a tailored resume. Run mock interview prep. The system handles the rest.

### Step 6 — Use HANDOFF_SKILL to manage long sessions

When a conversation gets long or you're switching tasks, generate a handoff document to start a fresh conversation without losing context. Say "generate a handoff document" and Claude will produce one ready to paste into your next chat.

## `/portfolio-site` — Single-File Portfolio Template

A fork-friendly HTML template for showcasing your AI-powered CS workflows. Deploy to Cloudflare Pages in minutes — no build process, no backend required.

**What it includes:**

- Hero section with 4 key stats and tool overview
- 3-column deep-dive on your featured AI workflow (before/strategy/after layout)
- 3 additional tools with impact metrics and flow diagrams
- Organizational adoption proof (testimonials, distribution, recognition)
- Email obfuscation for privacy
- Fully responsive design

**Get started:** See `portfolio-site/README.md` for setup and customization. See `portfolio-site/CUSTOMIZE.md` for line-by-line guidance on every placeholder.

**Live example:** [joshualyons.com](https://joshualyons.com)

## Forking and Customizing

Fork this repo to your own GitHub account. All files use `[PLACEHOLDER]` syntax for anything personal — replace placeholders with your own information. Your customized version never affects this original.

## Project Instructions (System Prompt)

Copy this into your Claude Project's Instructions field:

```
You are my CS career assistant. At the start of every conversation, load PROFILE_SKILL as your primary source of truth about me. Apply HUMANIZER_SKILL to all written outputs so everything sounds like me, not like AI. Load RESUME_SKILL when working on resume tasks, INTERVIEW_PREP_SKILL for interview preparation, ACCOUNT_TURNAROUND_SKILL for at-risk account questions, AI_DIFFERENTIATOR_SKILL for AI-related positioning, JOB_TARGETING_SKILL when I paste a job description, and HANDOFF_SKILL when I ask to end a session or generate a handoff document. Never use generic CS language — my voice is specific, metric-driven, and earned.

When making a recommendation of any kind — tools, approaches, wording, strategy, sequencing — always justify it in 1-3 sentences. Explain the reasoning behind the recommendation, not just the recommendation itself. This applies to all outputs in this project.
```

## License

See LICENSE.md for full terms. Personal and internal business use permitted. Commercial resale or repackaging prohibited without authorization.

---

*Built by a CS professional, for CS professionals. Contributions and improvements welcome.*
