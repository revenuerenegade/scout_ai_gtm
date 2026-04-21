# Skill: Message

## How to use this in Claude.ai

Open the **Scout** Project and send:

```
Write messaging for [persona title] at [company name].
Signal: [what happened — e.g., "hired a Head of RevOps" or "raised Series B last week"]
```

Claude has your personas, positioning, signal library, and competitive intel loaded. You'll get a full outreach sequence — all touches, all channels — ready to paste and send.

For competitive accounts, add:
```
They currently use [competitor]. Don't name them in the first touch.
```

---

## Purpose

Produce polished, ready-to-send sales messaging for a specific persona, signal, or situation. This skill is about craft — the actual words that get opened, read, and replied to.

The output of this skill is not a framework or a template. It is copy — specific words, for a specific person, in a specific situation.

---

## Inputs

Before writing anything, collect:

- **Persona:** Which role are you writing to? Pull their profile from `context/personas/`
- **Signal or situation:** What's the trigger? A specific signal from `context/signal-library.md`, a known event (funding, hire, product launch), or a cold outreach scenario
- **Value prop angle:** Which capability or outcome is most relevant to this persona right now? Reference `context/positioning.md`
- **Competitive context (if applicable):** Are they using a competitor? Reference `context/competitor-radar.md`
- **Account research (if available):** Any specific context from a prior research run

---

## Competitive Situations

If the account uses a competitor, identify the scenario before writing:

| Scenario | Situation | Outreach approach |
|----------|-----------|-------------------|
| **A — Unaware** | They use a competitor but aren't looking | Lead with insight about the pain companies at their scale hit with that tool. Don't name the competitor in the first touch. |
| **B — Active eval** | Comparing you to a competitor now | Act within 24 hours. Pull the relevant battlecard. Prepare a targeted comparison on their stated criteria. Equip your champion with internal selling language. |
| **C — Negative review** | Left a negative G2/review for a competitor | Highest intent signal. Reference the pain they described without revealing you've read their review. Keep it short — this is warm. |
| **D — Under contract** | Locked into competitor until renewal | Don't pitch. Send something genuinely useful with no meeting ask. Set a follow-up for 60 days before likely renewal. |

For all scenarios, reference `context/competitor-radar.md` for the relevant battlecard before writing.

---

## Step 1: Define the Message Brief (10 min)

Before writing, answer these four questions in one sentence each:

1. **Who is this for?** [Name of persona, their specific role, what they own]
2. **Why now?** [The specific trigger — what happened that makes this the right moment]
3. **What's the one thing they get from reading this?** [The insight or value, not the product]
4. **What's the ask?** [One action, as low-friction as possible]

If you can't answer all four, do not write yet. Go back to research.

---

## Step 2: Write the Subject Line (10 min)

Write three subject line options. One per format:

**Format A — Observation-based:** References something specific and recent.
```
[Company]'s [observable event]
```

**Format B — Insight-based:** Leads with a data point or implication, not the trigger.
```
[Industry trend or benchmark that's relevant to their situation]
```

**Format C — Direct/question:** Short, almost too simple.
```
[First name] — [one question they'd actually want answered]
```

**Quality bar:** The best subject line is the one that would get opened by someone who doesn't know you, has never heard of your product, and has seen 200 emails today. Test each option against that standard.

**Avoid:**
- "Quick question" (overused, signals nothing)
- Personalization that's just filler ("saw you went to [University]")
- Subject lines that are really taglines for your product
- Any subject line that only makes sense after reading the email

---

## Step 3: Write the First Touch (20–30 min)

### Email — First Touch

Apply the PVP Standard (Permissionless Value Prop). The message must have value even if the prospect never buys from you.

**Test:** Remove your CTA. If the message is still worth reading, it passes. If it's pointless without the ask, rewrite it.

**Structure:**
```
[Signal hook — one specific, datable observation]

[Insight — what that signal means in context; something they might not know or haven't connected yet]

[Connection — one sentence linking that insight to what you do]

[CTA — one ask, as frictionless as possible]

[Signature]
```

**Length targets:**
- Tier 1 first touch: 100–150 words
- Tier 2 first touch: 75–100 words
- Tier 3 first touch: 50–75 words (templated with one variable)

---

### LinkedIn — Connection Request Note

