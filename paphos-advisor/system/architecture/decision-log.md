# Architecture Decision Log

Decisions that shaped the system design. Format: context → decision → rationale → consequences.

---

## ADR-001 — GitHub as source of truth, not Notion

**Date:** 2026-04-13
**Status:** Accepted

**Context:** The system needed a canonical home for process documentation, schemas, templates, and governance rules. Notion was the obvious operational tool, but it lacks version control, structured review workflows, and the ability to enforce naming conventions.

**Decision:** GitHub holds all canonical definitions. Notion is the operational frontend built on top of those definitions.

**Rationale:**
- Version control allows us to see what changed, when, and why
- Pull-based collaboration means teammates always have the latest definitions
- Markdown files in GitHub can be reviewed with diffs; Notion edits cannot
- If Notion is replaced, the definitions survive

**Consequences:**
- Team members need basic git literacy (clone, pull, push)
- Schema changes require a two-step process: update GitHub first, then update Notion
- Notion databases must be kept in sync with GitHub schemas manually (until MCP automation is in place)

---

## ADR-002 — Confidence levels as a first-class field on all knowledge records

**Date:** 2026-04-13
**Status:** Accepted

**Context:** Cyprus administrative processes frequently diverge between official guidance and real-world practice. Presenting unverified or low-confidence information to clients as fact is a reputational and liability risk.

**Decision:** Every knowledge record and process document carries an explicit confidence level (high / medium / low / unverified) defined in `system/taxonomies/confidence-levels.yaml`.

**Rationale:**
- Makes the quality of information visible to the team before it reaches clients
- Forces explicit validation decisions rather than implicit assumptions
- Allows content to be published with appropriate caveats when confidence is lower

**Consequences:**
- All process templates and knowledge templates must include the `confidence` field
- Content published from low/medium confidence sources must include disclaimers
- Review cadences are partly driven by confidence level (lower confidence = more frequent review)

---

## ADR-003 — Partner interviews as the primary field intelligence source

**Date:** 2026-04-13
**Status:** Accepted

**Context:** Official sources alone are insufficient for Cyprus processes. Real-world procedures, processing times, office behaviours, and document requirements are known by practitioners, not published by government.

**Decision:** Structured partner interviews (recorded via Plaud Note, extracted via Claude) are the primary mechanism for acquiring field intelligence.

**Rationale:**
- Partners (immigration lawyers, tax advisors, property agents) handle these processes daily
- A single 60-minute interview can yield months of research value
- Structured extraction (using PRMT-EXT-001) produces consistent, comparable KB articles
- Partners benefit from the relationship, making interviews achievable

**Consequences:**
- Partner onboarding must include a knowledge interview (Stage 4 of the onboarding checklist)
- Knowledge extracted from interviews is attributed to the partner category (not individually, to protect partner privacy)
- Field intelligence has medium confidence by default; it can be elevated to high when corroborated by multiple partners or official sources

---

## ADR-004 — ICP segmentation drives content and service design

**Date:** 2026-04-13
**Status:** Accepted

**Context:** Cyprus relocators are not a homogeneous group. UK retirees, EU remote workers, non-EU digital nomads, and HNI permanent residency seekers have very different process needs, timelines, budgets, and questions.

**Decision:** All content and service design is anchored to defined ICP segments (`icps/segments/`). Every content brief, process doc, and partner referral should reference the relevant ICP(s).

**Rationale:**
- Generic content ranks poorly and converts poorly
- Segment-specific content answers real questions that real people are searching for
- ICP tagging allows us to analyse which segments generate the most cases and revenue over time

**Consequences:**
- ICP segments must be defined before content planning begins in earnest
- Content Pipeline in Notion includes an ICP field (to be added once the ICPs database exists)
- Topical map is structured around ICP needs, not just topic areas

---

## ADR-005 — Topical map as a single combined file initially, to be split by pillar as content scales

**Date:** 2026-04-13
**Status:** Accepted

**Context:** The architecture spec calls for one file per pillar topic. At system launch, content production has not yet begun and the full pillar structure is not yet operationally validated.

**Decision:** Start with a combined `pillar-topics.md` summarising all 6 pillars and 49 supporting ideas. Split into individual pillar files as content production begins and each pillar grows in complexity.

**Rationale:**
- A single file is easier to review and update while the content strategy is being formed
- Splitting prematurely creates 6 files with minimal content each
- The split can be done once each pillar has enough cluster content to justify it

**Consequences:**
- When splitting, each pillar file should follow the structure defined in the topical map overview
- The combined `pillar-topics.md` should be archived (not deleted) when the split is done
- CHANGELOG should record the split when it happens
