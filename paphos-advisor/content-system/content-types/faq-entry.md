# Content Type: FAQ Entry

## Definition

An FAQ Entry is a single question-and-answer unit addressing one specific, discrete question that a prospective or current client is likely to ask about Cyprus relocation. FAQ entries are designed to:

- Answer a specific question completely in a short, scannable format
- Capture long-tail and question-based search traffic via FAQPage structured data
- Feed directly into the Paphos Advisors FAQ database (groupable by topic, ICP segment, and process area)
- Serve as building blocks for FAQ sections embedded within longer guides

Each FAQ entry addresses **one question only**. If answering a question requires addressing two separate issues, write two entries.

---

## Format

### Question
- Written as the reader would actually ask it — natural language, not keyword-stuffed
- Starts with: What, How, Can, Do, Is, When, Why, Where, How long, How much
- Maximum 15 words
- Does not include the answer in the question

### Answer
- Begins with a direct answer to the question in the first sentence — do not lead with caveats or context
- Plain language; no jargon without explanation
- Where the answer varies by nationality, circumstance, or district, state the most common case first, then note variations
- Ends with a relevant internal link or a brief prompt to seek professional advice where appropriate

---

## Maximum Length

**500 words per answer**

- Aim for 150–300 words for most questions
- 300–500 words only where the question genuinely requires it (e.g. multi-condition eligibility questions)
- If the answer requires more than 500 words, the question is too broad — split it into multiple entries or redirect to a full guide
- Do not pad answers to appear more thorough

---

## Source Requirement

Every FAQ entry must meet the following sourcing standard:

| Requirement | Standard |
|-------------|---------|
| Official source | At least one official source (government portal, legislation, regulatory body) must support any factual claim about process, fees, eligibility, or legal status |
| Internal reference | Link to the relevant process document (PROC-XXX) or knowledge article (KB-XXX) where one exists |
| Field intelligence | If the answer includes a practitioner observation or real-world caveat, flag it explicitly: *"In practice..."* or *"Field experience suggests..."* |
| Recency | Verify the answer is current before publishing. State the date fees or timelines were last confirmed. |

**Minimum:** Every FAQ entry must be traceable to at least one official source or validated internal document before it is marked as approved.

---

## Structured Data (Schema Markup)

FAQ entries are the primary vehicle for FAQPage structured data on the Paphos Advisors website.

**Implementation rules:**

- All FAQ entries published on the site must be marked up with `FAQPage` + `Question` + `Answer` schema (JSON-LD format)
- The schema `name` field must match the question exactly as written
- The schema `text` field must contain the full answer text — do not truncate
- FAQPage schema should be applied at the page level when 2 or more FAQ entries appear together
- Individual FAQ entries embedded within longer guides should use the same schema on the parent page
- Do not duplicate the same question across multiple published pages — this creates schema conflicts and cannibalisation

**Example schema structure:**
```json
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "How long does it take to get a Yellow Slip in Cyprus?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Officially, the Yellow Slip (MEU1) is issued within 5 days..."
      }
    }
  ]
}
```

---

## Grouping Rules

FAQ entries are stored individually but grouped for publication. Grouping rules:

| Dimension | Rule |
|-----------|------|
| By process area | Group entries under the same process topic (e.g. all Yellow Slip FAQs together) |
| By ICP segment | Tag each entry with the relevant ICP segment(s) — allows segment-specific FAQ pages |
| By content type context | FAQs can be embedded in guides, published as standalone FAQ pages, or both |
| Maximum per published group | 8–12 entries per published FAQ section; more than 12 suggests the topic needs a full guide |
| Minimum per published group | 3 entries minimum before publishing as a standalone FAQ page |
| Ordering | Order within a group by: most common question first, then logical flow (e.g. eligibility before process before timeline) |

**Avoid:**
- Grouping unrelated questions together just to bulk up a page
- Publishing a single FAQ entry as a standalone page (too thin — embed in a guide or group)
- Repeating the same answer across multiple FAQ entries — cross-reference instead

---

## Update Cadence

| Volatility | Review Frequency |
|-----------|-----------------|
| Stable (process definitions, eligibility rules) | Every 12 months |
| Volatile (fees, timelines, government policy) | Every 3 months |

**Trigger for immediate review:**
- The linked process document (PROC-XXX) is updated
- A fee, deadline, or threshold cited in the answer changes
- A reader or client flags the answer as incorrect

---

## Frontmatter

```yaml
---
id: CNT-FAQ-[###]
title: ""                   # The question, written exactly as it will appear
content_type: faq
target_keyword: ""          # The long-tail keyword or question phrase this entry targets
search_intent: informational
target_icp:
  - ""
related_processes:
  - ""
source_knowledge:
  - ""
faq_group: ""               # The topic group this entry belongs to (e.g. "Yellow Slip", "Tax Residency")
status: briefed
assigned_to: ""
created: ""
updated: ""
---
```

---

## Quality Checklist

Before an FAQ entry is marked as approved:

- [ ] Question is 15 words or fewer and reads as a natural question
- [ ] Answer opens with a direct response in the first sentence
- [ ] Answer is 500 words or fewer
- [ ] At least one official source or validated internal document is cited
- [ ] Field intelligence (if present) is clearly flagged
- [ ] Fees or timelines include the date last confirmed
- [ ] Internal link to related PROC-XXX or KB-XXX document is included
- [ ] FAQPage schema is specified or noted for implementation
- [ ] ICP segment tags are assigned
- [ ] FAQ group is assigned
