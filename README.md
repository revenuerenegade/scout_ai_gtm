# GTM Starter Kit

Built by [The Revenue Architects](https://www.the-revenue-architects.com) — a GTM engineering firm based in San Francisco. We work with growth-stage B2B SaaS companies to design and build their revenue systems.

This repo is the open-source version of what we build with clients. Clone it, run setup once, and your sales team has an AI-powered GTM assistant in Claude.ai — no rebuilding context every session.

---

## Two Layers

| Layer | Who uses it | Interface | What it does |
|-------|-------------|-----------|-------------|
| **Claude Code (this repo)** | GTM ops / admin | Terminal | Setup once, sync weekly, maintain context |
| **Claude.ai Project** | All sales reps | Claude.ai web | Research, prospect scoring, sales messaging |

Ops fills in the context once. Claude.ai serves it to reps automatically. When context changes, ops re-uploads the affected files. Reps get the update on their next message — no action needed on their end.

---

## For GTM Ops

### Step 1: Clone and open

```bash
git clone https://github.com/KarlRaf/gtm-starter-kit.git
cd gtm-starter-kit
claude .
```

### Step 2: Run setup (15–30 min)

```
Read skills/setup/SKILL.md and set up this repo for [your-domain.com]
```

Claude researches your company publicly — website, Crunchbase, LinkedIn, G2, job postings — and writes every context file from real data. When it's done, it offers a short refinement pass to sharpen anything inferred.

**Then setup walks you through deploying to Claude.ai inline** — it outputs the Project instructions, the file upload list, and the rep skills sheet, all in one message. About 10 minutes to go live.

### Step 3: Sync weekly (10 min)

```
Read skills/sync/SKILL.md and run the weekly sync.
```

Run this every Monday. Claude identifies stale sections, drafts updates, and asks you to confirm. After applying changes, it tells you exactly which files to re-upload to the Claude.ai Project.

---

## For Sales Reps

You don't need this repo. Open the **[Company] GTM Assistant** Project in Claude.ai and use these three prompts:

```
Research [company.com]
```
```
Score these accounts and tell me who to prioritize:
[paste company names or domains]
```
```
Write messaging for [persona title] at [company].
Signal: [what happened]
```

Ask your GTM ops team for the full prompt sheet — it's in `claude-project/skills.md`.

---

## What's Inside

```
gtm-starter-kit/
│
├── CLAUDE.md                           ← Claude Code session context. Fill in once.
│
├── context/                            ← Source of truth. Never modified by reps.
│   ├── profile.md                      ← Company overview, product, team, reference customers
│   ├── icp-definition.md              ← ICP tiers, filters, anti-ICP, qualification criteria
│   ├── signal-library.md              ← Signals with scoring, detection methods, hooks
│   ├── positioning.md                 ← Value pillars, competitive positioning, what not to say
│   ├── competitor-radar.md            ← Battlecards, win/loss patterns
│   └── personas/
│       └── template.md                ← Persona template — duplicate for each buyer role
│
├── skills/                             ← Claude executes these in Claude Code
│   ├── setup/SKILL.md                 ← Run once: populate context + deploy to Claude.ai
│   ├── research/SKILL.md              ← Account intelligence brief before outreach
│   ├── prospect/SKILL.md              ← ICP scoring and prioritization
│   ├── message/SKILL.md               ← Ready-to-send outreach copy
│   └── sync/SKILL.md                  ← Weekly context maintenance + Claude.ai re-upload list
│
├── claude-project/                     ← Claude.ai Project setup reference
│   ├── README.md                       ← How to set up and maintain the org Project
│   ├── instructions.md                ← Paste-ready Project custom instructions
│   └── skills.md                       ← Rep-facing prompt sheet to share with the team
│
├── outputs/                            ← Skill outputs from Claude Code sessions
│   ├── scoring/
│   ├── plays/
│   └── .gitkeep
│
└── examples/
    └── sample-company/                 ← Relay — fully built example with real outputs
```

---

## Output Naming Convention

```
outputs/YYYY-MM-DD-[type]-[name].md

Examples:
outputs/2024-03-15-research-northstar-analytics.md
outputs/2024-03-01-scoring-q1-prospect-list.md
outputs/plays/2024-03-01-series-b-revops-tier2/brief.md
```

---

## What Not to Put in This Repo

- **CRM data or contact lists** — never commit customer or prospect data to git
- **API keys or credentials** — use environment variables, never hardcode
- **Raw meeting transcripts** — summarize into the relevant context file
- **Pricing** — keep commercial terms out of the repo

---

## Example

`examples/sample-company/` is a fully built version of the repository for Relay, a fictional workflow automation platform. Every context file is populated and two real outputs are included: an account research brief and a live play with email sequences and performance tracking.

Use it as a reference when filling in your own files — especially `examples/sample-company/context/signal-library.md`, which shows what a mature signal library looks like with detection methods, decay logic, and performance tracking.

---

## License

MIT
