# Skill: Dossier

## How to use this in Claude.ai

Open the **Scout** Project and send:

```
Read skills/dossier/SKILL.md and build a dossier for:
- [Company 1]
- [Company 2]
- [Company 3]
```

3–4 companies per run. These should be accounts with no outreach activity in the last 30 days — manually selected from your pipeline or account list.

---

## Purpose

Produce a polished, share-ready intelligence package for dormant accounts. The Dossier is not a cold-outreach prep document. It's a **re-engagement brief**: deeper than a standard research run, category-aware, and built to give a rep everything they need to walk back into a conversation with precision.

Use it before:
- Re-engagement outreach after 30+ days of silence
- An AE quarterly account review
- A pipeline scrub where you need to decide which dormant accounts to revive vs. retire

Each company section contains five layers: sub-vertical context, company deep dive, contact intelligence, signal check, and a specific re-engagement angle.

---

## Sub-Vertical Classification

For each company, identify the industry and primary sub-vertical before researching anything else. The sub-vertical determines which category intelligence to pull and which sources to use.

**How to classify:**
- Start with the company's industry (e.g., healthcare, fintech, logistics, manufacturing, SaaS)
- Then identify the specific sub-vertical within that industry (e.g., within healthcare: diagnostics, surgical devices, health IT, pharma services; within fintech: payments, lending, compliance, insurance)
- If a company spans multiple sub-verticals, identify the primary one (where most of their revenue and attention sits) and note any secondary

There is no fixed list — sub-verticals are whatever is accurate for the companies in the Dossier. Use the most specific, accurate description that would be recognized by someone in that industry.

If two companies in the same Dossier share a sub-vertical, write the category intelligence once and reference it for both.

---

## Inputs

- Company names or domains (3–4 accounts)
- `context/personas/` — to identify the right contacts to research
- `context/signal-library.md` — for signal check and scoring
- `context/icp-definition.md` — for fit context

---

## Step 1: Confirm the List

Validate input before researching anything:
- Confirm 3–4 companies are provided. If more than 4, ask which 4 to prioritize.
- Note any last-known engagement date if provided. If not provided, proceed — the 30-day dormancy is assumed.
- Identify the primary sub-vertical for each company before proceeding to Step 2.

---

## Step 2: Category Intelligence

**Run this step for each unique sub-vertical represented in the list.** If two companies share a sub-vertical, write the category intelligence once and reference it for both.

For each sub-vertical, research and summarize across these dimensions. Adapt the focus areas to what's actually relevant for that industry — not every dimension applies to every sub-vertical.

### Regulatory / Compliance
What rules, standards, or enforcement activity is shaping this space right now?
- Recent regulatory actions, guidance documents, or rule changes affecting companies in this sub-vertical
- Any new compliance requirements or enforcement trends that create urgency or friction
- Upcoming deadlines or transitions companies in this space are navigating

### Market Dynamics
What's happening to the competitive and funding landscape?
- Recent M&A: who acquired whom, what it signals about consolidation direction
- Notable funding rounds — which companies are being capitalized and for what
- New entrants or platform shifts changing how the sub-vertical competes

### Macro / Policy Tailwinds or Headwinds
What external forces are creating or removing pressure?
- Policy changes, legislation, or government priorities affecting this space
- Economic conditions (interest rates, capital availability, procurement freezes) specific to this sub-vertical
- Any coverage, reimbursement, or pricing changes (relevant for healthcare, insurance, or government-adjacent verticals)

### Technology Shifts
What's changing about how work gets done in this sub-vertical?
- Platform or modality changes reshaping the category (AI, automation, cloud migration, hardware shifts)
- Standards or interoperability developments that are creating new requirements
- Emerging tools or infrastructure that companies in this space are adopting or being pressured to adopt

### Competitive Landscape
Who's winning and losing, and why?
- Dominant players and which are gaining vs. losing ground
- Any notable product failures, service issues, or reputation events affecting incumbents
- Competitive moves (pricing changes, acquisitions, new product launches) that are shifting customer decisions

**Format:** 3–5 bullets per relevant dimension. Focus on what's current (last 90 days where possible) and specific — name companies, dates, and dollar amounts where available. Skip dimensions that don't apply to the sub-vertical rather than writing generic filler.

