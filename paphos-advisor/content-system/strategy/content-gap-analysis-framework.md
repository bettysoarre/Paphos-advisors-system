# Content Gap Analysis Framework

## Purpose
Defines how to identify content gaps — topics we should cover but do not yet — and prioritise which gaps to fill first.

---

## Gap Types

**Type 1 — Search gap:** A topic that people are actively searching for, that we do not yet cover.
*How to find:* Keyword research (Ahrefs, Google Search Console, Google autocomplete, "People Also Ask").

**Type 2 — ICP gap:** A question that a specific ICP segment needs answered, that we do not cover.
*How to find:* Client intake questions, case notes, partner feedback.

**Type 3 — Process gap:** A process we advise on that does not have corresponding content.
*How to find:* Review `processes/` — any process without a `published_date` is a potential content gap.

**Type 4 — Topical authority gap:** A topic that a competitor covers comprehensively that we do not, creating a gap in our topical cluster.
*How to find:* Review `content-system/topical-map/` and compare against top-ranking competitor content.

---

## Gap Scoring

Score each identified gap on three dimensions (1-3 each):

| Dimension | Score 1 | Score 2 | Score 3 |
|---|---|---|---|
| **Demand** | Low search volume / rare client question | Moderate | High search volume / frequent client question |
| **ICP relevance** | Applies to low-priority ICP | Applies to mid-priority ICP | Applies to top-priority ICP(s) |
| **Knowledge readiness** | No source material exists | Draft process doc or KB articles exist | Validated process doc + KB articles ready |

**Total score 7-9:** High priority — add to Content Pipeline immediately
**Total score 4-6:** Medium priority — add to pipeline, schedule for next quarter
**Total score 3:** Low priority — log and revisit in 6 months

---

## Gap Analysis Process

### Step 1 — Quarterly audit
Every quarter, run through each topic area in the topical map and ask:
- What are the top 10 search queries in this pillar area that we do not cover?
- What questions have clients asked in the last quarter that we could not point to content for?
- What has a competitor ranked for that we do not have content for?

### Step 2 — Score each gap
Apply the scoring model above.

### Step 3 — Check knowledge readiness
For high-priority gaps:
- Does a process doc exist and is it `validated` or better?
- Are there KB articles supporting the topic?
- If not: add a research task to the Research Log before creating a content brief

### Step 4 — Add to Content Pipeline
For gaps that score ≥ 7 and have knowledge readiness ≥ 2:
- Create a content brief in Notion
- Set priority
- Assign

### Step 5 — Log gaps awaiting knowledge
For gaps that score ≥ 7 but have knowledge readiness = 1:
- Add to the Content Pipeline as `blocked — awaiting research`
- Create a corresponding Research Log entry
- Link the two records in Notion

---

## Anti-Patterns to Avoid

**Writing thin content to fill gaps:** If the knowledge is not there to support a 2,000-word authoritative guide, do not write a shallow 500-word version. It will rank poorly and undermine trust. Wait until the knowledge is ready.

**Cannibalising existing content:** Before creating a new piece, search existing content to ensure you are not duplicating an angle already covered. See `content-system/rules/internal-linking-rules.md` for anti-cannibalisation rules.

**Chasing volume over relevance:** A high-volume keyword that does not map to any of our ICP segments is not worth pursuing. Our content must attract people who will become clients.
