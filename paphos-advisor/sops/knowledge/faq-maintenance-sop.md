---
id: SOP-KNW-004
title: FAQ Maintenance SOP
area: knowledge
status: validated
version: "1.0"
created: 2026-04-13
updated: 2026-04-13
related_sops: [SOP-KNW-001, SOP-CON-004]
---

# FAQ Maintenance SOP

## Purpose
Defines how FAQ content is created, maintained, and retired — both in the knowledge base and in published content.

---

## FAQ Sources

FAQs come from three sources:
1. **Client questions** — questions asked in active cases or initial enquiries
2. **Content research** — keyword research revealing what people are searching for
3. **Partner insights** — questions that partners commonly encounter from their clients

All three are valid. Client questions are the most valuable because they are real, specific, and unfiltered.

---

## Capturing New FAQs

### From client cases
When a client asks a question that is not clearly answered in existing content or process docs:
1. Answer the client from the best available source
2. Note the question in the Case notes
3. Add a task to the Content Pipeline for an FAQ entry (or add it to the relevant FAQ file)
4. If the question revealed a knowledge gap, run a research session to get the definitive answer before publishing

### From keyword research
When keyword research identifies a common question:
1. Add a content brief to the Content Pipeline for an FAQ entry
2. Research the answer from process docs and KB articles before writing
3. Do not publish FAQ answers that are not grounded in validated sources

---

## Creating a New FAQ Entry

Follow the `faq-page.md` content type definition for format requirements.

Key rules:
- Question format: "How do I...", "Can I...", "What is...", "How long does..." — not "FAQ about..."
- Answer: maximum 500 words. If the answer requires more, it is a guide, not an FAQ.
- Every answer must cite at least one source (KB article ID or process doc ID)
- Group FAQs by topic (minimum 3 per group, maximum 12)
- Add FAQPage JSON-LD structured data per the faq-entry.md content type spec

---

## Maintaining Existing FAQs

Review FAQ content:
- When the related process doc is updated
- On the standard content review cadence (see `content-system/rules/update-cadence-rules.md`)
- When a client provides an answer that contradicts published FAQ content

When updating:
1. Update the KB article or process doc first
2. Then update the FAQ content to match
3. Update the "Last updated" date on the published page
4. Re-submit for indexing if the change is significant

---

## Retiring FAQs

Retire a FAQ when:
- The process it relates to no longer exists
- The question is no longer commonly asked (traffic has dropped to near zero for 12+ months)
- A better, more comprehensive answer has been published elsewhere and the FAQ is now redundant

Retirement steps:
1. Remove or redirect the FAQ from the published page
2. Update the Notion Content Pipeline record to `archived`
3. Archive the KB-FAQ article following SOP-KNW-003
