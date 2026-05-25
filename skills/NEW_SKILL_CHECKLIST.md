# NEW SKILL CHECKLIST
## Instructions for Claude: Run this checklist every time a new skill is created in this project. Do not skip steps. Present the checklist to the user and walk through each item in order.

---

## WHY THIS EXISTS

Creating a new skill touches multiple systems — the Claude project, the GitHub public repo, the README, and the project instructions. Without a checklist, things get missed. This skill ensures every new skill is fully deployed across all the right places.

---

## TRIGGER

Run this checklist when:
- A new .md skill file has just been created in this session
- The user says "we just built a new skill" or "let's finalize this skill"
- A session ends with a new skill file that hasn't been fully deployed

---

## THE CHECKLIST

Present this to the user after every new skill is created. Walk through each item and confirm completion before moving on.

---

### STEP 1 — Save the Skill File

- [ ] **Private version saved** — Is there a user-specific version of the skill (with real metrics, stories, and context)? If yes, confirm it has been downloaded or is available to upload to the Claude project.
- [ ] **Public version created** — Is a genericized version needed for the GitHub repo? If yes, confirm it has been created with all personal details replaced by `[PLACEHOLDER]` syntax and attribution added to the footer.

**Decision rule:** If the skill contains personal data (metrics, company names, job targets, stories), a separate public version is required. If the skill is purely structural/methodological (like HANDOFF_SKILL), a lightly edited version is sufficient.

---

### STEP 2 — Upload to Claude Project

- [ ] Go to the Claude Project → Files panel
- [ ] Upload the private version of the new skill file
- [ ] Confirm the file appears in the project files list
- [ ] If replacing an older version of the same skill, delete the old file first

---

### STEP 3 — Update Project Instructions

- [ ] Open Claude Project → Instructions
- [ ] Add the new skill to the `## OTHER SKILLS — LOAD AS NEEDED` list
- [ ] Format: `- [When to use it] → [SKILL_FILENAME.md]`
- [ ] Place it in logical order relative to the other skills (meta-skills first, task-specific skills below)
- [ ] Save the instructions

---

### STEP 4 — Upload Public Version to GitHub

- [ ] Go to your GitHub repo
- [ ] Determine the correct folder:
  - Skill files → `/skills/`
  - Cover letter or other templates → `/templates/`
  - Guides or process docs → `/guide/`
- [ ] Click **Add file → Upload files**
- [ ] Upload the public version of the skill
- [ ] Commit directly to main

---

### STEP 5 — Update the README

The README at the root of the repo contains a skills table that lists every file in `/skills/`. It needs to be updated whenever a new skill is added.

- [ ] Go to your README.md in GitHub
- [ ] Click the pencil icon to edit
- [ ] Find the skills table
- [ ] Add a new row for the new skill:

```
| `NEW_SKILL_FILENAME.md` | [One sentence: what it does] | [Build order number] |
```

- [ ] Update the Project Instructions system prompt block in the README if the new skill should be referenced there
- [ ] Commit directly to main

---

### STEP 6 — Update the HANDOFF_SKILL Footer

Every handoff document ends with a list of active skills. Update it to include the new skill.

- [ ] Open HANDOFF_SKILL.md in the Claude project
- [ ] Find the footer line: `*Skills active in this project: ...*`
- [ ] Add the new skill filename to the list
- [ ] Re-upload the updated HANDOFF_SKILL.md to the Claude project (delete old version first)

---

### STEP 7 — Update ACTIVE_TASKS.md

- [ ] Open ACTIVE_TASKS.md
- [ ] Add the new skill file to the Files Reference table
- [ ] Note the conversation URL where it was created (populate at start of next session via `recent_chats`)
- [ ] Re-upload the updated ACTIVE_TASKS.md to the Claude project (delete old version first)

---

### STEP 8 — Confirm End-to-End

Run a quick sanity check:

- [ ] New skill file is in Claude project files ✓
- [ ] Project instructions reference the new skill ✓
- [ ] Public version is in the GitHub repo in the correct folder ✓
- [ ] README skills table includes the new skill ✓
- [ ] HANDOFF_SKILL footer is updated ✓
- [ ] ACTIVE_TASKS.md Files Reference table is updated ✓

---

## WHEN CLAUDE SHOULD SURFACE THIS

At the end of any session where a new skill was created, Claude should say:

> "We created a new skill this session — [SKILL_NAME]. Want to run the New Skill Checklist to make sure it's fully deployed?"

Do not wait for the user to remember. Surface it proactively.

---

*Last updated: May 2026*
*Depends on: PROFILE_SKILL, ACTIVE_TASKS*
*Used for: skill deployment, project hygiene, GitHub repo maintenance*
*Built by Joshua J. Lyons | linkedin.com/in/joshualyons | May 2026*
