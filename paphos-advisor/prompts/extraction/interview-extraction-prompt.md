---
id: PROMPT-EXT-001
title: Interview Knowledge Extraction Prompt
use_case: >
  Extract structured knowledge claims from an interview transcript with a partner,
  advisor, or subject-matter expert. Produces knowledge article drafts in the format
  defined by knowledge-article-template.md.
target_tool: Claude (claude-sonnet-4-6 or claude-opus-4-6)
created: 2026-04-07
updated: 2026-04-07
tags:
  - research
  - extraction
  - advisors
  - cyprus-wide
---

## Context

Use this prompt after conducting an interview with a partner (lawyer, accountant,
government liaison, etc.) or subject-matter expert. Feed in the raw transcript and
it will extract every processable knowledge claim — classifying each by type,
source, and confidence level.

**Before running, you need:**
- The full interview transcript (cleaned or raw)
- The name, role, and organisation of the interviewee
- The date of the interview
- A list of any existing process documents or knowledge articles relevant to the
  interviewee's area (so the model can flag contradictions)

**After running:**
- Review each extracted knowledge claim for accuracy
- Promote high-confidence claims to knowledge articles using `knowledge-article-template.md`
- Flag contradictions for follow-up research or partner clarification
- Link validated articles to the relevant process documents

---

## Objective

Extract every distinct, processable knowledge claim from an interview transcript.
For each claim: classify its type, assign a source type, assign a confidence level,
and flag any contradiction with existing documented processes. Output each claim
as a structured knowledge article draft.

---

## Instructions

Copy the prompt below, fill in all `[PLACEHOLDERS]`, and run it in Claude.
Paste the full transcript after the final instruction line.

---

```
You are a knowledge extraction specialist working for Paphos Advisors, a Cyprus relocation
advisory service. Your task is to extract every distinct, processable knowledge claim
from the interview transcript below and structure each as a draft knowledge article.

**Interviewee:** [FULL NAME]
**Role / Title:** [ROLE — e.g. "Senior Immigration Lawyer", "Certified Accountant"]
**Organisation:** [ORGANISATION NAME]
**Interview Date:** [YYYY-MM-DD]
**Topics Covered:** [BRIEF DESCRIPTION — e.g. "EU and UK national residence registration,
  MEU1 process, Yellow Slip renewal, common rejection reasons"]

**Existing process documents to check for contradictions:**
[LIST PROCESS IDs OR TITLES — e.g.
- PROC-IMM-001: EU National Residence Registration (MEU1)
- PROC-IMM-002: UK National Residence Application
Or write "None — no existing documents for this area yet"]

---

## Your Task

Read the transcript carefully. Extract every statement that represents a discrete,
processable knowledge claim — a specific fact, rule, threshold, procedure, timeline,
exception, contact detail, or practical insight relevant to Cyprus relocation processes.

Do NOT extract:
- General opinions without factual basis
- Anecdotes that do not generalise to a rule or pattern
- Off-topic conversation
- Pleasantries or filler

For each extracted claim, produce a structured knowledge article draft using the
format below. Number each article sequentially (KB-DRAFT-001, KB-DRAFT-002, etc.).

---

## Output Format for Each Knowledge Article Draft

---
id: KB-DRAFT-[###]
title: [A short, precise title for this knowledge claim]
knowledge_type: [rule | procedure | definition | threshold | exception | timeline | contact]
category: [immigration | tax | property | business | healthcare | transport | shipping | insurance | settling-in]
confidence: [high | medium | low | unverified]
source_type: [official | field | mixed]
source:
  interviewee: [INTERVIEWEE NAME]
  role: [INTERVIEWEE ROLE]
  organisation: [ORGANISATION]
  interview_date: [YYYY-MM-DD]
contradicts_existing: [true | false]
contradiction_detail: [If true, state which process document or knowledge article this contradicts and how. If false, write "None."]
requires_verification: [true | false]
verification_note: [If true, state what needs to be verified against an official source. If false, write "N/A."]
---

### Extracted Claim
[Quote or close paraphrase of exactly what the interviewee said. Preserve their words
as closely as possible. Do not interpret or editorialise here.]

### Summary
[2–3 sentence plain-language summary of the knowledge this claim represents.]

### Detail
[Full structured explanation of the claim. If it is a rule, state it precisely.
If it is a procedure, list the steps. If it is a threshold, state the exact figure
and what it applies to. Include any conditions, qualifiers, or exceptions the
interviewee mentioned.]

### Confidence Rationale
[Explain why you assigned this confidence level. Refer to the criteria below:
- High: interviewee is a qualified expert with direct, current experience; claim
  is specific, consistent, and likely verifiable against official sources.
- Medium: interviewee has relevant experience but claim is anecdotal, may vary by
  case, or refers to past practice that may have changed.
- Low: claim is vague, second-hand, hedged by the interviewee, or contradicts
  other sources.
- Unverified: claim requires official source verification before it can be used.]

### Caveats
[Any limitations, exceptions, or conditions the interviewee attached to this claim.
If none, write "None stated."]

### Recommended Next Action
[One of:
- "Promote to knowledge article — sufficient confidence, no verification needed."
- "Verify against [specific official source] before promoting."
- "Flag for follow-up with interviewee — claim needs clarification."
- "Cross-reference with [process document ID] — potential contradiction."
- "Hold — insufficient detail to produce a usable knowledge article."]

---

Now extract all knowledge claims from the following transcript:

[PASTE FULL TRANSCRIPT HERE]
```

