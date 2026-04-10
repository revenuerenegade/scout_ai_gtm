# Skill: Setup

**Duration:** 15–30 minutes (including your review)
**Run once:** When you first clone this repo
**Output:** All context files pre-populated, CLAUDE.md ready to use

---

## Quick Start

```
Read skills/setup/SKILL.md and set up this repo for [your-domain.com]
```

That's it. Claude will research your company, ask for any internal documentation you have, pre-fill every context file with real data, and write the full repo in one shot.

---

## What This Does

Instead of filling in 6 context files from blank templates, you provide a domain and Claude does the research. The output is a repo that's 70–80% complete from public information alone — and closer to 90–95% if you have internal docs to share.

**What Claude can find publicly:**
- Company overview, product description, value proposition
- Funding stage and amount (Crunchbase)
- Headcount and growth (LinkedIn)
- Tech stack (BuiltWith, job postings)
- Key customers and use cases (website, case studies, G2 reviews)
- Competitors (G2, website, positioning language)
- Buyer personas (job postings, team page, customer titles)
- Existing signal indicators (hiring patterns, recent news)

**What internal docs unlock (if you have them):**
- Actual ICP definition, tiers, and anti-ICP criteria
- Real persona profiles with pain points and objection patterns
- Validated messaging — the exact language that resonates
- Use cases tied to specific customer segments
- Win/loss patterns from real deals
- Signals your team has actually observed

**What gets marked `[inferred]` if neither public data nor internal docs cover it:**
- ACV range and deal profile
- Anti-ICP — who explicitly wastes your time
- Top 3 signals you've observed or want to track
- Current week's priorities
- Competitive dynamics not visible publicly

Claude writes the repo after research + any docs you share. After you see the result, it offers a targeted refinement pass for fields still marked `[inferred]`. Skip it and the repo still works.

---

## Step 1: Research the Company

**If public data is limited** (bootstrapped company, stealth stage, minimal web presence): use what's available and mark more fields as `[inferred]`. A company with no Crunchbase entry → mark funding stage as `[inferred: bootstrapped or undisclosed]`. No G2 presence → skip competitor reviews, infer from their own positioning language. No case studies → infer personas from job postings and team page only. The repo will be less complete but still usable — the docs step and refinement pass exist exactly for this situation.

Given the domain, Claude researches:

### Company snapshot
- Visit the domain. Extract: what they do, who they sell to, what problem they solve, how they position themselves. Look for customer logos, case studies, and the language they use to describe their own ICP.
- Check Crunchbase (crunchbase.com/organization/[company]): funding history, total raised, last round, lead investors, date.
- Check LinkedIn (linkedin.com/company/[company]): headcount, growth rate, recent hires, team structure.

### Product and positioning
- Read their homepage, pricing page, and "customers" or "case studies" page.
- Extract: primary value proposition, who it's for, what they replace or displace, proof points they highlight publicly.
- Note any "what not to say" signals — language on their site that suggests what they want to avoid being confused with.

### Competitors
- Check G2 (g2.com) for their category. Note the top 3–5 alternatives listed.
- Look for "vs." pages on their site or competitors' sites.
- Note any direct competitor mentions in their positioning.

### Buyer personas
- Check their team page and job postings. Who do they hire for? What titles appear in customer quotes and case studies?
- Look for the titles of people writing reviews on G2.
- Identify 2–3 likely buyer personas based on what you find.

### Tech stack and signals
- Check BuiltWith (builtwith.com/[domain]) for their own tech stack — useful context.
- Look at recent job postings for signals about who they're targeting (required tools, experience with specific platforms).
- Note any recent press, funding announcements, product launches.

---

## Step 2: Request Internal Documentation

After completing research, pause and ask the user for internal docs **before** writing any files. Internal docs replace inference with ground truth — the more you have, the fewer `[inferred]` tags end up in the repo.

Present this message exactly:

