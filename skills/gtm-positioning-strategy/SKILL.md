---
name: gtm-positioning-strategy
description: "Use this skill to generate positioning angles, headline combinations, and copy principles for a B2B SaaS client. Triggers: 'positioning', 'what angle should we use', 'headline options', 'how should we position', or Workstream 4 of the SignaluX GTM process. Requires product deep dive, competitive research, and ICP to be complete. Output: 10 positioning angles (labeled Proven/Hybrid/New), 2 headline+subheadline combinations, copy principles, and messaging hierarchy."
---

# GTM Skill 4: Positioning Strategy

## What This Skill Does

Produces a positioning strategy document that:
1. Generates 10 distinct angles (not variations — genuinely different strategic bets)
2. Labels each angle by risk level (Proven / Hybrid / New)
3. Recommends 2 headline+subheadline combinations with rationale
4. Locks copy principles for all downstream work
5. Builds the messaging hierarchy for ads, emails, and outbound

This is the strategic foundation that all copy builds from.

---

## Inputs Required

- Product deep dive document
- Competitive research document (especially: whitespace gaps + collision risks)
- Locked ICP document
- Founder feedback on which angles resonate from sales calls

---

## Step-By-Step Process

### Step 1: Mine Buyer Language

Before generating angles, collect the raw material:

From competitive research buyer language section:
- Exact phrases real users use to describe the problem
- Complaints about current solutions
- Words that appear repeatedly (repetition = high resonance)

From Gemini Deep Research (if not already done in competitive research):
```
Search: [pain category] site:reddit.com
Search: [product name] review
Search: [problem description] developer forum
```

Organize by theme. Do NOT generate angles yet.

---

### Step 2: Generate 10 Positioning Angles

Each angle must be:
- Genuinely distinct (not a variation of another angle)
- Tied to a specific buyer pain or desire
- Based on a real product capability (not invented)
- Labeled: **Proven** (category-validated), **Hybrid** (proven + differentiated), or **New** (category-creating)

**Angle template:**

```markdown
### Angle [N] — [Short Name]
**Label:** Proven / Hybrid / New
**Core claim:** [One sentence — what is this angle saying?]
**Buyer pain it addresses:** [What problem does this speak to?]
**Why it works:** [Evidence from buyer language or competitive gap]
**Risk:** [What could go wrong with this angle?]
**Example headline direction:** "[rough H1 sketch]"
```

**The 10 angle categories to cover (minimum):**

1. **Speed angle** — how does the product make teams faster?
2. **Safety/confidence angle** — what risk does it reduce?
3. **Cost/ROI angle** — what does it save in time, money, or headcount?
4. **Developer experience angle** — how does it make developers' lives better?
5. **Technical differentiation angle** — what unique capability sets it apart?
6. **Integration angle** — how does it fit into existing workflow?
7. **Trust/proof angle** — what social proof or outcome data validates it?
8. **Urgency/timing angle** — why does this problem matter more now than before?
9. **Competitor displacement angle** — why switch from what they're using today?
10. **Category creation angle** — is there a new way to frame the problem entirely?

Not all 10 will be strong — that's expected. Rank them after generating.

---

### Step 3: Select 2 Combinations For Headlines

A headline combination = H1 + subheadline.

Rules for good combinations:
- H1: bold claim, 5–8 words, speaks to ICP's primary KPI
- Subheadline: expands the claim, adds specificity, addresses the "how"
- The two combinations should be meaningfully different bets (not just word variations)
- Name each combination with a strategic label (e.g., "Speed first, safety second")

**Format:**

```markdown
## Headline Combination A — [Strategic Label]
**Angle:** [Which angle(s) this draws from]
**H1:** "[headline]"
**Subheadline:** "[subheadline]"
**Rationale:** [Why this combination, what it prioritizes, what it trades off]
**Best for:** [Which channel or buyer context this works best in]

## Headline Combination B — [Strategic Label]
[Same structure]
```

---

### Step 4: Lock Copy Principles

Based on the ICP and competitive analysis, define 3–5 copy rules that apply to ALL downstream work.

**Format:**

```markdown
## Copy Principles — [Client Name]
Locked: [date]

1. **Never lead with [X]** — [reason: too technical/too vague/competitor owns it/ICP doesn't care]
2. **Never use [word/phrase]** — [reason]
3. **Always frame from [perspective]** — [ICP's perspective, not product's perspective]
4. **Lead with [pain/outcome/problem]** — [reason: what ICP responds to]
5. **[Any other client-specific rule]**
```

These principles get referenced in every downstream skill.

---

### Step 5: Build Messaging Hierarchy

The messaging hierarchy orders claims from most to least important for the ICP.

```markdown
## Messaging Hierarchy — [Client Name]

**Primary message (the hook):**
"[Core claim — one sentence that captures the whole value prop]"

**Supporting messages (in priority order):**
1. [Message 1 — expands on primary hook]
2. [Message 2 — addresses primary objection]
3. [Message 3 — adds specificity/credibility]
4. [Message 4 — speaks to secondary pain]

**Proof points to use:**
- [Specific, concrete proof point 1]
- [Specific, concrete proof point 2]
- [Specific, concrete proof point 3]

**What NOT to say:**
- [Phrase to avoid + why]
- [Phrase to avoid + why]
```

---

### Step 6: Founder Review

Send the full document with a specific question:
- "Out of the 10 angles, which 2 resonate most with what you're hearing in sales calls?"
- Do NOT ask "which do you like best" — that invites aesthetic preference, not strategic input
- Do NOT accept "all of them" — push for a rank

Validate independently: test founder's preferred angles against the buyer language data. Flag if their preference conflicts with market evidence.

---

### Step 7: Quality Check

- [ ] 10 angles are genuinely distinct (not variations)
- [ ] Each angle is labeled Proven / Hybrid / New
- [ ] 2 headline combinations have strategic labels and rationale
- [ ] Copy principles are specific (not generic "be clear and concise")
- [ ] Messaging hierarchy has a clear primary message at top
- [ ] Founder has reviewed and confirmed preferred angle direction

---

## Critical Rules

- **Research before conclusions** — generate angles from data, not intuition
- **Strategic labels required** — always name the angle and the combination. Dropping labels when reformatting is an error.
- **Independent validation** — don't just validate the founder's preferred angles. Test ALL angles against buyer language data equally.
- **Headline collision check** — before finalizing, search: "[first 3 words of H1] site:[competitor.com]" — if a competitor has the same headline structure, flag it.

---

## Connected Workstreams

Feeds into: `gtm-landing-page-copy` (Workstream 5), `gtm-roadmap` (Workstream 6), `gtm-outbound-sequence` (Workstream 7)

The positioning document + messaging hierarchy is the brief that all copy work executes against.
