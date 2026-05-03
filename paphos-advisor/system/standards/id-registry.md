# ID Registry

Master registry of all ID prefixes, area/type codes, and current sequence numbers in the Paphos Advisor system.

**Rule:** Before creating any new record, check this registry, use the next available sequence number, then update this file to reflect the new current sequence.

**Format:** `[PREFIX]-[CODE]-[###]` — all uppercase, sequence zero-padded to 3 digits.

---

## Process IDs — `PROC`

| Area | Code | Current Sequence | Next ID to Use |
|------|------|-----------------|----------------|
| Immigration | IMM | 010 | PROC-IMM-011 |
| Tax | TAX | 000 | PROC-TAX-PROC-001 |
| Property | PROP | 002 | PROC-PROP-003 |
| Business | BIZ | 001 | PROC-BIZ-002 |
| Healthcare | HLTH | 003 | PROC-HLTH-004 |
| Transport | TRN | 002 | PROC-TRN-003 |
| Shipping | SHIP | 000 | PROC-SHIP-001 |
| Insurance | INS | 000 | PROC-INS-001 |
| Settling-In | SET | 005 | PROC-SET-006 |

---

## SOP IDs — `SOP`

| Area | Code | Current Sequence | Next ID to Use |
|------|------|-----------------|----------------|
| Content | CNT | 000 | SOP-CNT-001 |
| Partners | PRTN | 000 | SOP-PRTN-001 |
| Cases | CASE | 000 | SOP-CASE-001 |
| Research | RES | 000 | SOP-RES-001 |
| Knowledge | KB | 000 | SOP-KB-001 |
| Operations | OPS | 000 | SOP-OPS-001 |

---

## ICP Segment IDs — `ICP-SEG`

Ideal Customer Profile segment definitions. One record per distinct segment.

| Segment | Code | Current Sequence | Next ID to Use |
|---------|------|-----------------|----------------|
| Segments | SEG | 006 | ICP-SEG-007 |

---

## Decision Tree IDs — `DT`

Routing and eligibility decision trees. Domain codes match the process area.

| Domain | Code | Current Sequence | Next ID to Use |
|--------|------|-----------------|----------------|
| Residency / Immigration | RES | 001 | DT-RES-002 |
| Tax | TAX | 001 | DT-TAX-002 |
| Property | PROP | 000 | DT-PROP-001 |
| Business | BIZ | 000 | DT-BIZ-001 |
| Healthcare | HLTH | 000 | DT-HLTH-001 |
| Settling In | SET | 000 | DT-SET-001 |

---

## Field Intelligence Article IDs — `KA-FLD`

Location-specific and office-specific practical notes. Domain-agnostic — all field intelligence articles share the `FLD` code, organised by sequence.

| Type | Code | Current Sequence | Next ID to Use |
|------|------|-----------------|----------------|
| Field Intelligence | FLD | 019 | KA-FLD-020 |

---

## Knowledge Article IDs — `KB`

| Area | Code | Current Sequence | Next ID to Use |
|------|------|-----------------|----------------|
| Immigration | IMM | 000 | KB-IMM-001 |
| Tax | TAX | 000 | KB-TAX-PROC-001 |
| Property | PROP | 000 | KB-PROP-001 |
| Business | BIZ | 000 | KB-BIZ-001 |
| Healthcare | HLTH | 000 | KB-HLTH-001 |
| Transport | TRN | 000 | KB-TRN-001 |
| Shipping | SHIP | 000 | KB-SHIP-001 |
| Insurance | INS | 000 | KB-INS-001 |
| Settling-In | SET | 000 | KB-SET-001 |

---

## Content IDs — `CNT`

| Content Type | Code | Current Sequence | Next ID to Use |
|-------------|------|-----------------|----------------|
| Guide | GDE | 003 | CNT-GDE-004 |
| FAQ | FAQ | 000 | CNT-FAQ-001 |
| Checklist | CHK | 000 | CNT-CHK-001 |
| Comparison | CMP | 001 | CNT-CMP-002 |
| Partner Page | PRTN | 000 | CNT-PRTN-001 |
| Service Page | SVC | 000 | CNT-SVC-001 |
| Email Sequence | EMAIL | 000 | CNT-EMAIL-001 |
| Social Post | SOC | 000 | CNT-SOC-001 |
| Video Script | VID | 000 | CNT-VID-001 |
| Lead Magnet | LM | 000 | CNT-LM-001 |
| Landing Page | LP | 000 | CNT-LP-001 |
| Blog Post | BLOG | 000 | CNT-BLOG-001 |
| Lifestyle | LIFE | 000 | CNT-LIFE-001 |

---

## Content Brief IDs — `BRIEF`

