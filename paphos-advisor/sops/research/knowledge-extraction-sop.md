---
id: SOP-RES-003
title: Knowledge Extraction SOP
area: research
status: validated
version: "1.0"
created: 2026-04-13
updated: 2026-04-13
related_sops: [SOP-RES-001, SOP-RES-002, SOP-RES-004]
---

# Knowledge Extraction SOP

## Purpose
Defines how to extract structured knowledge from raw inputs (transcripts, research captures, documents) and integrate it into the system.

## When to Use
After a research session is captured, or after a partner interview transcript is available.

---

## Input Types

| Input | Extraction prompt to use |
|---|---|
| Partner interview transcript | `prompts/extraction/interview-extraction-prompt.md` (PROMPT-EXT-001) |
| Perplexity research session | `prompts/extraction/research-session-extraction-prompt.md` (PROMPT-EXT-003) |
| Official document / PDF | `prompts/extraction/document-extraction-prompt.md` (PROMPT-EXT-002) |

---

## Steps

### 1. Confirm the input is captured
Verify the raw file exists in `assets/transcripts/` or `assets/research-captures/` before beginning extraction.

### 2. Run the extraction prompt
Open Claude. Paste:
1. The full extraction prompt from `prompts/extraction/`
2. The raw input text

Run the extraction. The output will be a structured set of KB article drafts.

### 3. Review the extracted output
Before creating any files, review the extracted KB articles:
- Are the claims specific and actionable?
- Is the confidence level appropriately assigned?
- Are there contradictions with existing process docs?
- Are there any claims that seem implausible or need further validation?

### 4. Create KB article files
For each validated extraction item:
- Use the appropriate template from `knowledge/_templates/`
- Assign an ID from `system/standards/id-registry.md`
- Save to the correct subfolder in `knowledge/` (official, field, faqs, decision-trees)
- Populate all required frontmatter fields

### 5. Update related process documents
For each extracted item that relates to an existing process doc:
- Open the relevant process doc in `processes/`
- Add or update the `field_notes` section with the new intelligence
- Update the `confidence` level if the new intelligence changes it
- Update the `updated` date in the frontmatter

### 6. Update the Research Log in Notion
- Set the session status to `Integrated`
- Record how many KB articles were created
- Note which process docs were updated

### 7. Commit to GitHub
Commit all new KB articles and updated process docs in a single commit with a clear message:
```
Add KB articles from [source type] — [topic area]

Example: Add KB articles from immigration lawyer interview — MEU1 process
```

---

## Quality Rules
- Never create a KB article with `unverified` confidence unless it is explicitly a placeholder awaiting validation
- Every KB article must have a traceable source (interview date + category, or URL + retrieval date)
- If an extraction reveals a contradiction with an existing process doc, do not silently update the doc — flag the contradiction in `field_notes` and note both versions until resolved
