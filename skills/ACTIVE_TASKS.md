# ACTIVE TASKS — [YOUR NAME]
## Living document. Update at the end of every session where a task, draft, or file was created or changed.
## Last updated: [DATE]

---

## HOW CLAUDE USES THIS FILE

**At the start of any conversation where this file is present:**
Claude reads ACTIVE_TASKS.md first, before responding to any request. Claude then runs `recent_chats` to pull any missing conversation URLs for the Files Reference table. Claude surfaces any URGENT items or items due today/tomorrow proactively — without being asked.

**At the end of every session (any explicit stop signal or topic shift):**
Claude updates this file to reflect:
- Any new tasks created or completed
- Any drafts written (named and located)
- Any files created (name and location)
- Any status changes on open items
- The date in the "Last updated" line at the top — this is a required field, not decorative
- Conversation URLs — pulled automatically via `recent_chats`; current conversation URL populated at start of next session

**The rule for drafts:** If a draft was written in chat and you might need it later, it gets saved as a file to `/mnt/user-data/outputs/` before the session ends — no exceptions. A draft that exists only in chat is lost when the conversation closes.

**Session end signals that trigger an update:**
- "Let's wrap up" / "I'll continue this later" / "Let's pause here" / "I'm stopping for now"
- Conversation reaches ~80K tokens (proactive warning fires)
- Topic shifts to a new deliverable, new company/role, or new skill being built

---

## URGENT / DUE SOON

| Task | Due | Status | Notes |
|------|-----|--------|-------|
| [Task name] | [Date] | 🔴 / 🟡 / ✅ | [Notes] |

---

## DRAFTS IN CHAT (not yet saved as files)

| Draft | Status | Action Needed |
|-------|--------|---------------|
| [Draft name] | 🔴 Not saved | Save as [filename] before closing session |

*This section is cleared once a draft is saved as a file to outputs.*

---

## OPEN TASKS — JOB SEARCH

| Task | Status | Priority | Notes |
|------|--------|----------|-------|
| [Task] | 🟡 Not started | High / Medium / Low | [Notes] |

---

## OPEN TASKS — PROJECT / TOOLS

| Task | Status | Priority | Notes |
|------|--------|----------|-------|
| [Task] | 🟡 Not started | High / Medium / Low | [Notes] |

---

## PARKING LOT (not active — revisit later)

| Idea / Task | Added | Notes |
|-------------|-------|-------|
| [Idea] | [Date] | [Notes] |

---

## COMPLETED THIS SESSION

| Task | Completed | Notes |
|------|-----------|-------|
| [Task] | [Date] | [Notes] |

---

## FILES REFERENCE

### Project Files (in Claude project — always loaded)
| File | What It Is | Last Conversation |
|------|-----------|------------------|
| PROFILE_SKILL.md | Source of truth about you | — |
| HUMANIZER_SKILL.md | Voice and writing rules | — |
| RESUME_SKILL.md | Resume content and tailoring workflow | — |
| INTERVIEW_PREP_SKILL.md | SAR story bank and interview frameworks | — |
| ACCOUNT_TURNAROUND_SKILL.md | At-risk account methodology | — |
| AI_DIFFERENTIATOR_SKILL.md | AI work positioning by audience | — |
| JOB_TARGETING_SKILL.md | JD analysis framework | — |
| HANDOFF_SKILL.md | Session handoff protocol | — |
| NEW_SKILL_CHECKLIST.md | Skill deployment checklist | — |
| ACTIVE_TASKS.md | This file | — |

### Golden Files (local — upload to conversation when needed)
| File | What It Is |
|------|-----------|
| [Resume_IC].docx | IC resume baseline — required for tailored PDF generation |
| [Resume_Mgmt].docx | Management resume baseline — required for tailored PDF generation |

### External / Live
| Asset | Location |
|-------|----------|
| Portfolio site | [your URL] |
| GitHub repo | [your repo URL] |
| Job Tracker | [your tracking tool URL] |

---

## JOB SEARCH PIPELINE (quick reference)

| Company | Stage | Next Action |
|---------|-------|-------------|
| [Company] | [Stage] | [Next action] |

---

## UPDATE LOG

| Date | Session Focus | What Changed |
|------|--------------|--------------|
| [Date] | [Topic] | [Changes made] |

---

*Depends on: PROFILE_SKILL, HANDOFF_SKILL*
*Updated by: Claude at end of every session with task/file changes*
*Template — replace all [PLACEHOLDER] values with your own information*
*Built by Joshua J. Lyons | linkedin.com/in/joshualyons | May 2026*
