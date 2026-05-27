# HANDOFF SKILL
## Instructions for Claude: This skill governs how to end a conversation cleanly and prepare the user to start a fresh one without losing critical context. Apply this skill whenever the user signals a conversation is getting long, a task is wrapping up, or they're about to switch topics.

---

## WHY THIS SKILL EXISTS

Claude performs best early in a conversation — when the context window is relatively empty and attention isn't diffuse. As a conversation grows, response quality gradually degrades. This is called the **dumb zone**. The smart zone is roughly the first 100-120K tokens of a conversation.

The fix isn't to keep compressing and extending the same conversation indefinitely. It's to **hand off** — end the current conversation cleanly, capture what matters in a structured document, and start the next conversation fresh with only what's needed.

This skill defines:
- When to trigger a handoff
- What a handoff document must contain
- The exact template to use
- How to start a fresh conversation from a handoff document

---

## PROACTIVE CONTEXT WARNING

**At approximately 80K tokens, Claude must proactively flag the approaching limit — do not wait for quality to degrade.**

When the conversation approaches 80K tokens, Claude inserts this note at the top of its next response:

> ⚠️ **Heads up:** We're approaching the context limit where response quality starts to decline. Recommend wrapping up the current task and generating a handoff document before starting anything new.

After flagging, Claude continues with the current task normally. It does not stop mid-task. The warning is informational — the user decides when to wrap.

---

## WHEN TO TRIGGER A HANDOFF

Watch for these signals — any one of them is enough:

**Proactive trigger:**
- Conversation reaches ~80K tokens (Claude flags this automatically — see above)

**Explicit signals from the user:**
- "Let's do a handoff"
- "Generate a handoff document"
- "I'm going to start a new chat"
- "Let's wrap up"
- "I'll continue this later"
- "Let's pause here"
- "I'm stopping for now"

**Topic shift signal:**
- The conversation shifts to a task that requires its own focused context — meaning a new deliverable, a new company/role, or a new skill being built — rather than a continuation of the current task

**Task completion signals:**
- Resume tailored and approved → ready to move to cover letter or interview prep
- Interview prep complete for a specific company → ready to move to next company
- A major deliverable is complete and the next task is unrelated

---

## THE HANDOFF SEQUENCE — REQUIRED STEPS

When any trigger fires, Claude follows this sequence in order:

1. **Draft safety check** — Before generating the handoff doc, ask: "Were any drafts written this session that exist only in chat and haven't been saved as a file?" If yes, save them to `/mnt/user-data/outputs/` before proceeding.
2. **Ask for next session focus** — "What will the next session focus on?" The answer determines what context to include.
3. **Update ACTIVE_TASKS.md** — Reflect any task status changes, new files created, and completed items from this session. Use `recent_chats` to pull URLs for any conversations referenced.
4. **Generate the handoff document** — Using the template below, output in a code block ready to copy/paste.

---

## THE HANDOFF DOCUMENT — WHAT TO CAPTURE

A good handoff document is **concise and purposeful** — not a transcript or a dump of everything that happened. It contains only what the next conversation needs to hit the ground running.

### Required sections:

**1. PURPOSE OF NEXT SESSION**
What is the next conversation for? One sentence. This determines what context to include and what to leave out.

**2. SUGGESTED FIRST TASK**
One line: what should the next session start with? Removes the re-prioritization burden at the start of every new conversation.

**3. PIPELINE STATUS**
Current state of active leads or projects — name, stage, last action, next action. This is the most time-sensitive context.

**4. DECISIONS MADE THIS SESSION**
Specific decisions, approvals, or conclusions reached. Not a log of everything discussed — only things that affect future work.

**5. FILES / ARTIFACTS CREATED OR CHANGED**
Pointers to what was built or modified. File names and locations, not content. Keep it short.

**6. OPEN ITEMS**
Things that were identified but not completed. Tasks that need to happen in a future session.

**7. PARKING LOT — DEFERRED IDEAS**
Ideas or tasks that surfaced but were intentionally set aside for a future session. Each parking lot item MUST include three layers:
- **What** — the idea or task
- **Why** — the reasoning and context that produced it; what problem it solves, what was evaluated, what was decided and why
- **Where we left off** — specific enough that a new conversation can pick it up mid-stride without re-establishing context

> ⚠️ **Critical rule:** A parking lot item with only the decision and no context is not a handoff — it's a note. The next conversation will spend the first 10 minutes reconstructing the reasoning instead of doing work. Always include the why.

**8. CONTEXT FOR NEXT SESSION**
Any specific background the next conversation needs that isn't already in the project skills. Keep this lean — the skills files handle the standing context.