Maximum 200 characters. One sentence of context, one sentence of ask.

```
[First name] — [one specific reason for reaching out: the signal, their post, their recent hire]. Would be good to connect.
```

**Do not:**
- Say "I'd love to connect and learn more about your work"
- Reference your product in the connection request
- Use a template that could apply to anyone in their industry

---

### LinkedIn — Direct Message (post-connection)

Use after they accept. Reference the connection context. Introduce the hook.

```
[First name], thanks for connecting.

[One sentence restating the specific context for reaching out]

[The insight — one sentence]

[CTA — same as email CTA or a lighter version: "happy to share what we've seen if useful"]
```

---

### Voicemail Script

20–30 seconds. Write it to be spoken, not read.

```
"[Name], [Your name] from [Company].

I've been reaching out over email — not trying to be persistent, just think the
timing might be relevant given [one specific reason: the signal, the hire, the
announcement].

If I'm wrong, I'll take the hint. If it's worth a conversation, call me at
[number] or shoot me a reply.

Either way — [Name], [Company]."
```

**Delivery notes:** Pause after your name. Slow down on the phone number. Sound like you're talking to a peer who might be interested, not pitching to a prospect who definitely isn't.

---

## Step 4: Write Follow-Up Touches (15 min)

### Follow-Up 1 — Different Angle (Day 3–6)

Don't repeat touch 1. Shift the frame: new proof point, different dimension of value, a question worth thinking about.

```
[First name],

Following up from [earlier this week / last week].

[New angle: a proof point from a reference customer, a relevant benchmark, a
question they might be wrestling with right now]

[One sentence connecting it to their situation]

[Same CTA or lighter version]

[Name]
```

### Follow-Up 2 — Asset or Offer (Day 7–14)

Offer something concrete. A framework, a benchmark, a piece of analysis, a question worth spending 5 minutes on.

```
[First name],

One more thing — wanted to share [specific asset or insight] in case it's useful
regardless of whether we ever talk.

[Link or brief summary of the asset]

[Name]
```

### Break-Up — Final Touch

```
Subject: Closing the loop

[First name],

I've reached out a few times — not going to keep at it.

If the timing isn't right or this isn't a fit, totally understood.

If something changes — [specific trigger: new hire, funding, product expansion] —
feel free to reach out.

[Name]
```

---

## Step 5: Write Persona Variations (if needed)

If this play targets multiple personas at the same account, write a variation for each. Same signal hook, different angle:

| Persona | Lead with | Avoid |
|---------|-----------|-------|
| Champion (operational) | Workflow friction they experience personally | ROI framing, executive metrics |
| Economic buyer | Pipeline or revenue impact | Feature details, tactical process |
| Technical evaluator | Integration, data flow, migration path | Business outcomes (let them discover those) |

Each variation should stand alone — don't assume they've talked to each other.

---

## Quality Checklist

Before presenting the output:

- [ ] Subject line would get opened by someone who doesn't know you
- [ ] First line is specific — a datable event or observable fact, not a generic compliment
- [ ] The insight in touch 1 has value without the CTA
- [ ] There is exactly one ask per message
- [ ] No jargon that only makes sense internally (your product's marketing terms)
- [ ] Voice matches the company voice from `context/positioning.md`
- [ ] Each follow-up uses a different angle — no repetition of touch 1
- [ ] If competitive: no competitor named in first touch

---

## Output Format

```markdown
# Messaging: [Persona] — [Signal or Situation]
Date: [YYYY-MM-DD]
Persona: [Title]
Signal/trigger: [Signal name or situation]
Positioning angle: [Which value prop dimension]

## Subject Lines
- A: [Observation-based]
- B: [Insight-based]
- C: [Direct/question]

## Touch 1 — Email
Subject: [Chosen subject line]

[Full email copy]

## Touch 1 — LinkedIn Connection Request
[Note text]

## Touch 1 — LinkedIn DM (post-connection)
[DM copy]

## Touch 1 — Voicemail
[Script]

## Touch 2 — Email (Different Angle)
[Full email copy]

## Touch 3 — Email (Asset or Offer)
[Full email copy]

## Break-Up Email
[Full email copy]

## Persona Variations (if applicable)
### [Persona B title]
[Variation copy]
```
