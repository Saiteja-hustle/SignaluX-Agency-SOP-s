# SignaluX-SOPs

**Agency:** SignaluX — B2B SaaS Performance Marketing  
**Owner:** Teja  
**Purpose:** Reusable GTM operating system for onboarding and executing marketing for any B2B SaaS client.

---

## What This Repo Is

Every client that SignaluX onboards goes through the same 7-workstream GTM process. This repo contains:

- **Skills** — Claude-callable SOPs that can be triggered in any Claude project to replicate the exact process
- **Client folders** — Client-specific work, decisions, and deliverables for reference and handoff

Anyone hired into SignaluX can open this repo, read the relevant skill, and execute the process without needing to ask Teja how it was done before.

---

## The 7 GTM Workstreams

| # | Skill | What It Produces |
|---|-------|-----------------|
| 1 | `gtm-product-deep-dive` | NotebookLM podcast source doc + product summary |
| 2 | `gtm-competitive-research` | Competitor messaging analysis + gap map |
| 3 | `gtm-icp-definition` | Locked ICP table + persona + exclusion criteria |
| 4 | `gtm-positioning-strategy` | 10 positioning angles + headline combinations |
| 5 | `gtm-landing-page-copy` | Full 12-section landing page copy (confirmed section by section) |
| 6 | `gtm-roadmap` | 8-week GTM roadmap DOCX with audit, ads, SEO, tracking |
| 7 | `gtm-outbound-sequence` | Gojiberry/Apollo sequence structure + full copy |

---

## How To Use

### Starting a new client:
1. Create a new folder under `/clients/[client-name]/`
2. Start with `gtm-product-deep-dive` — this is always workstream 1
3. Follow the sequence in order — each workstream feeds the next
4. Save all client deliverables in their client folder

### Using a skill in Claude:
Each skill folder contains a `SKILL.md`. In any Claude project, reference it by name and Claude will follow the process.

---

## Clients

| Client | Product | Status |
|--------|---------|--------|
| Aiden | AI SDLC execution layer (aiden-platform.com) | Active — GTM in progress |
| Supatest AI | AI E2E test fixing agent | Pivoted to Aiden |

---

## Folder Structure

```
SignaluX-SOPs/
├── README.md
├── skills/
│   ├── gtm-product-deep-dive/
│   │   ├── SKILL.md        ← Claude-callable
│   │   └── SOP.md          ← Human-readable SOP
│   ├── gtm-competitive-research/
│   ├── gtm-icp-definition/
│   ├── gtm-positioning-strategy/
│   ├── gtm-landing-page-copy/
│   ├── gtm-roadmap/
│   └── gtm-outbound-sequence/
└── clients/
    └── aiden/
```