> **Context depth rule:** Simple task continuations need minimal context — just a pointer to where we stopped. Complex decisions, new ideas, or multi-session projects need full context: what was discussed, what was evaluated, what was decided, and why. Match context depth to complexity of the next task.

---

## HANDOFF DOCUMENT TEMPLATE

```
# HANDOFF DOCUMENT — [DATE]
## Generated at end of session. Paste at top of next conversation.
## Source conversation: [URL — pulled automatically via recent_chats at start of next session]

---

## PURPOSE OF NEXT SESSION
[One sentence: what will the next conversation focus on?]

## SUGGESTED FIRST TASK
[One line: what should the next session start with?]

---

## PIPELINE — CURRENT STATE

| Item | Role/Type | Stage | Last Action | Next Action |
|---|---|---|---|---|
| [Item] | [type] | [stage] | [last action] | [next action] |

---

## DECISIONS MADE THIS SESSION
- [Decision 1]
- [Decision 2]

---

## FILES / ARTIFACTS CREATED OR CHANGED
- [filename] — [what it is / what changed]

---

## OPEN ITEMS (carry to next session)
- [ ] [Task 1]
- [ ] [Task 2]

---

## PARKING LOT — DEFERRED IDEAS
[Each item must include all three layers: What / Why / Where we left off.
A parking lot item with only the decision and no context is not a handoff — it's a note.]

### [Idea or task name]
**What:** [The idea or task]
**Why:** [The reasoning and context — what problem it solves, what was evaluated, what was decided and why]
**Where we left off:** [Specific enough to pick up mid-stride in a new conversation without re-establishing context]

---

## CONTEXT FOR NEXT SESSION
[Only include if there's something the next conversation needs that isn't already in the project skills.
Simple continuations: minimal context — just a pointer to where we stopped.
Complex decisions or new projects: full context — what was discussed, evaluated, decided, and why.
Leave blank if not needed.]

---
*Skills active in this project: [list your active skills here]*
```

---

## HOW TO START A FRESH CONVERSATION FROM A HANDOFF DOCUMENT

1. Open a new conversation in the Claude project
2. Paste the handoff document at the top
3. Add one line below it stating what you want to work on:
   > "Continuing from handoff. Today I want to: [specific task]."

That's it. The project skills load automatically. The handoff document provides the session-specific context. Claude starts fresh and smart.

**What NOT to do:**
- Don't paste the entire previous conversation
- Don't summarize everything that happened in long paragraphs
- Don't include file contents in the handoff — use pointers (file names) instead
- Don't skip the handoff when switching topics — an informal start in a new chat means lost context

---

## GENERATING A HANDOFF DOCUMENT

When the user asks for a handoff document, Claude should:

1. Run the draft safety check — save any chat-only drafts to outputs first
2. Ask: "What will the next session focus on?" — the purpose determines what context to include
3. Pull current pipeline/project status from memory and recent conversation
4. Identify the suggested first task for next session
5. List only decisions that affect future work — not a recap of the whole session
6. List files/artifacts by name only — no content duplication
7. List open items that were identified but not completed
8. **For every parking lot item:** include all three layers — What, Why, and Where we left off. A parking lot item without context is a note, not a handoff. The next conversation should be able to pick it up mid-stride without asking "what was this about?"
9. **Match context depth to task complexity** — simple continuations need a pointer; complex decisions and new projects need full reasoning captured
10. Update ACTIVE_TASKS.md to reflect session changes; use recent_chats to populate any missing conversation URLs
11. Output the completed template, ready to copy/paste

**Format:** Output the handoff document in a code block so it's easy to copy cleanly.

---

## DESIGN PRINCIPLES (from Matt Pocock's handoff methodology)

- **Pointers, not content** — reference files by name; never duplicate content already captured elsewhere
- **Purpose-driven** — tailor what you include to what the next session will actually do
- **Disposable** — handoff documents are working tools, not permanent records
- **Clean break** — the value of a handoff is the fresh start; don't undermine it by carrying unnecessary context
- **One direction** — a handoff ends the current session; it doesn't try to extend it

---

## WHAT HANDOFF IS NOT

- **Not /compact** — compact summarizes and continues in the same session (building up layers of sediment). Handoff ends the session cleanly and starts a new one fresh.
- **Not a transcript** — don't capture everything that was said; capture only what the next session needs
- **Not a permanent document** — handoff documents are temporary; the project skills are the permanent context

---

*Last updated: May 2026*
*Depends on: PROFILE_SKILL, ACTIVE_TASKS*
*Used for: session transitions, context management, starting fresh conversations without losing critical state*
*Built by Joshua J. Lyons | linkedin.com/in/joshualyons | May 2026*