```
Research complete. Before I write the context files, do you have any
internal documentation you can share? Even one doc cuts the inference
significantly.

Most useful (in order):
1. Persona profiles or buyer personas doc — titles, pains, objections, what they care about
2. Messaging framework or messaging house — positioning statements, value pillars, what not to say
3. Use case library — specific use cases tied to segments or personas
4. ICP definition — your actual tiers, firmographic criteria, anti-ICP
5. Battlecards or competitive intel — win/loss patterns, how you beat each competitor
6. Sales deck or pitch deck — often contains the clearest articulation of positioning
7. Win/loss report or call recordings summary — what actually drives deals

Drop any files directly into the chat. Share as many or as few as you have.
If you don't have any of these, just type "skip" and I'll write from public data.
```

**When the user shares docs:**
- Read every file they share before writing anything
- Extract: ICP criteria, persona details, messaging language, use cases, competitive angles, signals, objection patterns
- Note the source of each key piece of data — "from messaging doc" vs. "from public data" vs. "[inferred]"
- Reconcile conflicts between internal docs and public data by defaulting to the internal doc (internal = ground truth)

**When the user skips:**
- Proceed immediately to Step 3. Do not ask again.

**Acceptable doc formats:** Any readable file — Google Doc export, PDF, Notion export, Word doc, slide deck, CSV, plain text. If a file is unreadable, note it and proceed with what you have.

---

## Step 3: Write All Context Files

Do not ask any more questions. Write every context file immediately using research + any docs provided. Prioritize data in this order:

1. **Internal docs** — use verbatim or lightly edited. This is ground truth.
2. **Public data** — from the research in Step 1.
3. **Inference** — only when neither source covers it. Always mark as `[inferred]`.

The goal is a working repo the user can immediately run skills against. Do not write placeholder text — every field should have a real value, a doc-sourced value, or a clearly marked inference.

Write files in this order:

### 1. `context/profile.md`
Fill with: company overview from research, product description, deal profile (from docs if available, otherwise `[inferred]` from pricing page and customer base), reference customers from public case studies or doc.

### 2. `context/icp-definition.md`
Fill with:
- Tier 1: from ICP doc if provided; otherwise infer from positioning and customer base
- Tier 2: adjacent segments — from doc or inferred from customer base
- Anti-ICP: from doc if provided (this is the hardest to infer publicly — mark `[inferred]` if not in docs)
- ICP evolution log: one entry dated today — "Initial definition from setup. Sources: [list what was used — internal doc / public data / inferred]. Validate against first 90 days of scored accounts."

### 3. `context/signal-library.md`
Fill with:
- Tier 1 signals: use signals named in internal docs first; fill remaining slots with inferred signals from hiring patterns and funding events. Structure each with definition, detection method, point value, decay curve, and message hook.
- Tier 2 signals: from docs or inferred from company category
- Signal combinations: at least 1 combination using signals above
- Performance log: empty table with headers, ready to fill

### 4. `context/positioning.md`
Fill with:
- Core positioning statement: from messaging doc if provided; otherwise extracted from homepage and pricing page
- Value pillars: use the exact language from the messaging doc if available. Do not paraphrase. If not available, infer from what they emphasize publicly.
- Use cases: from use case library if provided; otherwise infer from case studies and customer logos
- Messaging by persona: one row per persona — primary hook, proof point, what to avoid. Pull from docs; infer where not covered.
- Competitive positioning: from battlecards if provided; otherwise from research
- What not to say: from messaging doc if available; otherwise infer from their own positioning language
- Reference customers: from doc or public case studies

### 5. `context/competitor-radar.md`
Fill with:
- Top 3 competitors from research or battlecards
- For each: when they win, when they lose, our best counter-move. Use battlecard data if provided — this is where docs make the biggest difference.
- Note if win/loss patterns are from internal data or `[inferred]` from public reviews and positioning.

