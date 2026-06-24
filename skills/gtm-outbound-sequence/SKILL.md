---
name: gtm-outbound-sequence
description: "Use this skill to design and write outbound sequences for B2B SaaS clients using Gojiberry, Apollo, or similar tools. Triggers: 'write the outbound sequence', 'LinkedIn DM sequence', 'cold email sequence', 'Gojiberry sequence', or Workstream 7 of the SignaluX GTM process. Requires locked ICP and approved positioning. Produces a complete sequence map plus full copy for every touchpoint."
---

# GTM Skill 7: Outbound Sequence

## What This Skill Does

Produces a complete, deploy-ready outbound sequence including:
1. Sequence architecture (steps, channels, timing)
2. Full copy for every touchpoint (LinkedIn DMs + emails)
3. Tone and voice guidelines for the sender's personality
4. Gojiberry/Apollo configuration notes

---

## Inputs Required

- Locked ICP (who we're reaching)
- Approved positioning + messaging hierarchy (what angle we're using)
- Sender profile (whose LinkedIn/email is this coming from — name, role, personality)
- Tool being used (Gojiberry / Apollo / HubSpot sequences)
- Tool constraints (does it support branching? Max steps? DM vs email availability?)

---

## Step-By-Step Process

### Step 1: Define Sender Voice

The outbound copy must sound like a specific human, not a marketing team.

Answer these before writing a single word:
- Who is the sender? (Name, title, what they actually do day-to-day)
- What is their natural communication style? (Formal? Direct? Dry humor? Self-aware?)
- What would they never say? (Corporate-speak? Overly casual? Emojis?)
- What do they genuinely care about that the ICP also cares about? (The connection point)

Produce a **Sender Voice Card:**
```
Sender: [Name]
Role: [Title at company]
Voice: [3 adjectives]
Sounds like: [One reference — a real person, a writing style, an archetype]
Never says: [3 phrases they'd never use]
Genuine interest: [What do they actually care about that connects to the ICP's world?]
```

This card governs all copy in the sequence.

---

### Step 2: Design The Sequence Architecture

**For Gojiberry (linear only — no true branching):**

Default 8-step structure:
```
Step 1: Send LinkedIn connection request (no note, or short note — test both)
Step 2: LinkedIn DM 1 (+1 day after acceptance) — PATTERN INTERRUPT ONLY
Step 3: Profile visit (0 days — automated, shows up in their notifications)
Step 4: Email 1 (+3 days) — First pitch touchpoint
Step 5: LinkedIn DM 2 (+4 days) — Short follow-up, different angle
Step 6: Email 2 (+4 days) — Case study / proof angle
Step 7: LinkedIn DM 3 (+3 days) — Direct ask
Step 8: Email 3 (+4 days) — Break-up email
```

Total duration: ~22-23 days  
Touchpoints: 3 LinkedIn DMs + 3 emails + 1 profile visit

**If tool supports branching (Apollo):**
- Add branch after DM 1: if replied → exit sequence, enter manual follow-up
- Add branch after Email 1: if opened but no reply → send Email 1b with different subject

---

### Step 3: Write Each Touchpoint

**CRITICAL RULE FOR DM 1:**

DM 1 is a pattern interrupt. It must NOT:
- Pitch the product
- Include a Calendly link
- Ask about their tech stack or pain points
- Sound like it was written by a marketing team
- Use niche-specific "hooks" that feel researched and therefore fake

DM 1 MUST:
- Read as a real human reaching out
- Have a distinct personality (using the Sender Voice Card)
- Create curiosity or warmth without obligation
- Be short (3–4 sentences maximum)
- Make the recipient feel like they're talking to a person, not a sequence

**Test: Would the recipient show this DM to a colleague and say "this felt human"? If yes, it's right.**

---

**Copy templates by touchpoint:**

**DM 1 — Pattern Interrupt**
```
[Specific reference to something they actually did/said/built — not generic]
[One sentence about sender that creates a connection point — not a pitch]
[One low-stakes question or observation — NOT "do you have 15 minutes?"]
```

**Email 1 — First Pitch**
```
Subject: [Specific, non-clickbait — references their actual situation]

[1 sentence: why you're reaching out — their specific context]
[2-3 sentences: the problem in their language]
[2-3 sentences: what [product] does — positioning angle, not feature list]
[1 sentence CTA: soft ask — "worth a quick look?" not "book a demo now"]

[Sender name]
[Title]
```

**DM 2 — Short Follow-Up**
```
[Acknowledge the silence without being passive-aggressive]
[One new angle or piece of context — don't repeat DM 1]
[Same low-stakes energy]
```

**Email 2 — Proof Angle**
```
Subject: [Reference a specific outcome or customer]

[1 sentence: quick follow-up framing]
[1-2 sentences: specific proof — customer story, metric, outcome]
[1 sentence: connect proof to their situation]
[Soft CTA]
```

**DM 3 — Direct Ask**
```
[Acknowledge this is follow-up #3]
[One direct ask — be honest about what you want]
[Give them an easy out — "if now's not the time, no worries"]
```

**Email 3 — Break-Up**
```
Subject: "Closing the loop"

[Short: I'm going to stop reaching out]
[One last hook — the most compelling thing you have]
[Open door: "if this ever becomes relevant..."]
```

---

### Step 4: Peer Review The Copy

Before finalizing, check each touchpoint against:

**The "real human" test:** Read it out loud in the sender's voice. Does it sound like them?  
**The "pitch detector" test:** Does DM 1 contain any product information? If yes, cut it.  
**The "pattern" test:** Do all the DMs sound like slight variations of each other? If yes, rewrite.  
**The "CTA pressure" test:** Is there a Calendly link or "book a call" in DM 1 or DM 2? If yes, remove it.

---

### Step 5: Compile Gojiberry Configuration Notes

```
Sequence name: [Client] — [ICP target] — [Date]
Steps:
1. Connection request — [note/no note]
2. DM: [DM 1 text — paste ready]
3. Profile visit — [0 day delay]
4. Email: Subject: [X] / Body: [Email 1 text]
5. DM: [DM 2 text]
6. Email: Subject: [X] / Body: [Email 2 text]
7. DM: [DM 3 text]
8. Email: Subject: [X] / Body: [Email 3 text]

Daily send limits: [N connections/day, N DMs/day]
ICP filter: [Paste targeting config from ICP workstream]
```

---

### Step 6: Quality Check

- [ ] DM 1 contains zero product pitch
- [ ] DM 1 has no Calendly link or meeting ask
- [ ] Every touchpoint sounds like the sender (check against voice card)
- [ ] No two touchpoints use the same hook or angle
- [ ] Email subjects are specific — not clickbait, not generic
- [ ] Break-up email is genuinely closing the loop (not a fake break-up with a hidden ask)
- [ ] Gojiberry config notes are paste-ready

---

## Critical Rules

- **DM 1 = pattern interrupt only** — this is the most important rule in this entire skill
- **Sender voice overrides messaging hierarchy** — the copy must sound like the sender, not like the brand
- **No Calendly in the first two touchpoints** — earn the right to ask for time first
- **Gimmicks don't work** — niche-specific clever hooks that feel researched land as fake. Disarming and human beats clever every time.

---

## Connected Workstreams

Requires: `gtm-icp-definition` and `gtm-positioning-strategy` complete  
Runs in parallel with: `gtm-roadmap` (Workstream 6)

The outbound sequence is one of the primary channels in the roadmap — they are designed together.
