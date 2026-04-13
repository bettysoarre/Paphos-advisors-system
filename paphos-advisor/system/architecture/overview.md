# System Design Overview

## What We Are Building

Paphos Advisors is a Cyprus relocation advisory business. We help people and businesses relocate to Cyprus — primarily navigating immigration, tax residency, property, business formation, and settling-in processes.

The system we are building has three goals:

1. **Accumulate intelligence** that competitors do not have — field-validated, up-to-date, sourced from real practitioners
2. **Operate consistently** — so that quality does not depend on who happens to be available
3. **Build topical authority** — so that people searching for Cyprus relocation information find us

---

## The Problem This Solves

Cyprus relocation advisory is knowledge-intensive. The official guidance is often incomplete or out of date. Real-world procedures differ from what government websites say. Processing times, document requirements, and office behaviours vary. This intelligence lives in the heads of practitioners — immigration lawyers, tax advisors, property agents, relocation specialists.

Without a system:
- Knowledge walks out the door when advisors leave
- Clients get inconsistent answers depending on who they speak to
- Content quickly becomes stale and unreliable
- Partner relationships are managed informally and produce inconsistent referrals

With this system:
- Intelligence is extracted from practitioners and stored in version-controlled, confidence-rated documents
- Every team member follows the same procedures
- Content is grounded in validated knowledge and updated on a defined cadence
- Partners are onboarded consistently and referrals are tracked

---

## How the System Works

### Intelligence flows in from three sources

**Official sources** — government websites, legislation, official guidance documents. High confidence but often incomplete or slow to update.

**Field sources** — partner interviews (immigration lawyers, tax advisors, property agents, etc.) conducted via Plaud Note recordings and processed with the interview extraction prompt. Medium confidence but high practical value.

**Research sessions** — structured Perplexity Deep Research sessions using the process research prompt. Mixed confidence; used to bootstrap process documents before field validation.

### Intelligence is structured and stored

Raw inputs (transcripts, research captures) are stored in `assets/`. Structured knowledge is extracted and stored in `knowledge/` and `processes/` using the templates defined in `knowledge/_templates/` and `processes/_templates/`.

Every piece of knowledge carries:
- A **confidence level** (high / medium / low / unverified)
- A **source type** (official / field / mixed)
- A **status** (stub → draft → in-research → review → validated → published)
- **Field notes** capturing divergence from official guidance

### Intelligence surfaces to clients in two ways

**Content** — relocation guides, process explainers, FAQ pages, checklists published to the website. Governed by the content system in `content-system/`.

**Direct advice** — through cases managed in Notion. Processes documented in `processes/` underpin the advice given.

---

## Dual-Track Architecture: GitHub + Notion

| GitHub (this repo) | Notion |
|---|---|
| Source of truth | Operational frontend |
| Definitions, schemas, templates | Day-to-day work |
| Version-controlled | Team-accessible |
| Reviewed on cadence | Updated in real time |
| Pull requests for changes | Edit in place |

**The rule:** If a definition changes (taxonomy value, schema field, process status), it changes here first. Notion is then updated to match.

---

## Scalability Considerations

The system is designed for a small team now but structured to scale:

- **ICP segments** allow content and services to be tailored as the client base grows
- **Partner categories** allow the partner network to expand systematically
- **Workflow definitions** allow processes to be handed off without loss of context
- **SOPs** allow new team members to onboard without tribal knowledge transfer
- **ID registry** ensures no ID collisions as the record count grows
