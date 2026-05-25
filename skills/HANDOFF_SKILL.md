# HANDOFF SKILL — CS Job Search Assistant
## A context management skill for Claude-powered job search projects.
## Created by Joshua J. Lyons | linkedin.com/in/joshualyons | May 2026

---

## WHY THIS SKILL EXISTS

Claude performs best early in a conversation — when the context window is relatively empty and attention is focused. As a conversation grows longer, response quality gradually degrades. This is called the **dumb zone**. The smart zone is roughly the first 100-120K tokens of a conversation.

The fix isn't to keep extending the same conversation indefinitely. It's to **hand off** — end the current conversation cleanly, capture what matters in a structured document, and start the next conversation fresh with only what's needed.

This is especially important in a job search, where you're managing a live pipeline across multiple companies, generating multiple documents per application, and switching between very different tasks (resume tailoring, interview prep, cover letters, networking outreach) in the same Claude project.

This skill defines:
- When to trigger a handoff
- What a handoff document must contain
- The exact template to use
- How to start a fresh conversation from a handoff document

---

## WHEN TO TRIGGER A HANDOFF

Watch for these signals — any one of them is enough:

**Conversation signals:**
- The conversation has been going for a long time and covers multiple distinct topics
- You say "let's wrap up" or "I'll continue this later"
- A major task is complete and the next task is unrelated
- Responses are starting to feel less specific or sharp than they should be
- You're pasting a manual summary at the top of a new chat (this means the last handoff was informal — improve it)

**Task signals:**
- Resume tailored and approved → ready to move to cover letter or interview prep
- Interview prep complete for a specific company → ready to move to the next company
- Application submitted → ready to update your tracker and move to next application
- Networking outreach drafted → ready to move to a different pipeline task

**Explicit triggers:**
- "Let's do a handoff"
- "Generate a handoff document"
- "I'm going to start a new chat"

---

## THE HANDOFF DOCUMENT — WHAT TO CAPTURE

A good handoff document is **concise and purposeful** — not a transcript or a dump of everything that happened. It contains only what the next conversation needs to hit the ground running.

### Required sections:

**1. PURPOSE OF NEXT SESSION**
What is the next conversation for? One sentence. This determines what context to include and what to leave out.

**2. JOB SEARCH PIPELINE STATUS**
Current state of active leads — company, stage, last action, next action. This is the most time-sensitive context in any job search.

**3. DECISIONS MADE THIS SESSION**
Specific decisions, approvals, or conclusions reached. Not a log of everything discussed — only things that affect future work.

**4. FILES / ARTIFACTS CREATED OR CHANGED**
Pointers to what was built or modified. File names only — not content. Keep it short.

**5. OPEN ITEMS**
Things that were identified but not completed. Tasks to carry into a future session.

**6. CONTEXT FOR NEXT SESSION**
Any specific background the next conversation needs that isn't already in your project skills. Keep this lean — your skills files handle the standing context.

---

## HANDOFF DOCUMENT TEMPLATE

```
# HANDOFF DOCUMENT — [DATE]
## Generated at end of session. Paste at top of next conversation.

---

## PURPOSE OF NEXT SESSION
[One sentence: what will the next conversation focus on?]

---

## JOB SEARCH PIPELINE — CURRENT STATE

| Company | Role | Stage | Last Action | Next Action |
|---|---|---|---|---|
| [Company 1] | [Role] | [Stage] | [Last action] | [Next action] |
| [Company 2] | [Role] | [Stage] | [Last action] | [Next action] |
| [Company 3] | [Role] | [Stage] | [Last action] | [Next action] |

---

## DECISIONS MADE THIS SESSION
- [Decision 1]
- [Decision 2]
- [Decision 3]

---

## FILES / ARTIFACTS CREATED OR CHANGED
- [filename] — [what it is / what changed]
- [filename] — [what it is / what changed]

---

## OPEN ITEMS (carry to next session)
- [ ] [Task 1]
- [ ] [Task 2]
- [ ] [Task 3]

---

## CONTEXT FOR NEXT SESSION
[Only include if there's something the next conversation needs that isn't already in your project skills. Leave blank if not needed.]

---
*Active skills in this project: [list your skill files here]*
```

---

## HOW TO START A FRESH CONVERSATION FROM A HANDOFF DOCUMENT

1. Open a new conversation in your Claude project
2. Paste the handoff document at the top
3. Add one line below it stating what you want to work on:
   > "Continuing from handoff. Today I want to: [specific task]."

That's it. Your project skills load automatically. The handoff document provides the session-specific context. Claude starts fresh and smart.

**What NOT to do:**
- Don't paste the entire previous conversation
- Don't summarize everything that happened in long paragraphs
- Don't include file contents in the handoff — use pointers (file names) instead
- Don't skip the handoff when switching topics — an informal start costs you context quality

---

## HOW CLAUDE SHOULD GENERATE A HANDOFF DOCUMENT

When you ask for a handoff document, Claude should:

1. Ask: "What will the next session focus on?" — the purpose determines what context to include
2. Pull current pipeline status from recent conversation and memory
3. List only decisions that affect future work — not a full recap
4. List files/artifacts by name only — no content duplication
5. List open items that were identified but not completed
6. Output the completed template in a code block, ready to copy/paste

---

## DESIGN PRINCIPLES

These principles come from Matt Pocock's handoff methodology, adapted for job search use:

- **Pointers, not content** — reference files by name; never duplicate content already captured elsewhere
- **Purpose-driven** — tailor what you include to what the next session will actually do
- **Disposable** — handoff documents are working tools, not permanent records
- **Clean break** — the value of a handoff is the fresh start; don't undermine it by carrying unnecessary context
- **One direction** — a handoff ends the current session and starts a new one; it doesn't try to extend the current one

---

## WHAT HANDOFF IS NOT

- **Not /compact** — compact summarizes and continues in the same session. Handoff ends the session and starts a new one fresh.
- **Not a transcript** — don't capture everything said; capture only what the next session needs
- **Not a permanent document** — handoff documents are temporary working tools; your project skills are the permanent context

---

## CUSTOMIZATION NOTES

This template is built for CS job search workflows but the core pattern works for any Claude project where you're doing complex, multi-session work. To adapt it:

- Replace the pipeline table columns with whatever tracks your active work
- Update the "task signals" section to match your workflow milestones
- Add your active skill files to the footer of each handoff document
- Adjust the "context for next session" section to reflect what your skills don't already cover

---

## RELATED SKILLS IN THIS REPO

This skill works best alongside:
- `PROFILE_SKILL.md` — your professional background and target role criteria
- `HUMANIZER_SKILL.md` — your voice and writing standards
- `RESUME_SKILL.md` — resume tailoring and generation workflow
- `INTERVIEW_PREP_SKILL.md` — SAR stories and interview coaching
- `JOB_TARGETING_SKILL.md` — JD analysis and fit assessment

---

*Created by Joshua J. Lyons | linkedin.com/in/joshualyons | May 2026*
*Based on Matt Pocock's handoff methodology: aihero.dev/skills-handoff*
*Part of the CS Career Toolkit: github.com/joshualyons22/lyons-cs-jobsearch-skills*
