# Research Inbox

Drop new source material here before ingesting it into the knowledge system.

## What goes here

Any new information relevant to Cyprus processes, regulations, tax rules, or field intelligence that has not yet been processed:

- Saved web articles (paste as `.md` or save as `.txt`)
- Government announcement PDFs
- Law firm or accountant bulletins
- Field notes from partner conversations
- Practitioner observations not yet in a process doc
- Perplexity research outputs you want to ingest

## Naming convention

```
[YYYY-MM-DD]-[domain]-[short-description].[ext]
```

Examples:
- `2026-04-20-immigration-crmd-processing-time-update.md`
- `2026-05-01-tax-non-dom-ghs-rate-change.md`
- `2026-04-22-property-stamp-duty-clarification.md`

## How to ingest

Once a file is in this folder, run the ingest agent:

> "Run the ingest agent on `research/inbox/[filename]`"

Or for a URL or topic (no file needed):

> "Run the ingest agent on this URL: [URL]"
> "Run the ingest agent on this topic: [topic]"

The agent reads the file (or fetches the URL / searches the topic via Perplexity), compares it against existing process docs and FAQs, updates what it can, flags contradictions, and moves the file to `research/processed/` when done.

See `PRMT-AGT-003` for the full ingest agent instructions.

## After ingestion

The processed file moves to `research/processed/` with the change report appended. The inbox should be empty between sessions.
