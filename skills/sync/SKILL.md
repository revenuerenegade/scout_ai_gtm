# Skill: Sync

**Cadence:** Weekly (Monday morning recommended)
**Run by:** GTM ops / admin — in Claude Code, not Claude.ai

---

## Quick Start

```
Read skills/sync/SKILL.md and run the weekly sync.
```

Claude will read the current state of the repo, identify what's stale, draft every section that needs updating, ask you to fill in what it can't know, apply confirmed changes, and tell you exactly which files to re-upload to your Claude.ai Project.

---

## Purpose

Keep the repo accurate without making maintenance feel like a second job. This skill handles the diff — what changed since last week — rather than asking you to rewrite everything from scratch.

The output is a set of proposed edits, not final commits. You review, adjust, approve. Claude drafts; you decide.

After every sync, you'll get a **Claude.ai Project Update** section at the end — a specific list of which files changed and need to be re-uploaded so reps always have current context.

---

## What Claude Reads

Before producing any output, Claude reads:

1. `CLAUDE.md` — current priorities, active accounts, team focus
2. `context/signal-library.md` — signal performance log and last-updated date
3. `context/icp-definition.md` — ICP evolution log and last-updated date
4. `context/competitor-radar.md` — win/loss patterns and last-updated date
5. Any files in `outputs/dossier/` dated in the last 14 days

---

## Step 1: Staleness Check

Claude identifies which sections are out of date based on last-updated dates and play activity.

Flag any of the following:

| File / Section | Stale if... |
|---------------|-------------|
| `CLAUDE.md` → Current priorities | Not updated in the last 7 days |
| Signal performance log | Not updated in the last 14 days |
| Competitor radar | Last updated more than 60 days ago |
| ICP evolution log | Last updated more than 90 days ago |

Print a summary of what's stale before drafting anything.

---

## Step 2: Draft Updates

For each stale section, draft a proposed update in this format:

```
### [File] — [Section]
Last updated: [date]
Status: STALE — [reason]

CURRENT:
[existing content]

PROPOSED:
[drafted update based on what Claude can infer from the repo]

QUESTIONS FOR YOU:
- [anything Claude can't know — requires human input]
```

Work through each stale section in order of impact:

### 2a. CLAUDE.md — Current Priorities

Draft a new "Current priorities" block based on:
- Recent dossiers in `outputs/dossier/` (which accounts are in active re-engagement)
- What signals are active (from `context/signal-library.md`)
- What was in last week's priorities (carry forward anything still relevant)

Then ask:
- What changed this week that's not reflected in the repo?
- Any new accounts or segments becoming a focus?
- Any re-engagement efforts that landed a meeting or went cold?

### 2b. Signal Performance Log

Ask for any outreach results from the week:

```
What were the results on outreach this week?
Paste: Account | Sends | Replies | Meetings booked
```

Update the signal performance log with new data. Calculate reply and meeting rates.
Flag: if a signal has 30+ sends with no meetings booked, note it explicitly.

### 2c. Competitor Radar (if stale)

If `context/competitor-radar.md` hasn't been updated in 60+ days, ask:
- Any competitive deals won or lost since the last update?
- Any new objections you're hearing that aren't in the battlecard?

Do not draft a competitive update without input — competitive intel requires human knowledge.

### 2e. ICP Evolution Log (if stale)

If the evolution log hasn't been updated in 90+ days:
- Draft a log entry template pre-filled with today's date
- Ask: has anything changed about who you're targeting?

---

## Step 3: Confirm and Apply

Present all proposed changes in one response. For each:

- Show CURRENT vs. PROPOSED side by side
- Mark sections that need human input with `[NEEDS YOUR INPUT]`
- After confirmation, apply all approved changes to the relevant files

Do not apply changes until the user confirms. Do not invent performance data — if numbers aren't in the repo, ask for them.

Add a one-line entry to `outputs/weekly-log.md` (create it if it doesn't exist):

```
YYYY-MM-DD: Updated [list of files changed]. [One sentence on the most significant change.]
```

---

## Step 4: Claude.ai Project Update

After all changes are applied, output this block. It tells the admin exactly which files to re-upload to the Claude.ai Project so reps get the latest context.

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Claude.ai Project Update
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Re-upload these files to keep reps current:

[ ] context/[changed file]  ← [what changed]
[ ] context/[changed file]  ← [what changed]

No changes (skip):
[list of unchanged files]

How to re-upload:
1. Open the Scout Project in Claude.ai
2. Go to Project settings → Knowledge
3. Find each file above and replace it with the updated version from this repo

That's it — reps get updated context on their next message.
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

If no context files changed (only `outputs/` or `CLAUDE.md` were updated), output:

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Claude.ai Project Update
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
No context files changed this week. No re-upload needed.
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```
