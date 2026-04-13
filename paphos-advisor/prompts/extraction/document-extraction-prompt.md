---
id: PROMPT-EXT-002
title: Document Extraction Prompt
type: extraction
tool: claude
version: "1.0"
created: 2026-04-13
updated: 2026-04-13
output_format: Structured KB article drafts from an official document
use_with: SOP-RES-003 (Knowledge Extraction SOP)
---

# Document Extraction Prompt (PROMPT-EXT-002)

## Purpose
Extract structured knowledge from an official document (PDF, government webpage, legislation extract) and format it as KB article drafts for the knowledge base.

## Tool
Claude

---

## Prompt

```
You are extracting structured knowledge from an official Cyprus government document for the Paphos Advisors knowledge base. Your job is to identify the specific, actionable facts in the document and format them as KB article drafts.

DOCUMENT TYPE: [Official webpage / PDF / Legislation extract / Guidance document]
DOCUMENT NAME: [Name and URL/reference]
TOPIC AREA: [immigration / tax / property / business / healthcare / transport / shipping / insurance / settling-in]
RETRIEVED DATE: [YYYY-MM-DD]

DOCUMENT CONTENT:
[PASTE THE DOCUMENT CONTENT HERE]

INSTRUCTIONS:
1. Read the document carefully and identify all specific, actionable facts relevant to Cyprus relocation processes
2. For each fact, create a KB article draft using this format:

---
KB ARTICLE DRAFT
id: KB-OFF-[AUTO — assign sequential number]
title: "[Specific, concrete title — state the claim, e.g., 'MEU1 official processing time is 5 working days']"
type: official
topic_area: [area]
confidence: high
source_type: official
source: "[Document name] — [URL] — Retrieved: [date]"
related_process: [PROC-XXX-NNN if known]
created: [today's date]
updated: [today's date]

CLAIM:
[The specific factual claim, stated precisely]

OFFICIAL TEXT:
"[Direct quote from the document if available]"

CONTEXT:
[Any conditions, exceptions, or context needed to interpret the claim correctly]

LIMITATIONS:
[Any limitations of this official guidance — e.g., "this is the official position; real-world practice may differ"]
---

3. Only extract facts that are specific and actionable — skip general background information
4. If the document contains information that contradicts our existing process documentation, flag it explicitly with: [CONFLICT: describe the conflict]
5. Note any information that appears outdated (e.g., references to dates that have passed)
6. At the end, provide a SUMMARY listing: total KB articles extracted, any conflicts found, any information that needs field validation

DOCUMENT CONTENT:
[PASTE HERE]
```

---

## How to Use

1. Obtain the official document (copy the relevant text from the webpage, or paste PDF content)
2. Fill in the document details
3. Run in Claude
4. Review the extracted KB articles — remove any that are too vague or not actionable
5. Create the KB article files following SOP-KNW-001
6. Update related process docs
7. Log in Research Log