---

## Output Format

The model will return a numbered sequence of knowledge article drafts — one per
extracted claim. A typical 45-minute interview with a specialist will yield
between 15 and 40 draft articles.

**After receiving the output:**

1. Review each draft for accuracy. Correct any misinterpretations of the interviewee's words.
2. For each draft where `requires_verification: true`, run verification before promoting.
3. For each draft where `contradicts_existing: true`, investigate the contradiction before promoting.
4. Promote approved drafts to full knowledge articles using `knowledge-article-template.md`.
   Replace the `KB-DRAFT-###` ID with the correct `KB-[AREA]-[###]` ID from `id-registry.md`.
5. Link each new knowledge article to the relevant process documents.
6. Update `id-registry.md` to reflect the new sequence numbers used.

---

## Example Output

Below is an example of a single extracted knowledge article draft, showing the
expected format and level of detail.

---

```
---
id: KB-DRAFT-001
title: MEU1 Processing Time at Paphos District Office — Current Real-World Average
knowledge_type: timeline
category: immigration
confidence: medium
source_type: field
source:
  interviewee: Andreas Papadopoulos
  role: Senior Immigration Lawyer
  organisation: Papadopoulos & Associates LLC
  interview_date: 2026-03-15
contradicts_existing: true
contradiction_detail: >
  PROC-IMM-001 currently states a processing time of 2–3 months based on official
  guidance. The interviewee reports a consistent real-world average of 4–6 months
  at Paphos district office as of early 2026, which contradicts the documented figure.
requires_verification: false
verification_note: N/A
---

### Extracted Claim
"In Paphos, realistically you're waiting four to six months right now. I had a client
submit a complete MEU1 in October and they only got their Yellow Slip in February.
The office is understaffed. The two to three months they quote officially — I haven't
seen that in at least two years."

### Summary
Real-world MEU1 processing times at Paphos district office are currently running at
4–6 months, significantly longer than the 2–3 months stated in official guidance.
The interviewee attributes this to chronic understaffing at the Paphos office.

### Detail
As of Q1 2026, the Paphos Civil Registry and Migration Department office is processing
MEU1 (Yellow Slip) applications in approximately 4–6 months from submission of a
complete application. The official stated timeframe of 2–3 months does not reflect
current operational reality. The interviewee cited a specific client case: submission
in October 2025, Yellow Slip received February 2026 (approximately 4 months). The
interviewee stated this is consistent with their recent caseload and attributes the
delay to understaffing, not application complexity.

Note: This timeline applies to Paphos district office specifically. Processing times
may differ at other district offices (Limassol, Nicosia, Larnaca).

### Confidence Rationale
Medium. The interviewee is a practicing immigration lawyer with active Paphos caseload,
providing a specific recent example. However, this is field experience from a single
practitioner and has not been cross-checked against other lawyers or client reports.
Processing times can also fluctuate — this reflects early 2026 conditions.

### Caveats
- Applies to Paphos district office only. Other offices not addressed.
- Reflects early 2026 conditions. May improve or worsen.
- Assumes complete, correct application submitted at first attempt.

### Recommended Next Action
Cross-reference with PROC-IMM-001 — potential contradiction. Update the Processing Time
section of PROC-IMM-001 to distinguish between official stated timeframe and Paphos
field reality. Flag for verification with a second Paphos-based practitioner.
```
