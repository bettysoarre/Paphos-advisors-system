# Naming Conventions

All files, folders, IDs, tags, and taxonomy values in the Paphos Advisor system follow strict naming conventions to ensure consistency, searchability, and compatibility across GitHub, Notion, and AI tooling.

---

## 1. File Naming

**Rule:** All files use `kebab-case` — lowercase words separated by hyphens. No spaces, underscores, or uppercase letters.

**Format:** `[descriptive-slug].[extension]`

**Examples:**

| Correct | Incorrect |
|---------|-----------|
| `eu-national-residence-registration.md` | `EU National Residence Registration.md` |
| `non-dom-application.md` | `NonDomApplication.md` |
| `process-template.md` | `process_template.md` |
| `notion-partner-database.yaml` | `NotionPartnerDatabase.yaml` |
| `content-brief-template.md` | `Content Brief Template.md` |

**Rules:**
- Use the most descriptive slug possible — avoid single-word filenames unless the context is unambiguous
- Do not use version numbers in filenames (use git history instead)
- Templates always end with `-template` before the extension
- Index files are always named `_index.md` (with leading underscore)

---

## 2. Folder Naming

**Rule:** All folders use `kebab-case`. No spaces, underscores, or uppercase letters.

**Format:** `[descriptive-slug]/`

**Examples:**

| Correct | Incorrect |
|---------|-----------|
| `content-system/` | `Content System/` |
| `settling-in/` | `settling_in/` |
| `_templates/` | `Templates/` |
| `decision-trees/` | `decisionTrees/` |

**Rules:**
- Special system folders use a leading underscore: `_templates/`, `_archive/`
- Top-level folders should be single nouns or short noun phrases
- Sub-folders should be as specific as needed to distinguish their contents

---

## 3. ID Conventions

Every record type in the system has a unique ID. IDs are used in filenames, frontmatter, Notion databases, and cross-references.

**General format:** `[PREFIX]-[AREA CODE]-[3-digit sequence]`

All components are uppercase. Sequences are zero-padded to 3 digits and increment by 1.

### 3.1 Process IDs

**Format:** `PROC-[AREA]-[###]`

| Area | Code | Example |
|------|------|---------|
| Immigration | IMM | `PROC-IMM-001` |
| Tax | TAX | `PROC-TAX-PROC-001` |
| Property | PROP | `PROC-PROP-001` |
| Business | BIZ | `PROC-BIZ-001` |
| Healthcare | HLTH | `PROC-HLTH-001` |
| Transport | TRN | `PROC-TRN-001` |
| Shipping | SHIP | `PROC-SHIP-001` |
| Insurance | INS | `PROC-INS-001` |
| Settling-In | SET | `PROC-SET-001` |

### 3.2 SOP IDs

**Format:** `SOP-[AREA]-[###]`

| Area | Code | Example |
|------|------|---------|
| Content | CNT | `SOP-CNT-001` |
| Partners | PRTN | `SOP-PRTN-001` |
| Cases | CASE | `SOP-CASE-001` |
| Research | RES | `SOP-RES-001` |
| Knowledge | KB | `SOP-KB-001` |
| Operations | OPS | `SOP-OPS-001` |

### 3.3 Knowledge Article IDs

**Format:** `KB-[AREA]-[###]`

| Area | Code | Example |
|------|------|---------|
| Immigration | IMM | `KB-IMM-001` |
| Tax | TAX | `KB-TAX-PROC-001` |
| Property | PROP | `KB-PROP-001` |
| Business | BIZ | `KB-BIZ-001` |
| Healthcare | HLTH | `KB-HLTH-001` |
| Transport | TRN | `KB-TRN-001` |
| Shipping | SHIP | `KB-SHIP-001` |
| Insurance | INS | `KB-INS-001` |
| Settling-In | SET | `KB-SET-001` |

### 3.4 Content IDs

**Format:** `CNT-[TYPE]-[###]`

| Content Type | Code | Example |
|-------------|------|---------|
| Guide | GDE | `CNT-GDE-001` |
| FAQ | FAQ | `CNT-FAQ-001` |
| Checklist | CHK | `CNT-CHK-001` |
| Comparison | CMP | `CNT-CMP-001` |
| Partner Page | PRTN | `CNT-PRTN-001` |
| Service Page | SVC | `CNT-SVC-001` |
| Email Sequence | EMAIL | `CNT-EMAIL-001` |
| Social Post | SOC | `CNT-SOC-001` |
| Video Script | VID | `CNT-VID-001` |
| Lead Magnet | LM | `CNT-LM-001` |
| Landing Page | LP | `CNT-LP-001` |
| Blog Post | BLOG | `CNT-BLOG-001` |

### 3.5 Partner IDs

**Format:** `PRTN-[CATEGORY]-[###]`

| Category | Code | Example |
|----------|------|---------|
| Lawyer | LAW | `PRTN-LAW-001` |
| Accountant | ACCT | `PRTN-ACCT-001` |
| Government Liaison | GOV | `PRTN-GOV-001` |
| Shipping | SHIP | `PRTN-SHIP-001` |
| Property Developer | DEV | `PRTN-DEV-001` |
| Property Agent | AGENT | `PRTN-AGENT-001` |
| Insurance | INS | `PRTN-INS-001` |
| Tax Specialist | TAX | `PRTN-TAX-PROC-001` |
| Other | OTH | `PRTN-OTH-001` |

### 3.6 Prompt IDs

**Format:** `PROMPT-[AREA]-[###]`

| Area | Code | Example |
|------|------|---------|
| Research | RES | `PROMPT-RES-001` |
| Content | CNT | `PROMPT-CNT-001` |
| Extraction | EXT | `PRMT-EXT-001` |
| Analysis | ANL | `PROMPT-ANL-001` |
| Agents | AGT | `PRMT-AGT-001` |

### 3.7 Brief IDs

**Format:** `BRIEF-[TYPE]-[###]`

Uses the same type codes as Content IDs. Example: `BRIEF-GDE-001`

---

## 4. Taxonomy Value Format

All taxonomy values (used in YAML files, Notion selects, and frontmatter) follow these rules:

**Rule:** `kebab-case` — lowercase, hyphen-separated, no spaces or underscores.

**Examples:**

| Correct | Incorrect |
|---------|-----------|
| `needs-revalidation` | `Needs Revalidation` |
| `eu-national` | `EU National` |
| `multi-step-relocator` | `MultiStepRelocator` |
| `tax-specialist` | `tax_specialist` |
| `in-research` | `In Research` |

**Rules:**
- Values must exactly match the `id` field in the corresponding taxonomy YAML file
- Never create new values without adding them to the taxonomy YAML first
- Values are case-sensitive — always lowercase

---

## 5. Tag Conventions

Tags are drawn exclusively from `tag-registry.yaml`. No ad-hoc tags are permitted.

**Format:** `kebab-case`, same as taxonomy values.

**Rules:**
- Apply tags from all relevant dimensions (process, service, geography, audience)
- Use the most specific tag available — prefer `residence-permit` over `immigration` when the content is specifically about residence permits
- A content or process record should carry between 3 and 8 tags; fewer suggests under-tagging, more suggests the content scope is too broad
- If a needed tag does not exist, propose it for addition to `tag-registry.yaml` — do not use an informal variant

**Examples:**

```yaml
tags:
  - immigration          # process dimension
  - residence-permit     # service dimension
  - paphos               # geography dimension
  - eu-nationals         # audience dimension
```