**Sources:** Use the best sources for the specific industry. Trade publications, regulatory agency databases, earnings releases, funding announcements, conference coverage, and industry analyst reports. Name the source when the data point is specific.

---

## Step 3: Company Deep Dive

For each company:

**Overview**
- What they make or do, who they sell to (customer type, company size, buyer function)
- Business model (SaaS, services, hardware, marketplace, etc.) and where they sit in their growth stage
- Key differentiator or positioning claim

**Regulatory / Compliance Status** *(if applicable to their industry)*
- Any notable regulatory filings, approvals, certifications, or compliance events in the last 12 months
- Any enforcement actions, audits, or compliance issues — note if none found
- If regulatory/compliance is not material to this company's industry, skip this section

**Product / Service Activity**
- Announced product launches, feature releases, or service expansions
- Any discontinued products, platform pivots, or strategic exits
- Conference presentations, published research, or public demos that hint at direction

**Funding & Growth**
- Funding stage, last round, amount, date, lead investors (if VC-backed)
- Headcount — current size and trajectory (growing, stable, contracting)
- Any recent expansion (new markets, geographies, business units, partnerships)

**Organizational Changes**
- Leadership hires or departures in the last 90 days — especially in the C-suite or the functions relevant to your sale
- Any restructuring signals (layoffs, spinoffs, acquisition activity)

**Recent News**
- Last 90 days: press releases, conference presentations, published content, trade press coverage
- Use sources appropriate to the industry (trade publications, company blog, LinkedIn announcements, earnings calls if public)

---

## Step 4: Contact Research

Identify 2–3 specific contacts per company. Reference `context/personas/` for the right titles to target.

For each contact:

| Field | What to find |
|-------|-------------|
| **Name + title** | Full name, current role, company |
| **Tenure in role** | How long in this position — shorter = higher change appetite |
| **Recent public activity** | LinkedIn posts (last 30 days), conference talks, published papers, press quotes, podcast appearances |
| **What they're thinking about** | Based on their content: what problems, trends, or initiatives are they publicly engaged with? |
| **Background** | Previous companies, education, areas of expertise that create natural common ground |
| **Prior engagement** | Any known prior interactions, email history, or mutual connections |
| **Best channel** | Based on activity pattern: heavy LinkedIn poster → LinkedIn first; active conference speaker → post-event; low digital footprint → email direct |

**Quality bar:** Every contact needs a real name. Do not include a title without a name. If you can't find a named contact for a role, say so explicitly and suggest how to find one (e.g., "No public contact found for this role — check LinkedIn for [Company] + [title] or ask your champion for an intro").

---

## Step 5: Signal Check

Reference `context/signal-library.md`. For each company:

1. Check each Tier 1 and Tier 2 signal: is it present? When did it fire?
2. Apply decay multipliers from the signal library (0–30 days = 100%, 31–60 = 75%, 61–90 = 50%, 91–180 = 25%, 180+ = expired)
3. Calculate current signal score

**Universal re-engagement triggers** — even if not in the formal signal library, flag any of the following as high-priority hooks:
- New product launch or major feature release → active investment, vendor review window
- Significant funding round (Series B+) → scaling infrastructure, buying tools
- New commercial leadership hire (VP Sales, CCO, CRO, CFO) → new budget authority, likely to re-evaluate vendors
- Major conference keynote or flagship presentation → company signaling direction, leadership accessible
- Regulatory approval, certification, or compliance milestone → commercial ramp, new budget cycle
- Negative press, product recall, or service incident → operational urgency, potential vendor switch
- Strategic partnership or acquisition → integration needs, new priorities
- Geographic expansion or new market entry → scaling needs, new buying centers

If score ≥ 40 despite 30+ days of dormancy: flag as **high-priority re-engagement** in the output.

---

## Step 6: Re-Engagement Angle

The judgment call. For each company, answer four questions:

**1. Why now?**
What happened in the last 30–60 days — in the company, in their sub-vertical, or in the broader market — that creates a natural, specific reason to re-engage? This can be company-level (new hire, product launch, funding) or category-level (regulatory shift, market event, competitor move). If company-level news is thin, category intelligence from Step 2 is the fallback.

**2. What changed since last contact?**
What's different now vs. when the last engagement happened? New product, new leadership, new funding, new market condition, new regulatory reality. If nothing changed: say so, and note that re-engagement needs a genuine new angle — don't reach out just because 30 days passed.

