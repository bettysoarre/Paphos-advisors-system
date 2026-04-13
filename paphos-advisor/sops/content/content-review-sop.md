---
id: SOP-CON-002
title: Content Review SOP
area: content
status: validated
version: "1.0"
created: 2026-04-13
updated: 2026-04-13
related_sops: [SOP-CON-001, SOP-CON-003]
---

# Content Review SOP

## Purpose
Defines the review process for content before it is approved for publishing.

## When to Use
When a content item moves to `review` status in the Content Pipeline.

## Who Performs This
Jason (until a dedicated editor role is hired).

---

## Steps

### 1. Check the brief first
Before reading the draft, re-read the brief. Know what the draft was supposed to do before assessing whether it succeeded.

### 2. Accuracy review
For each factual claim, verify:
- Is it traceable to a process doc or KB article?
- Does the confidence level of the source justify presenting it as fact?
- If confidence is medium or lower — is the appropriate disclaimer present?
- If the claim references official guidance — does it match the current version of the process doc?

Flag any claim that cannot be verified with a `[NEEDS SOURCE]` comment.

### 3. Completeness review
Check against the content type definition (`content-system/content-types/[type].md`):
- Are all required sections present?
- Does the word count meet the target (within 10%)?
- Are the required number of internal links present?

### 4. Editorial review
Check against the style guide (`content-system/style-guide/`):
- Tone and voice consistent with brand guidelines
- No passive voice overuse
- No jargon without explanation
- No vague hedging ("it may be possible that..." — be specific or note the uncertainty explicitly)
- Legal disclaimers are correctly worded

### 5. SEO review
Check against `content-system/rules/seo-rules.md`:
- Meta title: within character limit, includes primary keyword
- Meta description: within character limit, includes call to action
- H1 matches meta title (or is a close variant)
- H2s follow logical hierarchy
- Primary keyword in first 100 words

### 6. Internal linking review
Check against `content-system/rules/internal-linking-rules.md`:
- No linking to pages that do not exist yet
- No more than one link to the same page in the same article
- Anchor text is descriptive (not "click here")

### 7. Decision
**Approve** — set status to `approved` in Notion. Note any minor edits made directly.

**Return for revision** — set status back to `in-production`. Add specific revision notes in the brief. Do not return without specific, actionable feedback.

---

## Review Checklist
- [ ] All factual claims traceable
- [ ] Disclaimers present where required
- [ ] All required sections present
- [ ] Word count within range
- [ ] Tone and voice consistent
- [ ] Meta title and description correct
- [ ] SEO requirements met
- [ ] Internal links valid and sufficient
- [ ] No broken or placeholder links
