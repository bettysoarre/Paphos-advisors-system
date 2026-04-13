# Content Type: Process Explainer

## Definition
A step-by-step walkthrough of a single Cyprus administrative process. More detailed than a FAQ, less comprehensive than a full relocation guide. The primary format for documenting "how to do X in Cyprus."

## Source requirement
Must be grounded in a validated process doc (`processes/[area]/[slug].md`) at status `validated` or `published`. Do not write a process explainer from a `draft` process doc.

## Word count
1,000–2,000 words

## Required sections

1. **What this process is** (1-2 paragraphs) — what it achieves, who needs it, when
2. **Who this applies to** — nationality, residency status, circumstances
3. **Before you start** — prerequisites, things to have in place first
4. **Step-by-step process** — numbered steps, each with: what to do, where, documents needed, expected timeline
5. **Documents required** — table format (Document | Format | Where to get it | Notes)
6. **Costs** — official fees and any expected incidental costs
7. **Timeline** — official timeline AND real-world timeline (where they differ)
8. **Common issues and how to avoid them** — sourced from field intelligence
9. **Frequently asked questions** — 3-5 questions specific to this process
10. **Next steps** — what to do after this process is complete; what related processes follow

## SEO requirements

| Element | Requirement |
|---|---|
| Meta title | "[Process name] Cyprus — [qualifier]" |
| Meta description | 150-160 chars, includes process name and key benefit |
| H1 | Matches meta title closely |
| Primary keyword | In H1, first 100 words, 2+ times in body |
| Structured data | HowTo schema |

## Disclaimer requirement
Standard disclaimer (footer). Enhanced accuracy disclaimer if source confidence is medium.

## Internal links
- Link to parent pillar page
- Link to related processes (e.g. Yellow Slip explainer links to Non-Dom Status)
- Link to relevant checklist
- Link to partner profile page for relevant partner category

## Update cadence
6 months or when related process doc is updated (whichever is sooner).

## HowTo Schema Example

```json
{
  "@context": "https://schema.org",
  "@type": "HowTo",
  "name": "How to Get a Yellow Slip in Cyprus (EU National)",
  "description": "Step-by-step guide to registering as an EU national in Cyprus with the MEU1 form.",
  "step": [
    {
      "@type": "HowToStep",
      "name": "Obtain a Tax Identification Code (TIC)",
      "text": "Visit the Tax Department Paphos to register for a TIC. Bring your passport."
    },
    {
      "@type": "HowToStep",
      "name": "Book an appointment at CRMD Paphos",
      "text": "Book via the CRMD online portal or call the Paphos office directly."
    }
  ]
}
```
