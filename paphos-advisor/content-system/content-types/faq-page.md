# Content Type: FAQ Page

## Definition
A grouped collection of specific questions and direct answers on a topic area. Optimised for featured snippets and FAQPage structured data. Each page covers a defined topic cluster, not a broad subject area.

## Distinction from faq-entry.md
- `faq-entry.md` — the rules for a single FAQ answer
- `faq-page.md` — the rules for a full FAQ page (collection of entries)

## Word count
800–2,000 words (total across all Q&As on the page)

## Required sections

1. **Introduction** (optional, 1 paragraph max) — briefly frame the topic and who this FAQ is for
2. **FAQ groups** — questions grouped by sub-topic
3. **Related guides callout** — links to deeper content on related topics
4. **Professional advice CTA** — prompt to speak to an advisor for specific situations

## FAQ question rules

- Format: "How do I...", "Can I...", "What is...", "How long does...", "Do I need..."
- No: "FAQ: What is the Yellow Slip?" — drop the "FAQ:" prefix
- Each question must be distinct — no duplicate intent
- Questions must be what real people actually ask (derived from search data, client questions, or partner experience)

## FAQ answer rules

- Maximum 300 words per answer (aim for 100-200)
- Lead with the direct answer in the first sentence
- If the answer has conditions or exceptions, list them after the direct answer
- Every answer must cite at least one source (link to a process doc or KB article)
- If confidence is medium: add the accuracy callout
- Do not make the answer a preamble to a longer guide — answer the question here

## Grouping rules

- Minimum 3 questions per group
- Maximum 12 questions per group
- If a group grows beyond 12, split it into two sub-groups or a separate FAQ page
- Group label should be a topic phrase, not a question (e.g., "Yellow Slip Process", not "Questions About Yellow Slips")

## SEO requirements

| Element | Requirement |
|---|---|
| Meta title | "[Topic] FAQ — Common Questions Answered" or "[N] Questions About [Topic] Answered" |
| Primary keyword | In meta title, H1, and first question |
| Structured data | FAQPage schema (mandatory) |

## FAQPage Schema Example

```json
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "How long does the Yellow Slip take in Paphos?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Officially 5 working days, but in practice the Paphos CRMD office typically takes 1–3 months. Book your appointment as early as possible after arrival."
      }
    }
  ]
}
```

## Update cadence
6 months, or when a client question reveals an inaccuracy.

## Anti-cannibalisation
Do not create an FAQ page that answers questions already answered comprehensively in a process explainer on the same topic. The FAQ page should complement the explainer (quick answers) not duplicate it.
