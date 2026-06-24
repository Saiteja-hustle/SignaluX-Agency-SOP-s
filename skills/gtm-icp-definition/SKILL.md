---
name: gtm-icp-definition
description: "Use this skill to define and lock the Ideal Customer Profile for a B2B SaaS client. Triggers: 'define the ICP', 'who should we target', 'lock the ICP', 'build the persona', or when starting Workstream 3 of the SignaluX GTM process. Requires gtm-product-deep-dive and gtm-competitive-research to be complete. Output is a locked ICP table, buyer persona, exclusion criteria, and targeting configuration."
---

# GTM Skill 3: ICP Definition

## What This Skill Does

Produces a locked, specific ICP that answers:
- Exactly who to target (job title, seniority, company type, stage, size)
- What pain they experience (in their words, not product words)
- What they care about most (their KPIs and success metrics)
- Who to explicitly exclude (prevents wasted outreach spend)
- How to configure targeting in LinkedIn Ads / Gojiberry / Apollo

This ICP locks before any copy or campaign work begins.

---

## Inputs Required

- Completed product deep dive document
- Completed competitive research document
- Founder interview answers (see Step 1)
- Any existing customer data (even 1-2 customers reveals ICP signals)

---

## Step-By-Step Process

### Step 1: Founder ICP Interview

Ask the founder these exact questions (async or on a call):

```
1. Who was your first paying customer? Describe their role, company, team size.
2. Which of your current customers gets the most value? What's different about them?
3. Who have you lost deals to competitors with? What was different about them?
4. When a CTO says yes to you on a sales call — what problem did they describe before they bought?
5. Who should we NOT target? Who's bought from you and been a bad fit?
6. What company stage/size has been the best fit so far?
```

Do NOT skip this step. Founder sales call experience is more reliable than any desk research.

---

### Step 2: Layer In Product + Competitive Signals

From the product deep dive:
- What integrations signal ICP? (e.g., supports Playwright/Cypress → teams already doing E2E testing)
- What setup complexity signals? (complex setup → larger, more technical teams)
- What pricing signals? (self-serve → SMB; enterprise pricing → mid-market+)

From competitive research:
- Who are competitors targeting? (validated category)
- What company size/stage language appears in competitor copy?
- What buyer titles appear in competitor social proof?

---

### Step 3: Build The ICP Table

```markdown
## ICP — [Client Name]
Locked: [date]

### Primary ICP

| Parameter | Definition | Notes |
|-----------|-----------|-------|
| Company type | B2B SaaS | Software sold to other businesses |
| Geography | US primary, UK secondary | English-speaking globally |
| Stage | Series A–B | $2M–$30M ARR |
| Engineering team size | 20–200 engineers | Large enough to have CI/CD; small enough to not have dedicated QA |
| Decision maker title | CTO / VP Engineering / Engineering Manager | Who owns the problem |
| Decision maker context | Managing managers, not writing code | Cares about velocity metrics, not syntax |
| Primary KPI | Engineering velocity / shipping speed | Their #1 job metric |
| Pain signal | [specific symptom in their words] | What they complain about |
| Budget signal | Already paying for [category tools] | Signals willingness to pay for dev tooling |
| Framework signal | Already using [specific frameworks] | Product compatibility signal |

### Secondary ICP (if applicable)
[Repeat table for secondary buyer if meaningful]

### Explicit Exclusions

Do NOT target:
- [Exclusion 1 + reason]
- [Exclusion 2 + reason]
- [Exclusion 3 + reason]

### Buyer Persona — Primary

**Name:** [Archetype name, e.g., "The Velocity CTO"]  
**Title:** CTO at Series B B2B SaaS  
**Team size:** 40 engineers across 4 squads  
**Day-to-day:** In strategy and planning meetings, not writing code. Reviews PRs occasionally to stay sharp.  
**Primary pressure:** Board and investors are tracking velocity metrics. Every sprint delay is a conversation.  
**Relationship with testing:** Knows it's important. Doesn't have time to manage it. Inherited a messy test suite.  
**Current behavior:** [What are they doing today to cope with the pain?]  
**Trigger for buying:** [What makes them start looking for a solution?]  
**Objections:** [Top 2-3 things that make them hesitate]  
**What winning looks like for them:** [Their definition of success after buying]
```

---

### Step 4: Translate ICP Into Targeting Configuration

**For LinkedIn Ads:**
```
Job titles: [list exact titles]
Seniority: [Director / VP / C-Suite]
Company size: [employee range]
Industry: [Software / Internet / SaaS]
Skills (optional): [relevant technical skills]
Exclude: [company sizes, industries, job functions to exclude]
```

**For Gojiberry / Apollo outbound:**
```
Title filter: [exact title strings]
Company type: B2B SaaS
Employee count: [range]
Technology used: [if detectable — e.g., "uses GitHub Actions"]
Funding stage: Series A–B
Location: United States, United Kingdom
Exclude: [specific industries, company sizes, or signals]
```

---

### Step 5: Validate With Founder Before Locking

Send the completed ICP table to the founder:
- "Does this match who you're seeing buy?"
- "Is there anything here that doesn't feel right?"
- "Are there any exclusions we're missing?"

Get explicit sign-off before proceeding to positioning.

---

### Step 6: Quality Check

- [ ] ICP has exact ranges (not "mid-size companies" — specific employee counts)
- [ ] Exclusions are specific with reasons (not just "bad fit")
- [ ] Buyer persona answers: what they care about, what triggers a buy, what their objections are
- [ ] Targeting config is ready to paste into LinkedIn Ads or Apollo
- [ ] Founder has reviewed and signed off

---

## Critical Rules

- **Lock the ICP before writing any copy** — copy written for a vague audience is copy that works for no one
- **ICP is a hypothesis until validated by sales data** — revisit after 30 demos
- **One primary ICP** — don't try to target 3 different ICPs simultaneously at the start
- **Exclusions matter as much as inclusions** — knowing who NOT to target saves significant spend

---

## Connected Workstreams

Feeds into: `gtm-positioning-strategy` (Workstream 4), `gtm-outbound-sequence` (Workstream 7)

The ICP is the audience filter that every downstream workstream writes for.
