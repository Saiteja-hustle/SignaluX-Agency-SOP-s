---
name: gtm-landing-page-copy
description: "Use this skill to write full landing page copy for a B2B SaaS client. Triggers: 'write the landing page', 'landing page copy', 'homepage copy', or Workstream 5 of the SignaluX GTM process. Requires positioning strategy to be complete and approved. Produces 12-section landing page copy confirmed section-by-section with client, plus an editorial DOCX with rationale for each section."
---

# GTM Skill 5: Landing Page Copy

## What This Skill Does

Produces complete, production-ready landing page copy across 12 sections — confirmed section by section with the client — plus a DOCX deliverable with editorial notes explaining why each section is structured the way it is.

This is not a brief or an outline. This is ready-to-publish copy.

---

## Inputs Required

- Locked positioning strategy document (especially: chosen headline combination + copy principles)
- Locked ICP document (who we're writing for)
- Competitive research (what to differentiate from)
- Product deep dive (accurate product claims)
- Any real proof: customer quotes, logos, outcome metrics, framework names

---

## The 12-Section Structure

Every B2B SaaS landing page follows this structure. Do not deviate from the order.

| # | Section | Purpose |
|---|---------|---------|
| 1 | Hero | First impression — hook + primary CTA |
| 2 | Social proof bar | Credibility signal above the fold |
| 3 | Problem statement | Validate the pain before pitching the solution |
| 4 | Solution overview | What the product does at the category level |
| 5 | How it works | Step-by-step product narrative |
| 6 | Feature deep dive | Specific capabilities with outcomes |
| 7 | Proof / metrics | Numbers, outcomes, third-party data |
| 8 | Integrations | "Works with what you have" trust signal |
| 9 | Social proof (testimonials) | Real customers, real words |
| 10 | Security / trust | Address objections proactively |
| 11 | FAQ | Handle remaining objections |
| 12 | Final CTA | Last chance to convert |

---

## Step-By-Step Process

### Step 1: Brief Review

Before writing, read and confirm:
- Which headline combination did the founder approve?
- What are the copy principles? (What never to say, what always to lead with)
- What proof exists? (Real logos, real quotes, real metrics — no invented social proof)
- What are the two CTAs? (Primary = "Book a demo"; confirm secondary CTA)

---

### Step 2: Write Section By Section — Confirm Each Before Proceeding

**Critical rule: Write one section. Present it. Wait for client "yes" before writing the next.**

Do not batch sections. Do not present multiple sections at once. The client must read and confirm each section because later sections depend on choices made in earlier ones.

**Section writing rules:**
- Lead each section with the ICP's perspective, not the product's perspective
- Every benefit claim needs a specific "so that" — what does this mean for the buyer?
- No generic superlatives: "powerful", "seamless", "robust", "revolutionary", "game-changer"
- Shorter sentences than you think. Technical buyers skim.
- Every section ends with a micro-transition to the next section's idea

---

### Section Templates

**Section 1: Hero**
```
Eyebrow: [Category label — 3-5 words]
H1: [Approved headline from positioning strategy]
Subheadline: [Approved subheadline — expands claim, adds specificity]
Primary CTA: [Primary CTA text — "Book a demo" is default]
Secondary CTA: [Secondary CTA text — link style]
```

**Section 2: Social Proof Bar**
```
Format: [Logo] [Logo] [Logo] [Logo] [Logo]
Caption: "Trusted by engineering teams at [company type]"
```
Only use real logos. If no logos yet: use a metric or a single testimonial quote instead.

**Section 3: Problem Statement (3 problem cards)**
```
Card 1: [Problem 1 name]
[2-3 sentences describing the exact pain — in buyer language]

Card 2: [Problem 2 name]
[2-3 sentences]

Card 3: [Problem 3 name]
[2-3 sentences]
```
Problem cards use "we" language (shared problem) or "your" language (their problem) — never "engineers" as a third party when writing for CTOs.

**Section 4: Solution Overview**
```
Eyebrow: "How [Product] works"
H2: [Solution category claim]
Body: [2 paragraphs — what the product does at the category level, not feature level]
```

**Section 5: How It Works (3-4 steps)**
```
Step 1: [CTO-level outcome as title, not mechanical description]
[Explanation of what happens — 2 sentences]

Step 2: [Same structure]
Step 3: [Same structure]
```

**Section 6: Feature Deep Dive (3-4 feature cards)**
```
Feature: [Name]
[What it does] + [What that means for the buyer]
```

**Section 7: Proof / Metrics**
```
[Metric] — [What it means]
[Metric] — [What it means]
[Metric] — [What it means]
```
Only use real metrics. If no real metrics yet: use third-party category data (cite source).

**Section 8: Integrations**
```
H2: "Works with [framework/tool category] teams already use"
[Integration logos or text list]
Subtext: "No migration. No replacement. Drop it in."
```

**Section 9: Testimonials**
```
[Real quote — in the customer's words]
[Name, Title, Company]
```
Only real quotes. If no quotes yet: mark as TBD and note it as a pre-launch action item.

**Section 10: Security / Trust**
```
3-card format:
Card 1: [Security claim]
Card 2: [Privacy/data claim]
Card 3: [Reliability claim]
```

**Section 11: FAQ (5-7 questions)**
Target the real objections from the ICP, not generic questions. Source: founder's sales call objections.

**Section 12: Final CTA**
```
H2: [Urgency-framed benefit claim]
Subheadline: [Time-anchored outcome — "30 minutes from now..."]
Primary CTA: [Same as hero]
```

---

### Step 3: Compile Into DOCX

After all 12 sections are confirmed:

Use `docx` skill to produce a DOCX with:
- Section title
- Editorial note: why this section matters, what it covers, what changed from any prior version
- Final confirmed copy

File name: `[client]_Landing_Page_Copy_v[N].docx`

---

### Step 4: Quality Check

- [ ] All 12 sections present
- [ ] No invented social proof (no logos, quotes, or metrics without real sources)
- [ ] Copy principles are followed throughout (check against the list from positioning)
- [ ] CTAs are consistent (same text, same style) across all sections
- [ ] No banned words used
- [ ] DOCX has editorial notes for every section

---

## Critical Rules

- **Section-by-section confirmation is non-negotiable** — never batch sections
- **No invented proof** — mark gaps as TBD, note as pre-launch action items for founder
- **Copy principles carry through** — check every section against the locked principles
- **CTA consistency** — primary CTA text must be identical across all touchpoints (hero, section headers, final CTA)

---

## Connected Workstreams

Feeds into: HTML prototype (optional, build from this copy) and `gtm-roadmap` (Workstream 6)

Requires: `gtm-positioning-strategy` complete and approved