**3. The hook**
One sentence. Specific, datable, relevant. Should reference something that happened, not something general. Pass this test: would someone who doesn't know your product find this sentence interesting on its own?

**4. Who leads the re-engagement and how**
- Which contact (name, not title)
- Which channel (email / LinkedIn / phone)
- What tone: warm re-introduction ("following up on our conversation about X"), new angle ("something changed in your space I wanted to flag"), or trigger response ("saw your [specific news] and wanted to reach out")

---

## Output Format

One unified document. Polished, section-structured, suitable for sharing with an AE before a re-engagement push.

```markdown
# Dossier
**Accounts:** [Company 1], [Company 2], [Company 3]
**Prepared:** [YYYY-MM-DD]
**Status:** Dormant 30+ days — re-engagement brief

---

## Executive Summary

[3–4 sentences. Identify which 1–2 accounts have the strongest re-engagement case
right now and why. Flag any time-sensitive category events or signals that require
action this week. Name the specific hook for the top-priority account.]

---

## [Company 1]

**Sub-vertical:** [e.g., Surgical Robotics — primary | Digital Health — secondary]

### Category Intelligence: [Sub-vertical name]

- **Regulatory / Compliance:** [Specific regulatory or compliance activity in this space, last 90 days]
- **Market:** [M&A or funding news, specific]
- **Policy / Market:** [Macro or policy dynamics, if applicable]
- **Technology:** [Platform or modality shifts]
- **Competitive:** [Who's winning/losing, any notable events]

### Company Overview

[2–3 sentences: what they make, who they sell to, lifecycle stage]

- **Regulatory / compliance status:** [Recent activity or "No notable regulatory activity found as of YYYY-MM-DD"]
- **Pipeline:** [Known product activity or "None publicly announced"]
- **Funding:** [Stage, last round amount, date, lead investor, headcount]
- **Recent news (last 90 days):**
  - [Event, date]
  - [Event, date]
- **Org changes:** [Key hires/departures or "None identified"]

### Contacts

| Name | Title | Tenure | Reach via | What they're focused on |
|------|-------|--------|-----------|------------------------|
| [Full name] | [Title] | [X mo] | [Channel] | [Recent post/talk/theme] |
| [Full name] | [Title] | [X mo] | [Channel] | [Recent post/talk/theme] |

### Signal Check

| Signal | Status | Score | Decay | Adjusted |
|--------|--------|-------|-------|---------|
| [Signal name] | Active | +[X] | [X]% | +[X] |
| [Signal name] | Inactive | — | — | — |

**Current signal score: [X]/100**
[If ≥ 40: flag as HIGH PRIORITY despite dormancy]

### Re-Engagement Angle

- **Why now:** [Specific trigger — company or category level]
- **What changed:** [Since last engagement]
- **Hook:** [One sentence, specific and datable]
- **Lead with:** [Full name] via [channel] — [tone: warm re-intro / new angle / trigger response]

---

[Repeat structure for Company 2, 3, 4]

---

## Re-Engagement Priority Order

| Priority | Company | Signal score | Hook strength | Act by |
|----------|---------|-------------|--------------|--------|
| 1 | [Company] | [X] | [One-line reason] | [This week / This month] |
| 2 | [Company] | [X] | [One-line reason] | [This week / This month] |
| 3 | [Company] | [X] | [One-line reason] | [This month / Hold] |
```

---

## Output Location

Save to: `outputs/dossier/YYYY-MM-DD-dossier-[co1]-[co2]-[co3].md`

Example: `outputs/dossier/2026-04-21-dossier-acuity-medovation-spectra.md`

---

## Quality Standard

Before presenting the Dossier:

- [ ] Every company has a named sub-vertical
- [ ] Category intelligence contains at least one specific, dated data point per company (not general descriptions)
- [ ] Every contact has a full name — no anonymous titles
- [ ] The hook for each company is specific and datable — passes the "would this be interesting without our product?" test
- [ ] Signal scores use decayed values, not raw scores from stale signals
- [ ] Universal re-engagement triggers (funding, new commercial hire, product launch, regulatory milestone, negative press, acquisition) are checked even if not in the formal signal library
- [ ] The executive summary names 1–2 accounts to act on this week and says exactly why
- [ ] Re-engagement priority table has a clear #1 with a reason
