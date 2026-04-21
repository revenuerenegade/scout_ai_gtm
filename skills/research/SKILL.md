# Skill: Research

## How to use this in Claude.ai

Open the **[Company] GTM Assistant** Project and send:

```
Research [company.com]
```

That's it. Claude has your ICP, signals, personas, and competitive context loaded automatically. The full research brief will appear inline — copy it into your CRM notes or call prep doc.

---

## Purpose

Build a complete intelligence brief on a target account before any outreach. The goal is not a company summary you could get from their About page. The goal is to find the specific trigger — the moment, the hire, the product shift, the funding event — that makes this the right time to reach out, and the right angle to use.

---

## Inputs

- Account name and domain
- `context/icp-definition.md` — to score fit
- `context/signal-library.md` — to check for active signals
- `context/competitor-radar.md` — to flag competitive context
- `context/personas/` — to identify the right stakeholders

---

## Research Steps

### Step 1: Company Snapshot (5 min)

Pull the basics. Don't stop here — this is table stakes.

- **Funding history:** Last round, amount, date, lead investors. Calculate months since last raise.
- **Headcount and growth:** Current size, growth rate over last 12 months. Is it accelerating?
- **Recent hires:** What roles have they added in the last 90 days? Especially in GTM, ops, data, or the function your product serves.
- **Product updates:** Recent changelog, press releases, or product announcements. Are they expanding into an area relevant to your product?
- **Tech stack:** What tools are they using? Identify integration opportunities and displacement signals.

Sources: LinkedIn, Crunchbase, BuiltWith, their own blog and changelog.

---

### Step 2: Stakeholder Map (10 min)

Identify the 2–3 people to reach. Reference `context/personas/` for titles and roles to target.

For each stakeholder:
- Full name and current title
- Time in role (shorter tenure = more likely to be making changes)
- Recent activity: LinkedIn posts, conference talks, published content — what are they thinking about?
- Mutual connections or shared context (alumni, past companies, investors in common)
- Best channel based on their activity patterns

---

### Step 3: Signal Check (5 min)

Reference `context/signal-library.md`. For each Tier 1 and Tier 2 signal:

- Is this signal present for this account?
- When did it fire?
- What's the current signal score?

If score ≥ 60: outreach should go out within 48 hours.
If score < 40: note the gap and flag what would change the picture.

---

### Step 4: Competitive Context (5 min)

Reference `context/competitor-radar.md`.

- Is there any evidence they use a competitor? (Job postings, tech stack, content)
- If yes: which competitive angle applies?
- Are they evaluating alternatives? (Job postings for vendor evaluation, RFP language on LinkedIn)

---

### Step 5: The Angle (10 min)

This is the only thing that matters. Everything above was research. This step is judgment.

Answer these questions:

1. **Why now?** What's the specific event or condition that makes this the right moment to reach out? If you can't answer this, don't reach out yet.

2. **Why us?** What's the specific capability or outcome that maps to their current situation — not our general value prop, but the specific thing they need right now?

3. **What's the hook?** The first line of the email. It should reference something specific — a recent hire, a product move, a funding event — and connect it to a relevant insight. Not "I saw you raised Series B." Something they'd actually want to read.

4. **Who leads?** Which stakeholder gets the first touch, and in what channel?

---

## Output Format

Produce the full brief below. Format it clearly — reps will copy this into CRM notes or their call prep doc.

```markdown
# Account Research: [Company Name]
Date: [YYYY-MM-DD]
Signal score: [X/100]
Recommended action: [Immediate outreach / Sequence / Monitor / Skip]

## Company Snapshot
[2–3 sentences: what they do, stage, recent momentum]

## Funding & Growth
- Last round: [Amount, Date, Lead]
- Headcount: [X, growth rate]
- Key recent hires: [Roles, dates]

## Tech Stack
- [Tools identified]
- Integration opportunities: [List]
- Displacement signals: [List]

## Stakeholder Map
| Name | Title | Tenure | Reach via | Notes |
|------|-------|--------|-----------|-------|
| [Name] | [Title] | [X months] | [Channel] | [Key context] |

## Active Signals
| Signal | Status | Fired | Score contribution |
|--------|--------|-------|-------------------|
| [Signal] | Active/Inactive | [Date] | +[X] pts |

## Competitive Context
[Any competitor usage or evaluation signals]

## The Angle
**Why now:** [Specific trigger]
**Why us:** [Specific fit]
**Hook:** [Proposed first line]
**Recommended sender:** [Name / Role]

## Suggested Next Action
[Specific: which persona to contact first, which channel, what signal to reference in the first touch]
```

---

## Quality Check

Before presenting the output, confirm:

- [ ] The "why now" is specific — a datable event or observable condition, not a generic assumption
- [ ] The stakeholder map has at least 2 people with contact info
- [ ] Signal score is calculated and recorded
- [ ] The hook would make sense to someone who doesn't know our product
- [ ] Competitive context has been checked
