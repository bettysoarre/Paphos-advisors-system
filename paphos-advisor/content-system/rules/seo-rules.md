# SEO Rules

## Purpose
Defines the SEO requirements for all published content. These are minimum standards, not aspirational targets.

---

## Meta Title

| Rule | Detail |
|---|---|
| Length | 50-60 characters |
| Primary keyword | Must appear, ideally near the start |
| Brand inclusion | Optional for inner pages; "Paphos Advisors" or "Paphos" can be appended |
| Format | [Primary keyword] — [Qualifier] | Paphos Advisors |

**Examples:**
✓ `Yellow Slip Cyprus — EU National MEU1 Guide`
✓ `60-Day Tax Residency Rule Cyprus — How It Works`
✗ `Information About the Yellow Slip Registration Process for European Union Nationals in Cyprus` (too long)
✗ `Our Guide` (not descriptive)

---

## Meta Description

| Rule | Detail |
|---|---|
| Length | 150-160 characters |
| Primary keyword | Must appear once |
| Value proposition | What will the reader learn / get? |
| CTA | Soft call to action ("Learn how...", "Find out...") |

**Example:**
✓ `Everything you need to know about getting a Yellow Slip in Cyprus as an EU national. Steps, documents, processing times, and Paphos office tips.`

---

## H1

- Must match meta title closely (not identical but aligned)
- One H1 per page — no exceptions
- Include the primary keyword naturally

---

## URL Structure

- Lowercase, hyphenated, no underscores
- Include the primary keyword
- Short as possible while being descriptive
- No dates in URLs (they become stale and cause redirect needs)

✓ `/guides/yellow-slip-cyprus-eu-national`
✗ `/blog/2026/04/how-to-get-yellow-slip-cyprus-2026`

---

## Keyword Usage

- Primary keyword: in H1, meta title, meta description, first 100 words, at least 2 more times in body
- Secondary keywords: naturally in H2s and body
- No keyword stuffing — write for humans first
- Do not force keywords into headings if it makes them unnatural

---

## Content Length

Minimum content lengths by content type:
| Content type | Minimum | Target |
|---|---|---|
| Relocation guide | 2,000 words | 3,000-4,000 |
| Process explainer | 1,000 words | 1,500-2,000 |
| FAQ page | 800 words | 1,200-2,000 |
| Checklist | 500 words | 800-1,200 |
| Comparison article | 1,500 words | 2,000-3,000 |
| News update | 300 words | 400-600 |

---

## Internal Linking

- Minimum 2 internal links per 1,000 words
- Link to pillar pages from cluster content
- Link between related cluster pages
- Use descriptive anchor text (not "click here")
- Full rules in `content-system/rules/internal-linking-rules.md`

---

## Structured Data

Required structured data by content type:
| Content type | Schema type |
|---|---|
| FAQ page | FAQPage |
| Process explainer (step-by-step) | HowTo |
| Guide / article | Article |
| Partner profile | LocalBusiness |

See `content-system/content-types/` for specific schema examples.

---

## Image SEO

- Alt text on every image (required)
- File names: descriptive, hyphenated (`yellow-slip-application-form.jpg` not `IMG001.jpg`)
- Compress all images before upload (target < 200KB for non-hero images)
- Add title attribute where appropriate

---

## Core Web Vitals

(To be addressed when the website platform is selected.)
- Largest Contentful Paint (LCP): < 2.5s
- Cumulative Layout Shift (CLS): < 0.1
- Interaction to Next Paint (INP): < 200ms
