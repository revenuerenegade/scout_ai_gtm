# CLAUDE.md

Persistent context for this GTM repo. Claude Code reads this at the start of every session. The full context lives in `context/` — this file is the summary layer, enough to execute most tasks without reading anything else.

---

## Company

**[Your company name]** helps [specific customer type] [specific outcome] — without [the alternative they're currently using or the pain they're experiencing].

Stage: [Series A / B / C / bootstrapped] — [X] employees, [Y] in GTM
HQ: [City] | Website: [domain.com]

GTM motion: [Sales-led / PLG + Sales / Community-led]
ACV: [$X – $Y] | Sales cycle: [X days median]
Primary channels: [Outbound / Inbound / Events — list in order of volume]

Stack: see `context/profile.md`

---

## ICP

Full definition: `context/icp-definition.md`

**Who we sell to:** [One specific sentence. Employee range, industry, stage, what they have in place that makes them ready.]

**Tier 1 (Top 150):** [The tightest filter — what makes an account a dream account]
**Tier 2 (500–1,000):** [One step looser — still strong fit, signal-triggered]
**Tier 3 (1,000–3,000):** [Minimum criteria — automated outreach only]

**Never target:**
- [Exclusion 1 + one-line reason]
- [Exclusion 2 + one-line reason]
- [Exclusion 3 + one-line reason]

---

## Personas

Full profiles: `context/personas/`

| Role | Title(s) | Primary concern | Best channel |
|------|----------|----------------|-------------|
| Champion | [e.g., Head of RevOps] | [Specific pain they own] | [Email / LinkedIn] |
| Economic buyer | [e.g., CRO] | [What they're measured on] | [Events / Email] |
| Technical evaluator | [e.g., GTM Engineer] | [Integration / migration concern] | [Slack / LinkedIn] |

---

## Positioning

Full document: `context/positioning.md`

**We win when:** [The specific condition where we're the obvious choice]
**We lose when:** [Be honest — price, timing, a specific competitor]

vs. [Competitor A]: [Our edge in one line]
vs. [Competitor B]: [Our edge in one line]

**Voice:** [e.g., Direct and technical. No fluff. We write like we're talking to a peer, not selling to a prospect.]

---

## Signals

Full library: `context/signal-library.md`

**Act immediately (Tier 1):**
1. [Signal name] — [What fired, where it comes from, why it matters]
2. [Signal name] — [What fired, where it comes from, why it matters]
3. [Signal name] — [What fired, where it comes from, why it matters]

**Add to sequence (Tier 2):**
1. [Signal name]
2. [Signal name]

---

## Team

| Name | Role | Owns |
|------|------|------|
| [Name] | [Title] | [Clay, sequences, signals] |
| [Name] | [Title] | [CRM, reporting, inbound] |

---

## This Week

- [ ] [Priority 1 — specific, actionable]
- [ ] [Priority 2]
- [ ] [Priority 3]

---

## Quick Start

**Research an account:**
```
Research [company.com]
```

**Score a list:**
```
Score these accounts and tell me who to prioritize:
[paste list]
```

**Write messaging:**
```
Write messaging for [persona title] at [company].
Signal: [what happened]
```

**Run weekly sync (ops):**
```
Read skills/sync/SKILL.md and run the weekly sync.
```

*Reps use these prompts in the Claude.ai Project — see `claude-project/` for setup.*
