---
name: gtm-competitive-research
description: "Use this skill when you need to research competitors for a B2B SaaS client before positioning or copy work. Triggers: 'research competitors', 'who are the competitors', 'competitive analysis', 'what are competitors saying', or when starting Workstream 2 of the SignaluX GTM process. Requires gtm-product-deep-dive to be complete first. Produces a structured competitor messaging analysis and gap map."
---

# GTM Skill 2: Competitive Research

## What This Skill Does

Scrapes and analyzes competitor homepages to produce:
1. Verbatim competitor messaging (what they actually say, not summaries)
2. Category-level messaging patterns (what the whole market is saying)
3. Gap map (what no competitor is saying — the whitespace)
4. Differentiation risks (where the client's messaging overlaps with competitors)

This is **research only** — no positioning recommendations yet. Positioning comes in Workstream 4.

---

## Inputs Required

- Completed `gtm-product-deep-dive` document for the client
- Competitor list (ask founder: "Who do you lose deals to?" + "What do buyers compare you to?")
- If founder can't name competitors: use product category from deep dive to search

---

## Step-By-Step Process

### Step 1: Build The Competitor List

Start with founder's list. Then expand:

```
web_search: "[product category] alternatives"
web_search: "[product category] tools comparison"
web_search: "best [product category] 2025"
web_search: site:g2.com "[product category]"
```

Target: 5–8 competitors. More than 8 = diminishing returns. Fewer than 4 = incomplete picture.

Categorize each competitor:
- **Direct** — same product, same buyer, same problem
- **Adjacent** — overlapping buyer or problem but different solution
- **Indirect** — different product, same budget category

---

### Step 2: Scrape Each Competitor Homepage

For each competitor:
```
web_fetch: [competitor homepage URL]
```

Extract verbatim (copy exact words, do not paraphrase):
- H1 headline
- Subheadline / hero paragraph
- Primary CTA text
- 3 main feature/benefit claims
- Social proof format (logos? numbers? quotes?)
- Pricing signal (free tier? enterprise only? self-serve?)
- Any named integrations or frameworks

---

### Step 3: Run Perplexity Search For Live Messaging

```
[In Perplexity]: What is [competitor name]'s current positioning and messaging? 
What does their homepage say about what they do and who they're for?
```

Use this to supplement direct scraping, especially for recently updated pages.

---

### Step 4: Synthesize Into Competitor Analysis Document

Structure:

```markdown
# [Client] — Competitive Research
Date: [date]

## Competitor Overview Table

| Competitor | Type | H1 | Primary Claim | Social Proof | Pricing Signal |
|-----------|------|-----|---------------|--------------|----------------|
| [name] | Direct | "[exact H1]" | "[exact claim]" | [logos/numbers/quotes] | [free/paid/enterprise] |

## Per-Competitor Deep Dives

### [Competitor Name]
- **URL:** 
- **Type:** Direct / Adjacent / Indirect
- **H1:** "[verbatim]"
- **Subheadline:** "[verbatim]"
- **Top 3 claims:** 
  1. "[verbatim]"
  2. "[verbatim]"
  3. "[verbatim]"
- **Social proof:** [describe exactly what they show]
- **Integrations mentioned:** 
- **Notable:** [anything unusual or worth flagging]

## Category Messaging Patterns

What messaging themes appear across 3+ competitors:
- [Theme 1]: Used by [competitor names]
- [Theme 2]: Used by [competitor names]

These are the "table stakes" messages — if everyone is saying it, it's not a differentiator.

## Messaging Gaps (Whitespace)

Claims that NO competitor is making:
- [Gap 1]
- [Gap 2]

These are candidate differentiators — validate against client's actual product capabilities.

## Collision Risks

Places where the client's current messaging overlaps with competitors:
- [Client claim] ← same as [competitor]'s "[their exact claim]"

These are differentiation problems to solve in positioning.

## Raw Buyer Language (From Reviews/Reddit/HN)

Phrases real users use to describe the problem (not marketing language):
- "[exact quote]" — source
- "[exact quote]" — source
```

---

### Step 5: Quality Check

- [ ] Every H1 is verbatim (not paraphrased)
- [ ] At least 5 competitors covered
- [ ] Whitespace gaps are based on actual absence of claims, not assumptions
- [ ] Collision risks are specific (exact overlap, not "similar theme")
- [ ] Raw buyer language section has at least 5 real quotes with sources

---

## Tools Used

| Tool | Purpose |
|------|---------|
| `web_fetch` | Direct competitor homepage scraping |
| `web_search` | Finding competitor list, category pages |
| Perplexity | Live competitive messaging verification |
| Gemini Deep Research | Bulk buyer language mining (Reddit, G2, Capterra, GitHub issues) |

**Gemini Deep Research prompt template:**
```
I'm doing competitive research for a B2B SaaS product in the [category] space.

Please search Reddit, G2, Capterra, GitHub issues, and LinkedIn for:
1. How do buyers describe the problem [product category] solves in their own words?
2. What do they complain about with current solutions?
3. What language do they use (not marketing language — their actual words)?

Product context: [paste product deep dive summary]

Output: raw language dump, organized by source type. No synthesis yet.
```

---

## Critical Rules

- **Never paraphrase competitor copy** — verbatim only in the analysis
- **Research before conclusions** — produce the data dump first, synthesis second
- **Don't skip adjacent competitors** — they reveal category expectations buyers bring
- **Date-stamp everything** — competitor messaging changes; old analysis misleads

---

## Connected Workstreams

Feeds into: `gtm-icp-definition` (Workstream 3) and `gtm-positioning-strategy` (Workstream 4)
