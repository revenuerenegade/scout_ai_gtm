# Claude.ai Project Setup

This folder is the bridge between your Claude Code repo and the Claude.ai Project your sales team uses daily.

---

## Two-Layer System

| Layer | Who uses it | Interface | What it does |
|-------|-------------|-----------|-------------|
| **Claude Code (this repo)** | GTM ops / admin | Terminal | Setup, weekly sync, context maintenance |
| **Claude.ai Project** | All sales reps | Claude.ai web | Research, prospect scoring, sales messaging |

The `context/` files in this repo are the source of truth. Ops keeps them current via the sync skill. The Claude.ai Project serves them to reps automatically through Project knowledge.

---

## When to Use This Folder

- **Initial setup:** The `skills/setup/SKILL.md` guides you through the full deployment inline — you shouldn't need to open this folder. But if you're rebuilding the Project from scratch, these files are your reference.
- **Updating the Project:** After the weekly sync runs and tells you which files changed, re-upload only those files. This folder's `instructions.md` and `skills.md` are templates — they were already deployed by setup and rarely need updating.

---

## One-Time Setup (if doing it manually)

### 1. Create the Project
Go to [claude.ai](https://claude.ai) → Projects → New Project.
Suggested name: `Scout`

### 2. Upload Context Files
Go to Project settings → Knowledge → upload these 6 files from this repo:

- `context/profile.md`
- `context/icp-definition.md`
- `context/signal-library.md`
- `context/positioning.md`
- `context/competitor-radar.md`
- `context/personas/[your persona files]`

### 3. Paste Project Instructions
Go to Project settings → Instructions → paste the contents of `claude-project/instructions.md`.

Before pasting, fill in:
- `[Company]` → your company name
- `[Voice and tone]` → 2–3 sentences from `context/positioning.md` describing your voice

### 4. Share Skills with Reps
Copy the contents of `claude-project/skills.md` and share it where your team lives — a Slack channel, a Notion page, a pinned message. Reps don't need repo access. They just need these three prompts.

---

## Keeping It Current

Run `Read skills/sync/SKILL.md and run the weekly sync` each Monday.

After the sync runs, it outputs a **Claude.ai Project Update** block that tells you exactly which context files changed. Re-upload only those files:

1. Open the `Scout` Project in Claude.ai
2. Go to Project settings → Knowledge
3. Find each changed file and replace it with the updated version from this repo

Reps get the updated context on their next message. No rep action needed.

---

## What Stays in Claude Code (Never Upload)

These files are for ops only — don't upload them to the Claude.ai Project:

- `skills/` — SKILL.md files are ops tools, not rep tools
- `outputs/` — research briefs and play results live here, not in the Project
- `CLAUDE.md` — this is Claude Code's session context, not the Project's instructions
- Any files with real prospect data, CRM exports, or call recordings
