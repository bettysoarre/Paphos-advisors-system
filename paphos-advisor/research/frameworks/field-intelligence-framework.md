---
id: RES-FRM-003
title: Field Intelligence Framework
type: framework
version: "1.0"
created: 2026-04-13
updated: 2026-04-13
applies_to: Partner knowledge extraction, client case observations, practitioner insights
linked_sops: [SOP-RES-001, SOP-RES-003, SOP-RES-004]
linked_prompts: [PRMT-EXT-001, PRMT-EXT-003]
---

# Field Intelligence Framework (RES-FRM-003)

## Purpose
Defines what field intelligence is, where it comes from, how it is captured, and how it is classified and used within the Paphos Advisors knowledge system. Field intelligence is the practitioner layer of knowledge that sits between official rules and real-world experience.

---

## What Is Field Intelligence?

Field intelligence is knowledge derived from:
- Direct practitioner experience (what actually happens vs. what the rules say)
- Partner observations (how CRMD staff behave, what documents they accept or reject in practice)
- Client case outcomes (what worked, what failed, what surprised us)
- Community-sourced intelligence (expat groups, advisory forums — lower confidence)

Field intelligence does **not** replace official guidance. It supplements it by capturing:
- Divergence between official rules and current practice
- Informal norms (what CRMD offices actually request vs. their published list)
- Timing intelligence (real-world wait times vs. official figures)
- Qualitative nuance (which advisors are effective, what tone to take with which office)

---

## Sources of Field Intelligence

### Source Tier 1 — Partner Interviews (highest quality)
Structured interviews with vetted professional partners (immigration lawyers, tax advisors, property agents) conducted via Plaud Note and transcribed.

**Why high quality:** Professional accountability; partners stake their reputation on accuracy; they have current, practice-based knowledge.

**How captured:** Partner onboarding interview (PRMT-EXT-001) + ongoing check-ins.

**Confidence output:** low–medium (field intelligence, but from accountable professionals)

### Source Tier 2 — Case Observations (medium quality)
Observations made during active client cases: what documents were requested, what processing time was experienced, what outcome was reached.

**Why medium quality:** Sample size is small initially; individual cases may not be representative.

**How captured:** Case closure notes in Notion; advisor observations logged during case lifecycle.

**Confidence output:** low (until corroborated by multiple cases)

### Source Tier 3 — Advisor Network Intelligence (medium quality)
Informal knowledge gathered from Cyprus-focused advisory communities, accountant and lawyer networks, or expatriate community managers.

**Why medium quality:** Sources are experienced but may not be directly accountable; information is unattributed.

**How captured:** Research notes during PROMPT-RES-001 / PROMPT-RES-002 sessions.

**Confidence output:** low

### Source Tier 4 — Community Intelligence (lower quality)
Information from expatriate Facebook groups, Reddit communities, Quora answers, travel forums.

**Why lower quality:** Unattributed, anecdotal, may be outdated or jurisdiction-confused.

**How captured:** Only when corroborating other intelligence — never used as a standalone source.

**Confidence output:** unverified (requires partner corroboration before use)

---

## Classification of Field Intelligence Claims

When a field intelligence claim is captured, it must be classified as one of:

### Type A — Confirmed Divergence
Official rule says X, but field intelligence from Tier 1 or Tier 2 sources consistently shows Y.

**Example:** CRMD's published document list does not include apostilled bank statements, but partners report they are consistently requested for Yellow Slip applications.

**Action:** Document both positions. Note the divergence. Add to KB as a field knowledge article (KB-FLD-NNN). Flag the official process document.

### Type B — Timing Intelligence
Official guidance quotes processing time X; real-world experience is Y.

**Example:** Yellow Slip applications listed as 30 days on CRMD website; partner reports current average is 8–12 weeks at Paphos office.

**Action:** Note both figures. Mark real-world figure as field intelligence with date. Flag for monitoring.

### Type C — Practical Nuance
The rule is as stated, but there are practical implications the official source does not mention.

**Example:** The official document list is accurate, but the documents must be presented in a specific order or the application is delayed.

**Action:** Document the nuance in the process document under "Practical Notes". Attribute to field intelligence.

### Type D — Unverified Claim
A claim that has not been corroborated by Tier 1 or Tier 2 sources.

**Action:** Do not include in process docs or published content. Log as unverified. Schedule for verification.

---

## Capture Standards

### During Partner Interviews
1. Use Plaud Note for transcription
2. Save transcript to `assets/partner-interviews/` per SOP-RES-001 naming convention
3. Run PRMT-EXT-001 to extract structured intelligence
4. Classify each claim (A/B/C/D)
5. Create KB-FLD-NNN articles for Type A and B claims
6. Update process documents with Type C nuances
7. Log Type D claims for follow-up

### During Case Work
1. Advisor notes any discrepancy between our process documentation and what they observed
2. Log in Notion case record under "Process Observations"
3. If discrepancy is significant: flag for research team review
4. After 3+ cases show the same pattern: elevate to Type A or B intelligence and update documentation

### During Research Sessions
1. Use PROMPT-RES-001 or PROMPT-RES-003 when field intelligence is referenced
2. Classify the claim before logging
3. Do not mix official-source content and field intelligence in the same KB article without explicit labelling

---

## Use in Documentation

### When field intelligence may be used in process documents
- To supplement (not replace) official guidance
- To add a "Practical Notes" section
- To provide realistic timelines alongside official ones
- To warn of known difficulties or rejections

### When field intelligence must NOT be used
- As the sole basis for a process step
- In place of confirmed official guidance that contradicts it (unless the official guidance is demonstrably out of date)
- In published content without appropriate hedging language
- For investment or legal thresholds (fees, income requirements) — these must come from official sources

### Labelling in documents
Field intelligence must always be clearly labelled:

> **Field Intelligence (as of [date]):** [claim]. Source: [partner category or case observation]. Confidence: low. Verify against current official guidance before advising.

---

## Cadence and Decay

Field intelligence has a shorter shelf life than official guidance because practice changes even when rules do not.

| Intelligence Type | Revalidation cadence |
|---|---|
| CRMD processing times | Every 3 months |
| Document checklist nuances | Every 6 months |
| Informal office practices | Every 6 months (or after next partner review) |
| Partner capacity and service quality | Per partner annual review (SOP-PAR-003) |
| Community intelligence | Every 3 months (highest decay) |

When field intelligence reaches its revalidation date, it is not automatically retired — it is flagged for verification. If the partner or case data confirms it still holds, the date is updated. If it cannot be confirmed, confidence is downgraded to `unverified`.
