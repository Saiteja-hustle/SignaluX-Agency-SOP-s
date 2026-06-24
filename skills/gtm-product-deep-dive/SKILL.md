---
name: gtm-product-deep-dive
description: "Use this skill at the start of every new client engagement before any GTM work begins. Triggers: new client onboarded, need to understand a product from scratch, preparing source material for NotebookLM podcast, or any request to 'understand the product' or 'do a product deep dive'. Produces a structured markdown document covering what the product is, how it works, ICP signals, competitive signals, and key messaging — ready to feed into NotebookLM for podcast generation."
---

# GTM Skill 1: Product Deep Dive

## What This Skill Does

Transforms a client's raw product (website, docs, GitHub) into a structured markdown document that:
1. Gives Claude full product context for all downstream GTM work
2. Serves as the source document for a NotebookLM podcast (for deeper product understanding)
3. Becomes the client's permanent product reference in their SignaluX client folder

This is always **Workstream 1**. Nothing else starts until this is done.

---

## When To Trigger

- New client has been onboarded
- Product has significantly changed or pivoted
- Starting a new GTM sprint and product understanding needs refreshing
- User says "understand the product", "do a product deep dive", "create the NotebookLM doc"

---

## Inputs Required From Client

Before starting, collect:

| Input | Why It's Needed |
|-------|----------------|
| Product website URL | Primary source for homepage copy and positioning |
| Docs site URL (if exists) | Deep product feature detail |
| GitHub org URL (if public) | Release notes, README files, technical signals |
| 1-paragraph founder description | How the founder describes the product in their own words |
| Current customers (if any) | Social proof signals + use case validation |
| Who they think the buyer is | Starting hypothesis for ICP (will be validated later) |

If docs site doesn't exist: use homepage only + GitHub releases page.

---

## Step-By-Step Process

### Step 1: Scrape All Sources

**Homepage:**
```
web_fetch: [product URL]
```
Extract: headline, subheadline, all feature descriptions, social proof, CTAs, pricing signals.

**Docs site (if exists):**
```
web_fetch: [docs URL]/llms.txt  ← Check this first, it's an index of all pages
```
If llms.txt exists: fetch each listed URL. If not: navigate docs manually and fetch key sections.

**GitHub releases (if public):**
```
web_fetch: github.com/[org]/[repo]/releases
```
Extract: recent release notes, feature names, changelog language.

**Web search supplement:**
```
web_search: "[product name] site:reddit.com OR site:hackernews.com"
web_search: "[product name] reviews"
```
Extract: how users describe it in their own words (not marketing language).

---

### Step 2: Synthesize Into Structured Document

Produce a markdown document with these exact sections:

```markdown
# [Product Name] — Complete Product Deep Dive
### Source material for NotebookLM Podcast

---

## WHAT IS [PRODUCT]?
[2-3 paragraph plain-English explanation. What does it do? Who is it for? What problem does it solve? Written as if explaining to a smart non-technical person.]

## CORE VALUE PROPOSITION
[The single clearest statement of value. What does the customer get that they couldn't get before?]

## HOW IT WORKS
[Step-by-step: what happens when a customer uses the product. Be specific and sequential.]

## PRODUCT COMPONENTS
[Each major feature/module. For each: name, what it does, why it matters.]

## SUPPORTED INTEGRATIONS / ECOSYSTEM
[What tools/platforms/frameworks does it work with? Specificity here = trust signals for GTM.]

## TARGET CUSTOMER (HYPOTHESIS)
[Who appears to be the buyer based on product signals. NOT the locked ICP — that comes in Workstream 3. This is the raw signal.]

## COMPETITIVE SIGNALS FROM PRODUCT
[What does the product implicitly compete with? What are they positioning against?]

## KEY MESSAGING FROM PRODUCT
[Verbatim copy of: headline, subheadline, key feature descriptions. These are the seeds for positioning work.]

## SOCIAL PROOF FOUND
[Customer logos, quotes, case studies, testimonials found anywhere on the site or in search.]

## OPEN QUESTIONS FOR FOUNDER
[Things the product doesn't make clear that need to be answered before GTM work proceeds.]

## GLOSSARY
[Any product-specific terms, acronyms, or technical vocabulary that will appear in GTM copy.]
```

---

### Step 3: Quality Check Before Handing Off

Before saving the document, verify:

- [ ] Every section is filled — no "TBD" or empty sections
- [ ] The "What Is" section can be understood by a non-technical marketer
- [ ] Key messaging section contains verbatim copy from the actual product (not paraphrased)
- [ ] Open questions are specific enough to ask the founder (not vague)
- [ ] Glossary covers all acronyms that will appear in future GTM copy

---

### Step 4: Save and Hand Off

1. Save as `[client-name]_product_deep_dive.md` in `/clients/[client-name]/`
2. Tell the client: "Feed this into NotebookLM → New Notebook → Upload source → Generate podcast"
3. This document becomes the context source for all downstream GTM workstreams

---

## Output Format

Single markdown file. Named: `[client]_product_deep_dive.md`

Length: 1,500–4,000 words depending on product complexity. Err toward more detail — this is the foundation everything else builds on.

---

## Tools Used In This Skill

| Tool | Purpose |
|------|---------|
| `web_fetch` | Scrape product site, docs, GitHub |
| `web_search` | Find user language on Reddit, HN, G2, review sites |
| Claude synthesis | Structure raw content into the markdown template |
| NotebookLM (client-run) | Generate podcast from the output doc |

---

## Common Failure Modes

| Problem | Fix |
|---------|-----|
| Docs site doesn't exist | Use homepage + GitHub only. Note what's missing in Open Questions. |
| GitHub repo is private | Skip GitHub step. Ask founder for a product one-pager or internal doc instead. |
| Product has recently pivoted | Don't use old docs. Scrape current homepage only and note pivot in the doc. |
| Founder description contradicts website | Include both. Flag the discrepancy in Open Questions. |
| Token limit hit on docs scraping | Use llms.txt index to prioritize which pages matter most. Fetch top 10 only. |

---

## Connected Workstreams

After this skill is complete → run `gtm-competitive-research` (Workstream 2).

The product deep dive document feeds directly into:
- Competitive research (what category to research)
- ICP definition (who the product signals it's for)
- Positioning strategy (raw messaging to react against)
