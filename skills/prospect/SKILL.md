# Skill: Prospect

## How to use this in Claude.ai

Open the **[Company] GTM Assistant** Project and send:

```
Score these accounts and tell me who to prioritize:
[paste company names or domains]
```

For a single account:
```
Score [company.com] against our ICP
```

Claude has your ICP criteria and signal definitions loaded. You'll get a scored table (batch) or a full breakdown (single account), sorted by priority, with a recommended next action for each.

---

## Purpose

Score any account against your ICP and assign it to the right tier. Replaces gut feel with a repeatable model. Run it before building your prospecting list for the week, after a new batch comes in from marketing, or when deciding which pipeline accounts to focus on.

---

## Inputs

- Account name, domain, and any available firmographic/technographic data
- `context/icp-definition.md` — scoring criteria and tier definitions
- `context/signal-library.md` — signal scores to add on top of ICP fit

---

## Scoring Model

### Part 1: ICP Fit Score (0–70 points)

Measure how well the account matches your ideal customer profile.

#### Firmographic Fit (0–30 points)

| Criterion | Points | How to assess |
|-----------|--------|---------------|
| Employee count in range | 0–10 | [Your range from ICP definition] |
| Industry match | 0–10 | Primary = 10, Secondary = 5, Other = 0 |
| Funding stage match | 0–10 | Ideal stage = 10, Adjacent = 5, Outside = 0 |

#### Technographic Fit (0–20 points)

| Criterion | Points | How to assess |
|-----------|--------|---------------|
| Uses [key integration tool] | 0–10 | Confirms workflow match |
| Uses [secondary tool] | 0–5 | Confirms sophistication level |
| No [disqualifying tool] | 0–5 | Absence of competitive blocker |

#### Organizational Fit (0–20 points)

| Criterion | Points | How to assess |
|-----------|--------|---------------|
| Has [key role/function] | 0–10 | Confirms decision-maker exists |
| [Role] hired in last 12 months | 0–5 | New leader = change appetite |
| Hiring for [relevant role] | 0–5 | Active investment in function |

---

### Part 2: Signal Score (0–30 points)

Add points for active signals from `context/signal-library.md`. Reference the point values defined there.

**Note:** Signal scores decay over time. Apply the decay multipliers from `context/signal-library.md` — a signal at 91–180 days is worth 25% of its original value; at 180+ days it expires entirely.

---

### Total Score Interpretation

| Total | Tier | Action |
|-------|------|--------|
| 80–100 | Tier 1 | Immediate outreach — run Research first, then Message |
| 60–79 | Tier 2 | Signal-triggered sequence within 48 hours |
| 40–59 | Tier 3 | Add to automated sequence |
| 20–39 | Tier 4 | Monitor, check again in 90 days |
| 0–19 | Exclude | Remove from active list |

---

## Output Format

### Single Account

```markdown
# ICP Score: [Company Name]
Date: [YYYY-MM-DD]

## Score Breakdown

| Category | Score | Max | Notes |
|----------|-------|-----|-------|
| Firmographic fit | X | 30 | [Key observations] |
| Technographic fit | X | 20 | [Key observations] |
| Organizational fit | X | 20 | [Key observations] |
| Active signals | X | 30 | [Signals present] |
| **Total** | **X** | **100** | |

## Tier Assignment: [Tier 1 / 2 / 3 / 4 / Exclude]

## What Qualifies Them
- [Specific reason 1]
- [Specific reason 2]

## What Reduces the Score
- [Gap — what would need to change for a higher tier]

## Recommended Next Action
[Specific: Research → Message, or which sequence to assign, or what signal to watch for]
```

### Batch (multiple accounts)

Output a table sorted by total score descending:

| Account | Tier | Score | Top qualifying reasons | Next action |
|---------|------|-------|----------------------|-------------|
| [Name] | 1 | 88 | [2–3 reasons] | Research + immediate outreach |
| [Name] | 2 | 65 | [2–3 reasons] | Sequence: [name] |
| [Name] | 4 | 28 | [1–2 reasons] | Monitor |

Flag any Tier 1 accounts (80+) at the top of the output.
