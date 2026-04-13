# Tool Stack

## Overview

| Tool | Role | Who Uses It |
|---|---|---|
| GitHub | Source of truth — version-controlled definitions, templates, process docs | All team members |
| Notion | Operational frontend — cases, content pipeline, partner records, research log | All team members |
| Perplexity | Deep research sessions for process documentation | Jason / Research role |
| Plaud Note | Recording partner interviews and client consultations | Jason / Advisor role |
| Claude | Knowledge extraction, content drafting, system maintenance | Jason / Content role |
| VS Code | Editing repository files | Jason / Technical role |

---

## Tool Details

### GitHub — `bettysoarre/Paphos-advisors-system`

**Role:** Canonical definition layer. Everything authoritative lives here.

**What it holds:**
- Process documentation
- SOPs
- Knowledge templates
- Content system definitions
- Taxonomies and schemas
- Governance documents
- Prompt library
- ICP profiles
- Workflow definitions

**How it is used:**
- Files are edited locally in VS Code and pushed to GitHub
- Claude Code (VS Code extension) is used for structured file creation and edits
- Team members clone the repo locally and pull to get updates
- GitHub is not used for issue tracking — it is a document store

**Integration with Notion:** Notion databases are built from the schemas defined in `system/schemas/`. Changes to schemas in GitHub must be reflected in Notion manually (or via MCP).

---

### Notion

**Role:** Operational frontend. Where work happens day to day.

**Databases:**
| Database | Purpose | Schema reference |
|---|---|---|
| Partners | Partner records, trust levels, commercial terms | `system/schemas/notion-partner-database.yaml` |
| Content Pipeline | Content briefs, statuses, ownership | `system/schemas/notion-content-database.yaml` |
| Research Log | Research sessions, source tracking | `system/schemas/notion-research-database.yaml` |
| Process Library | Process doc registry | `system/schemas/notion-process-database.yaml` |
| Knowledge Base | KB article registry | `system/schemas/notion-knowledge-database.yaml` |
| Cases | Client case tracking | `system/schemas/notion-case-database.yaml` |
| Contacts/Clients | Client records | `system/schemas/notion-contact-database.yaml` |

**Integration with GitHub:** Notion does not auto-sync with GitHub. Schema changes, new process docs, and new KB articles created in GitHub should be reflected in the relevant Notion database manually.

---

### Perplexity

**Role:** Research tool for deep-diving Cyprus administrative processes.

**How it is used:**
- Use `prompts/research/process-research-prompt.md` (PROMPT-RES-001) as the input prompt
- Run as a Deep Research session
- Export the output and save to `assets/research-captures/`
- Extract structured content into `processes/` using the process template
- Log the research session in the Notion Research Log

**Limitations:** Perplexity output is treated as medium confidence / mixed source. It must be validated against official sources or field partners before status reaches `validated`.

---

### Plaud Note

**Role:** Recording device for partner interviews and client consultations.

**How it is used:**
- Record all partner interviews during Stage 4 of the partner onboarding process
- Export transcript (text) and save to `assets/transcripts/` with naming convention: `transcript-[partner-slug]-[YYYY-MM-DD].txt`
- Run `prompts/extraction/interview-extraction-prompt.md` (PROMPT-EXT-001) on the transcript in Claude
- Extracted knowledge is structured into KB articles in `knowledge/`

---

### Claude (claude.ai / Claude Code)

**Role:** Knowledge extraction, content drafting, system file creation, Notion operations via MCP.

**How it is used:**
- Knowledge extraction from transcripts: `prompts/extraction/interview-extraction-prompt.md`
- Content drafting: `prompts/content/`
- Research synthesis: `prompts/analysis/`
- System file creation and editing: Claude Code extension in VS Code
- Notion operations: Claude AI with Notion MCP connection

**MCP integrations:** Notion MCP is connected, enabling Claude to read and write Notion pages and databases directly.

---

### VS Code

**Role:** Primary editor for repository files.

**Extensions in use:**
- Claude Code — AI-assisted file creation and editing, Notion MCP operations
- GitLens (recommended) — enhanced git history and blame

**Workflow:** Edit files locally → stage → commit → push to GitHub → teammates pull.