### 6. `context/personas/`
Create one file per persona. If persona docs were shared, use them as the primary source and supplement with public data. For each:
- Title, seniority, decision role
- What they measure themselves on — from doc, or inferred from job postings and G2 reviews
- Core pains and objections — from doc, or inferred from review language and sales content
- What gets their attention — from doc or content they engage with publicly
- Outreach hooks: one hook per Tier 1 signal from the signal library. Use messaging from the messaging doc where available.

### 7. `CLAUDE.md`
Fill with all of the above — ICP summary, top 3 signals, persona table, positioning summary. For "This Week's Priorities," leave blank with a prompt: `[Update with current campaign focus before running skills]`.

---

## Step 4: Present the Summary and Offer Refinement

After writing all files, show a summary that distinguishes doc-sourced from inferred fields — then offer a targeted refinement pass only for what's still `[inferred]`.

```
Setup complete for [Company].

Here's what was written:

- CLAUDE.md — full context layer
- context/profile.md — company overview, product, [N] reference customers
- context/icp-definition.md — [N] tiers [from: internal doc / public data / inferred]
- context/signal-library.md — [N] signals with detection methods
- context/positioning.md — value pillars, messaging by persona, competitive summary
- context/competitor-radar.md — [N] competitors [from: battlecards / public data / inferred]
- context/personas/ — [N] personas: [titles] [from: persona doc / public data / inferred]

[If inferred fields remain]:
Fields still marked [inferred]: [list them]
These are Claude's best guess — good enough to run skills against,
but may not match your actual win patterns.

---

You can start using the repo right now:

  Read skills/account-research/SKILL.md and research [example account from their ICP]

---
[If inferred fields remain]:
Want to sharpen what's still inferred? I'll ask only about the gaps —
[N] questions based on what wasn't in the docs. Takes 2–3 minutes.

Type "refine" to continue, or skip and start running skills.
```

If there are no `[inferred]` fields remaining, skip the refinement offer entirely — the repo is complete.

---

## Step 5: Targeted Refinement Pass (Optional)

Only run this if `[inferred]` fields remain after Step 3.

Identify which fields are still `[inferred]` and ask only the questions needed to resolve them. Do not ask the full 5-question list if docs already covered those fields.

**Standard questions (ask only if field is still inferred):**

```
[Ask only the questions relevant to remaining [inferred] fields]

ACV range — what's a typical deal worth?
(Only ask if not found in docs or pricing page)
e.g., "$20k–$80k" or "sub-$5k self-serve to $200k enterprise"

Anti-ICP — who explicitly wastes your time?
(Only ask if not in ICP doc)
Which company types, sizes, or situations should never enter your pipeline?

Top 3 signals — what tells you an account is ready to buy?
(Only ask if not in docs or signal library is fully inferred)
Can be rough — I'll structure them.

This week — what's your current focus? Any active or planned campaigns?
(Always ask — this changes too frequently to be in any doc)

Competitive nuance — anything not in what you shared?
(Only ask if battlecards were not provided or are missing a key competitor)
```

After receiving answers, update every relevant file — replace `[inferred]` fields with confirmed data. Then confirm what changed:

```
Updated with your answers:

- [file] — [what changed]
- [file] — [what changed]

All [inferred] flags removed.
[If any remain]: Still inferred: [list] — update these when you have the data.
```

---

## Quality Standard

Before presenting the summary, verify:

- [ ] No file contains lorem ipsum, "TBD", or generic placeholder text
- [ ] Every signal has a detection method (not just a description)
- [ ] Every persona has at least one outreach hook tied to a real signal
- [ ] Messaging in `positioning.md` uses the company's own language where docs were provided — not paraphrased
- [ ] CLAUDE.md is scannable in under 2 minutes
- [ ] The ICP definition is specific enough that two people would build the same list from it independently
- [ ] Anti-ICP has at least 3 explicit exclusions
- [ ] Every `[inferred]` tag is clearly labeled — no silent guesses

If any of these fail, fix the file before presenting the summary.
