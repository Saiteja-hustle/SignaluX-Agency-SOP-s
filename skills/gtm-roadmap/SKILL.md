---
name: gtm-roadmap
description: "Use this skill to produce an 8-week GTM roadmap DOCX for a B2B SaaS client. Triggers: 'build the roadmap', '8-week plan', 'GTM plan', 'marketing plan', or Workstream 6 of the SignaluX GTM process. Requires product deep dive, ICP, and positioning to be complete. Produces a comprehensive DOCX covering current-state audit, outbound sequence, paid ads structure, SEO briefs, tracking dashboard, and weekly action checklist."
---

# GTM Skill 6: GTM Roadmap

## What This Skill Does

Produces a comprehensive 8-week GTM roadmap as a formatted DOCX that covers every channel, every week, and every metric — ready to execute without further planning.

This is not a strategy deck. It's an execution plan.

---

## Inputs Required

- Completed product deep dive
- Locked ICP + targeting config
- Approved positioning strategy + messaging hierarchy
- Current state of any existing marketing (what's running, what's been tried)
- Budget (monthly paid ads budget — in INR or USD)
- Founder's existing LinkedIn audience size and content output
- Demo booking infrastructure (Calendly/Cal.com — is it live?)

---

## Step-By-Step Process

### Step 1: Current State Audit

Before planning forward, audit what exists:

**Outbound sequence audit:**
- What sequence is live in Gojiberry/Apollo?
- Map it step by step (channel, message, timing, copy)
- Diagnose: what's broken? (wrong ICP, wrong messaging, wrong channel order)

**ICP targeting audit:**
- What filters are configured in the outbound tool?
- Do they match the locked ICP? (company size, industry, job title, stage)
- Flag every mismatch

**Landing page audit:**
- Does the current page match the locked positioning?
- Does the hero match the approved headline?

**LinkedIn content audit (if applicable):**
- What has the founder posted in the last 30 days?
- What got engagement? What got ignored?

Produce: **Audit table** with current state, diagnosis, and fix for each item.

---

### Step 2: Build The 8-Week Plan

Structure by phase:

**Weeks 1–2: Foundation**
- Fix ICP targeting in all tools
- Deploy new outbound sequence
- Publish revised landing page copy
- Set up tracking dashboard (6 core metrics)

**Weeks 3–4: First Signal**
- Outbound running — track reply rates
- Start LinkedIn content cadence (3 posts/week minimum)
- Google Ads: launch awareness campaigns for bottom-of-funnel keywords
- First demos from warm network if applicable

**Weeks 5–6: Optimize**
- Review demo data — who's showing up? Does ICP match?
- Pause what's not working. Double what is.
- Test email sequences based on outbound reply data
- First SEO content published

**Weeks 7–8: Scale**
- LinkedIn Ads launched (if budget allows)
- Second blog post published
- Outbound sequence iteration based on 6 weeks of data
- Review: are we on track for 30 demos/month?

---

### Step 3: Build Each Channel Plan

**Channel 1: LinkedIn Outbound (Gojiberry/Apollo)**

Include the full rewritten sequence (from `gtm-outbound-sequence` skill) plus:
- Sequence map (step, channel, timing, copy reference)
- ICP filter configuration (paste-ready)
- Volume targets (connections/week, DMs/week)
- Reply rate benchmarks (what counts as success)

**Channel 2: Google Ads**

Campaign structure:
```
Campaign: [Bottom-of-funnel intent]
Ad Groups:
  - [Keyword cluster 1] — e.g., "fix playwright tests"
  - [Keyword cluster 2] — e.g., "flaky cypress tests"
  - [Keyword cluster 3] — e.g., "e2e test automation"

Ad copy (3 variations per ad group):
Variation A: [Pain-led headline]
Variation B: [Solution-led headline]
Variation C: [Outcome-led headline]
```

**Channel 3: LinkedIn Ads (Phase 2)**

Targeting config:
```
Job titles: [from ICP]
Seniority: Director, VP, C-Suite
Company size: [from ICP]
Industry: Software / Internet
Format: Single image (awareness) → Lead gen form (conversion)
```

**Channel 4: Content / SEO**

Two blog briefs:
```
Post 1: [High-intent keyword] — [Estimated monthly searches]
Target: [Buyer intent: informational / transactional]
Angle: [Which positioning angle does this support?]
Outline: [5-section structure]

Post 2: [Second keyword]
[Same structure]
```

**Channel 5: Warm Network (Weeks 1-4 only)**

If founder has 1,000+ relevant LinkedIn connections:
```
Step 1: Identify 50-100 warm connections matching ICP
Step 2: Personal outreach (not sequence — personal DM)
Step 3: Ask for: intro / referral / feedback call / demo
Goal: 5–10 demos from warm network in first 30 days
```

---

### Step 4: Tracking Dashboard

6 metrics tracked weekly:

| Metric | Target | Source |
|--------|--------|--------|
| LinkedIn connections sent | [N]/week | Gojiberry |
| Connection acceptance rate | >30% | Gojiberry |
| DM reply rate | >10% | Gojiberry |
| Demo calls booked | [N]/week | Calendly |
| Demo to qualified rate | >70% | Founder |
| Cost per demo (paid) | <₹[X] | Ads platform |

Weekly review cadence: every Monday, 30 minutes, review prior week against targets.

---

### Step 5: Weekly Action Checklist

For each of the 8 weeks, produce a specific task list:

```
Week 1 Checklist:
[ ] Update Gojiberry ICP filters (company size: 20-200, title: CTO/VP Eng/EM)
[ ] Deploy new outbound sequence (DM 1 → profile visit → email cadence)
[ ] Update landing page hero copy with approved headline
[ ] Set up Calendly with 20-min "Aiden Demo" event
[ ] Configure weekly tracking spreadsheet
[ ] Send 50 connection requests (manual filter review first)
```

---

### Step 6: Compile Into DOCX

Use `docx` skill to produce a formatted DOCX with:
- Cover page with client name, date, goal (30 demos/month)
- Executive summary (1 page)
- Current state audit table
- 8-week phase plan
- Per-channel plans with copy
- Tracking dashboard
- Weekly checklists

File name: `[client]_GTM_Roadmap_8Week.docx`

---

### Step 7: Quality Check

- [ ] Every week has specific tasks (not "continue outreach")
- [ ] Tracking metrics are measurable and have specific targets
- [ ] Ad copy has at least 3 variations per ad group
- [ ] SEO briefs have keyword + search volume + angle
- [ ] Audit table has diagnosis AND fix for every item
- [ ] DOCX is formatted and readable (not a wall of text)

---

## Critical Rules

- **Execution-ready outputs only** — no "explore X" tasks. Every task must be completable by a junior hire.
- **Budget reality check** — if monthly budget is ₹1L–₹3L, don't plan 5 paid channels simultaneously
- **Demo pipeline is the only metric that matters** — every channel decision is judged by its contribution to demos booked

---

## Connected Workstreams

Requires: All of Workstreams 1–4 complete  
Runs in parallel with: `gtm-outbound-sequence` (Workstream 7)