| Content Type | Code | Current Sequence | Next ID to Use |
|-------------|------|-----------------|----------------|
| Guide | GDE | 000 | BRIEF-GDE-001 |
| FAQ | FAQ | 000 | BRIEF-FAQ-001 |
| Checklist | CHK | 000 | BRIEF-CHK-001 |
| Comparison | CMP | 000 | BRIEF-CMP-001 |
| Partner Page | PRTN | 000 | BRIEF-PRTN-001 |
| Service Page | SVC | 000 | BRIEF-SVC-001 |
| Email Sequence | EMAIL | 000 | BRIEF-EMAIL-001 |
| Social Post | SOC | 000 | BRIEF-SOC-001 |
| Video Script | VID | 000 | BRIEF-VID-001 |
| Lead Magnet | LM | 000 | BRIEF-LM-001 |
| Landing Page | LP | 000 | BRIEF-LP-001 |
| Blog Post | BLOG | 000 | BRIEF-BLOG-001 |
| Lifestyle | LIFE | 000 | BRIEF-LIFE-001 |

---

## Partner IDs — `PRTN`

| Category | Code | Current Sequence | Next ID to Use |
|----------|------|-----------------|----------------|
| Lawyer | LEG | 001 | PRTN-LEG-002 |
| Accountant | ACC | 001 | PRTN-ACC-002 |
| Government Liaison | GOV | 001 | PRTN-GOV-002 |
| Shipping | SHIP | 000 | PRTN-SHIP-001 |
| Property Developer | DEV | 000 | PRTN-DEV-001 |
| Property Agent | AGENT | 000 | PRTN-AGENT-001 |
| Insurance | INS | 000 | PRTN-INS-001 |
| Tax Specialist | TAX | 000 | PRTN-TAX-PROC-001 |
| Other | OTH | 000 | PRTN-OTH-001 |

---

## Prompt IDs — `PRMT`

| Area | Code | Current Sequence | Next ID to Use |
|------|------|-----------------|----------------|
| Research | RES | 004 | PRMT-RES-005 |
| Content | CNT | 004 | PRMT-CNT-005 |
| Extraction | EXT | 003 | PRMT-EXT-004 |
| Analysis | ANL | 003 | PRMT-ANL-004 |
| Agents | AGT | 013 | PRMT-AGT-014 |

---

## Taxonomy IDs — `TAX`

Taxonomy definition files. Format: `TAX-[CATEGORY]-[NNN]`. Each category has its own sequence.

| Category | Code | Current Sequence | Next ID to Use |
|----------|------|-----------------|----------------|
| Process Status | PROC | 001 | TAX-PROC-002 |
| Confidence Levels | CONF | 001 | TAX-CONF-002 |
| Content Categories | CNT | 001 | TAX-CNT-002 |
| ICP Segments | ICP | 001 | TAX-ICP-002 |
| Immigration | IMM | 001 | TAX-IMM-002 |
| Partner Categories | PART | 001 | TAX-PART-002 |
| Service Types | SVC | 001 | TAX-SVC-002 |
| Source Types | SRC | 001 | TAX-SRC-002 |
| Tag Registry | TAG | 001 | TAX-TAG-002 |

---

## Content Type Definition IDs — `CT-DEF`

Definitions and rules for each content type. One record per content type.

| Type | Code | Current Sequence | Next ID to Use |
|------|------|-----------------|----------------|
| Content Type Definitions | DEF | 001 | CT-DEF-002 |

---

## Notion Schema IDs — `SCH-NOT`

GitHub schema specifications for Notion databases. One record per Notion database.

| Database | Code | Current Sequence | Next ID to Use |
|----------|------|-----------------|----------------|
| Notion Schemas | NOT | 007 | SCH-NOT-008 |

Assigned IDs:
- SCH-NOT-001 — notion-contact-database.yaml (Contacts)
- SCH-NOT-002 — notion-partner-database.yaml (Partners)
- SCH-NOT-003 — notion-content-database.yaml (Content Pipeline)
- SCH-NOT-004 — notion-case-database.yaml (Cases)
- SCH-NOT-005 — notion-research-database.yaml (Research Log)
- SCH-NOT-006 — notion-knowledge-database.yaml (Knowledge Base)
- SCH-NOT-007 — notion-process-database.yaml (Processes)

---

## Official Source Reference IDs — `OFF`

Structured reference files capturing key official figures (fees, thresholds, form codes, contacts) from Cypriot government and regulatory bodies. One file per official body or domain.

| Body | Code | Current Sequence | Next ID to Use |
|------|------|-----------------|----------------|
| CRMD (Civil Registry & Migration Dept) | CRMD | 001 | OFF-CRMD-002 |
| Department of Labour | LAB | 001 | OFF-LAB-002 |
| Cyprus Examinations Authority | CEA | 001 | OFF-CEA-002 |

---

## How to Use This Registry

1. Identify the correct prefix and area/type code for the record you are creating.
2. Note the **Current Sequence** number for that row.
3. Increment by 1 — that is the ID to assign to your new record.
4. Update the **Current Sequence** and **Next ID to Use** columns in this file.
5. Commit the update to the registry alongside the new record.

**Never skip numbers or reuse IDs.** If a record is deleted, its ID is retired — do not reassign it.
