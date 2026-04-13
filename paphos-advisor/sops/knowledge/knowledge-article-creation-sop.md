---
id: SOP-KNW-001
title: Knowledge Article Creation SOP
area: knowledge
status: validated
version: "1.0"
created: 2026-04-13
updated: 2026-04-13
related_sops: [SOP-KNW-002, SOP-RES-003]
---

# Knowledge Article Creation SOP

## Purpose
Defines how to create a structured knowledge article in the `knowledge/` folder.

## When to Use
When creating a new KB article — whether from an interview extraction, research session, or direct observation.

---

## Steps

### 1. Determine the article type
| Type | Use when | Template |
|---|---|---|
| Official | Documenting official government guidance | `knowledge/_templates/official-knowledge-template.md` |
| Field | Documenting practitioner intelligence | `knowledge/_templates/field-knowledge-template.md` |
| FAQ | Answering a specific frequently asked question | `knowledge/_templates/knowledge-article-template.md` |
| Decision tree | Documenting logic for routing a client | `knowledge/_templates/decision-tree-template.md` |

### 2. Assign an ID
Get the next available ID from `system/standards/id-registry.md`:
- Official: `KB-OFF-[NNN]`
- Field: `KB-FLD-[NNN]`
- FAQ: `KB-FAQ-[NNN]`
- Decision tree: `KB-DEC-[NNN]`

Increment the counter in `id-registry.md` after assigning.

### 3. Copy the template
Copy the appropriate template from `knowledge/_templates/` to the correct subfolder:
- Official → `knowledge/official/`
- Field → `knowledge/field/`
- FAQ → `knowledge/faqs/`
- Decision tree → `knowledge/decision-trees/`

Name the file using kebab-case: `[topic-slug]-[KB-ID].md`
Example: `meu1-real-world-processing-time-KB-FLD-001.md`

### 4. Populate the frontmatter
Fill in all required fields from `system/schemas/content-frontmatter-schema.yaml`. Pay particular attention to:
- `confidence` — be honest; default to one level lower if uncertain
- `source` — must be specific and traceable
- `related_process` — link to the relevant PROC-XXX if applicable

### 5. Write the article body
- State the knowledge claim clearly in the first paragraph
- Do not hedge with vague language — if uncertain, reflect it in the confidence level
- Cite the source explicitly
- For field articles: note the context (practitioner type, location, date)
- For official articles: quote the relevant passage and include the URL

### 6. Create the Notion Knowledge Base record
Add an entry in the Notion Knowledge Base database:
- Set all fields per the schema in `system/schemas/notion-knowledge-database.yaml`
- Set `GitHub File Path` to the path of the new file
- Set `Date Created` to today

### 7. Commit to GitHub
Include the new file in a commit with a clear message.

---

## Quality Check
- [ ] ID assigned and registered in id-registry.md
- [ ] All required frontmatter fields populated
- [ ] Confidence level is honest (not optimistic)
- [ ] Source is specific and traceable
- [ ] Body states a clear, specific claim (not vague)
- [ ] Notion record created
