---
id: SKL-RES
title: Research with Citations
type: agent-skill
version: "1.0"
created: 2026-04-24
updated: 2026-04-24
assigned_to:
  - PRMT-AGT-002 (Research Agent)
  - PRMT-AGT-011 (PR / Links Research Agent)
  - PRMT-AGT-013 (Blog Refresh Agent)
---

# SKL-RES — Research with Citations

## Trigger

Activate this skill whenever the agent is asked to find, verify, or compile information about Cyprus regulations, tax rules, immigration procedures, property law, business setup, or any factual topic for the content pipeline.

---

## Perplexity as the Primary Search Tool

This skill uses Perplexity (via the `perplexity_research` or `perplexity_search` tool) as its primary search method. Perplexity searches the live web and returns cited results alongside an AI-generated summary.

**How to use Perplexity correctly:**

1. Run a minimum of three searches per topic: one broad (what is this process/rule), one specific (fees / timelines / exact requirements), one verification (recent changes or updates in the past 12 months)
2. Always read the cited sources in the Perplexity result — not just the summary text
3. A Perplexity summary with no cited URL is not a source — treat it as unverified and flag `[NEEDS SOURCE]`
4. Cross-reference any figure (fee, threshold, timeline) against at least one additional source before assigning `high` confidence
5. Note the publication date on every cited source — Perplexity may surface outdated pages

**Search patterns that work well:**
- `Cyprus Yellow Slip MEU1 2025 official requirements` — surfaces official and practitioner sources
- `Cyprus 60 day tax rule non-domicile 2025 current` — targets recent guidance
- `Cyprus company registration fees 2025 Registrar of Companies` — forces official-adjacent results
- Add `site:gov.cy` or `site:mof.gov.cy` when targeting a specific official domain

**What Perplexity cannot reliably verify:**
- Current CRMD processing times by office (these change without notice — flag as `low` confidence unless sourced from a dated official announcement)
- Outcomes of individual applications
- Informal practitioner practices (these require field intelligence / partner interviews, marked as `low` confidence)

---

## Source Hierarchy

Always prefer sources in this order. Do not skip to a lower-tier source if a higher-tier one exists.

| Tier | Source type | Examples |
|---|---|---|
| 1 — Primary | Official Cypriot government portals | CRMD, Cyprus Tax Department, Registrar of Companies, Land Registry |
| 2 — EU official | EU/EEA publications | European Commission, EURES |
| 3 — Professional bodies | Recognised industry associations | Cyprus Bar Association, ICPAC, CREAA |
| 4 — Named publications | Reputable legal/advisory media with named authors | Major law firm client alerts, KPMG Cyprus, Deloitte Cyprus |
| 5 — Field intelligence | Partner interview transcripts | Mark explicitly as field intelligence — not a primary source |

**Never use:** anonymous forums, Reddit, unattributed blog posts, or AI-generated summaries from unknown sources.

---

## Execution Steps

1. Identify the research objective as a single sentence before starting.
2. Search Tier 1 sources first. If the answer is there, use it and cite it. Do not continue to lower tiers for the same claim.
3. For each finding, record: the claim, the source name, the URL, and the date the source was published or last verified.
4. Assign a confidence level to every claim (see table below).
5. Flag anything that cannot be verified: write `[NEEDS SOURCE: describe what is needed]` — never fill from assumption.
6. Flag conflicting sources explicitly: `[CONFLICT: Source A says X, Source B says Y — resolve before using]`.
7. Note the date of publication for every source — not just the date of the research session.
8. For figures that change frequently (fees, processing times, tax thresholds), add: `⚠ Verify current figures — these change`.
9. For rules recently changed or under review, add: `★ Recent change — verify current position`.

---

## Confidence Levels

Every claim must carry one of these labels:

| Level | When to use |
|---|---|
| `high` | Direct quote from a current official primary source, verified within 12 months |
| `medium` | Official source older than 12 months, or reputable secondary source with named author |
| `low` | Field intelligence (practitioner observation) without official corroboration |
| `unverified` | Cannot confirm from available sources — flag for follow-up |

---

## Output Format

```
## Research Session: [TOPIC]
Date: [YYYY-MM-DD]
Objective: [one sentence]

---

## Findings

### [Sub-topic]
[Finding — written as a factual statement]
Source: [Name, URL, date published/accessed]
Confidence: [high / medium / low / unverified]

---

## Open Questions
- [What is unknown and why it matters]

---

## Recommended Next Steps
- [e.g., "Verify CRMD processing time figure against current portal"]

---

## Data Quality Note
[Completeness of this session: sources found, gaps, primary vs secondary split]
```

---

## Topic-Specific Cautions

### Immigration
- Yellow Slip (MEU1) applies to EU nationals only — confirm before citing
- Digital Nomad Visa is a distinct route — do not conflate with Category F
- Category F income thresholds must be verified — they change
- Processing times vary by CRMD office (Paphos, Limassol, Nicosia) — note which

### Tax
- Non-Dom status, 60-Day Rule, and 183-Day Rule are three separate tests — keep them distinct
- GHS (GESY) contribution: Non-Dom individuals are not automatically exempt — verify
- Corporate tax (12.5%) applies to Cyprus HE companies — substance requirements apply for treaty benefits
- IP Box rate (2.5%) is a separate regime — do not apply to all income

### Property
- Title deed delays are a known systemic issue — do not present the formal legal position as typical experience
- Stamp duty abolished January 2026 — verify current transfer fee structure
- Immovable Property Tax abolished 2017 — do not cite pre-2017 figures

### Business
- Registrar of Companies compliance and OECD substance requirements are two distinct layers
- Banking for non-EU-founded companies: present as a known difficulty, not a solved problem

---

## Anti-Patterns

- Do not invent or extrapolate fees, timescales, or thresholds
- Do not summarise without citing the source
- Do not present contested information as settled
- Do not combine rules from different years without noting the applicable year
- Do not conflate EU national and non-EU national rules — these are different processes
- Do not describe the current position if only pre-2020 sources were found (Brexit implications)

---

## Quality Check

Before handing off research output, confirm:
- [ ] Every claim has a named source and date
- [ ] Every claim has a confidence level
- [ ] No claim is filled from assumption or AI general knowledge
- [ ] All `[NEEDS SOURCE]` and `[CONFLICT]` flags are visible — none buried
- [ ] Figures that change frequently are flagged with `⚠`
- [ ] Output uses the standard session format above
