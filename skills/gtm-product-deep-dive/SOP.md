# SOP-01: Product Deep Dive
**SignaluX GTM Operating System**  
Version 1.0 | Owner: Teja | Last updated: June 2026

---

## Purpose

Every GTM engagement starts here. Before writing a single line of copy, running a single ad, or sending a single outreach message — we understand the product.

This SOP tells you exactly how to take a new client from "I don't know what this product does" to a complete, structured product document that becomes the foundation for everything else.

**Time required:** 2–4 hours  
**Who does this:** The account lead (or Claude with account lead reviewing output)  
**Output:** One structured markdown document saved to the client folder

---

## Why This Exists

Bad GTM almost always traces back to the same root cause: the marketer didn't understand the product deeply enough. They copied the founder's language, which was either too technical or too vague. They targeted the wrong buyer. They led with the wrong pain.

This process forces you to go to the source — the actual product, the actual docs, the actual user language — before forming any opinions.

---

## Before You Start: Collect These From The Client

Have a 30-minute kickoff call or async form. You need:

1. **Product website URL** — the live site customers see
2. **Docs URL** — if it exists (often docs.[product].com or [product].com/docs)
3. **GitHub org** — if they have a public repo (ask even if you're not sure)
4. **Founder's description** — ask them: "Describe what your product does in 2-3 sentences the way you'd explain it to a customer"
5. **Existing customers** — names, logos, industries if they have any
6. **Buyer hypothesis** — who do they think buys this? (Job title, company stage, team size)

Do NOT start the deep dive without at least #1 and #4.

---

## The Process

### Phase 1: Scrape (45–90 minutes)

Work through these sources in order:

**Source 1: The Homepage**
- Read every word. Don't skim.
- Copy: headline, subheadline, all feature names, all benefit statements, CTA text, pricing signals, any social proof
- Note: what problem does the hero section lead with? What is the first thing they want you to feel?

**Source 2: The Docs Site**
- If there's a `/llms.txt` file, check it first — it's an index of all doc pages
- Work through: Getting Started, Core Features, Integrations, API/CLI reference
- You don't need to read every page. You need to understand every major capability.
- Copy: any technical specifics that would matter to a buyer (frameworks supported, setup time, CI environments, etc.)

**Source 3: GitHub (if public)**
- Check the README first
- Check recent releases/changelog — what have they been building? This reveals product direction.
- Note: any interesting technical architecture decisions that become differentiation signals

**Source 4: User Language (search)**
- Search Reddit, Hacker News, G2, Capterra for the product name or category
- You are looking for: how do users describe the problem in their own words? What language do they use?
- This is buyer language, not product language. Both matter but they are different.

---

### Phase 2: Synthesize (45–60 minutes)

Fill in the 11-section template (see below). Rules:
- Write the "What Is" section as if explaining to a smart non-technical person
- Use verbatim product copy in the "Key Messaging" section — don't paraphrase
- Be specific in "Open Questions" — vague questions don't get useful founder answers

**The 11 Sections:**
1. What Is [Product]?
2. Core Value Proposition
3. How It Works
4. Product Components
5. Supported Integrations / Ecosystem
6. Target Customer (Hypothesis)
7. Competitive Signals From Product
8. Key Messaging From Product
9. Social Proof Found
10. Open Questions For Founder
11. Glossary

---

### Phase 3: Quality Check (15 minutes)

Before calling it done, check every item:

- [ ] All 11 sections are filled — no empty sections
- [ ] "What Is" section: read it out loud. Would a non-technical marketer understand it?
- [ ] "Key Messaging" section: is this verbatim from the product, not your paraphrase?
- [ ] "Open Questions": are these specific enough to ask the founder directly?
- [ ] "Glossary": does it cover every acronym that will appear in GTM copy?
- [ ] Document is saved in `/clients/[client-name]/` with filename `[client]_product_deep_dive.md`

---

### Phase 4: NotebookLM Handoff (5 minutes)

Send the client (or do it yourself):
1. Go to notebooklm.google.com
2. New Notebook → Upload source → upload the markdown file
3. Generate podcast (Audio Overview)
4. Listen to the podcast while doing other work — it cements the product understanding

---

## Common Problems & Fixes

**"The docs site doesn't exist"**  
Use homepage + GitHub only. Note what's missing in Open Questions so the founder knows to build it.

**"The product just pivoted"**  
Throw out anything from before the pivot. Scrape only current live product. Note the pivot context in the document intro.

**"The founder's description contradicts the website"**  
Include both, verbatim. Flag the contradiction in Open Questions. This is a positioning problem to solve in Workstream 4.

**"GitHub is private"**  
Ask the founder for: a product one-pager, any internal spec docs, or a 20-minute screen share walkthrough.

---

## Output

**File:** `[client]_product_deep_dive.md`  
**Saved to:** `/clients/[client-name]/`  
**Length:** 1,500–4,000 words  
**Format:** Markdown (for NotebookLM upload and Claude context)

---

## What Comes Next

Hand this document to Workstream 2: **gtm-competitive-research**

The competitive research analyst needs this document to know:
- What category to research
- Who to look at as competitors
- What claims to check against the market

---

*SOP-01 | SignaluX GTM Operating System | Do not modify without updating the version number*
