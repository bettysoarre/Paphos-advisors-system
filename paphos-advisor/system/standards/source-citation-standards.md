# Source Citation Standards

## Purpose

Every knowledge claim in the system must be traceable to a source. This document defines how sources are cited in process documents, KB articles, and content — and what constitutes an acceptable source.

---

## Source Types

Defined in `system/taxonomies/source-types.yaml`. Summary:

| Type | Description | Default confidence |
|---|---|---|
| `official` | Government websites, legislation, official guidance | High |
| `field` | Partner interviews, practitioner observations | Medium |
| `mixed` | Combination of official and field | Medium |

---

## Citation Formats

### Official sources (in process documents and KB articles)

Use the full URL plus a retrieval date. Government pages move or get updated.

```yaml
sources:
  - type: official
    name: Cyprus Civil Registry and Migration Department — MEU1 guidance
    url: https://www.moi.gov.cy/moi/crmd/crmd.nsf/...
    retrieved: 2026-04-01
    notes: Official page for Yellow Slip applications. Check for updates.
```

### Field sources (partner interviews)

Do not name individual partners in public-facing documents. Reference the interview by category and date.

```yaml
sources:
  - type: field
    category: immigration-lawyer
    location: paphos
    interview_date: 2026-03-15
    notes: Confirmed 1-3 month real-world processing time at Paphos CRMD office.
```

### Research session sources (Perplexity)

Reference the session by date and the prompt used.

```yaml
sources:
  - type: research-session
    tool: perplexity
    prompt_ref: PROMPT-RES-001
    session_date: 2026-04-01
    capture_file: assets/research-captures/yellow-slip-research-2026-04-01.md
    notes: Used for initial draft. Treat as medium confidence until field-validated.
```

---

## Inline Citations in Markdown Content

For published website content, do not expose raw source URLs inline. Instead:

- Cite official sources as "According to the Cyprus Civil Registry and Migration Department..."
- Cite field intelligence as "In practice..." or "Our advisors' experience indicates..."
- Never present field intelligence as official guidance
- Always add the accuracy disclaimer when confidence is medium or lower

---

## Acceptable vs Unacceptable Sources

### Acceptable

| Source | Acceptable? | Notes |
|---|---|---|
| Official government website (Cyprus) | Yes | Preferred for official claims |
| Cyprus legislation (official gazette) | Yes | Highest authority |
| Official government PDF/document | Yes | Save a copy in `assets/` |
| Partner interview (immigration lawyer, tax advisor, etc.) | Yes | Cite as field source |
| Perplexity Deep Research | Yes | Treat as medium confidence; must be corroborated |
| Established expat community (Expats in Cyprus, etc.) | Conditional | Only for qualitative/anecdotal context, not procedural facts |
| News article | Conditional | Only for recent regulatory changes; corroborate with official source |

### Not Acceptable

| Source | Reason |
|---|---|
| Wikipedia | Not authoritative for legal/regulatory claims |
| Reddit / Facebook groups | Anecdotal, unverified, frequently wrong |
| Other advisory websites | May be outdated, biased, or incorrect |
| "General knowledge" | Untraceable |
| AI-generated without source | AI hallucination risk |

---

## Updating Sources

When a source is updated (e.g., the government changes its guidance page):
1. Update the URL and retrieval date in the relevant process doc or KB article
2. Review whether the content needs updating
3. Update the confidence level if appropriate
4. Add a `field_note` entry recording the update
5. Log in CHANGELOG if it is a significant change

---

## Source Registry

Known reliable sources for Cyprus processes are catalogued in [research/sources/official-sources-cyprus.md](../../research/sources/official-sources-cyprus.md). Check there before searching from scratch.
