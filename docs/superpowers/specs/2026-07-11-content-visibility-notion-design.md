# Design: Content Visibility in Notion (for Perplexity/Claude page-building handoff)

## Problem

Jason can't reliably tell, from Notion, what website/blog content has actually been written and where to find it, so he can't consistently feed finished content into Claude when building wireframes/pages.

Investigation findings (live Notion + repo, 2026-07-11):

- The Content Pipeline database has 56 records for website pages, but only ~6 have real drafted content. For those, the full draft is pasted into the Notion page body **and** linked via a field currently named "GitHub Content-Type Definition."
- That field name is not just unclear — it's the wrong ID scheme entirely. The system's own ID registry defines `CT-DEF` as "Content Type Definitions" (writing rules per content type, e.g. word count/SEO rules), not a draft-file link. The field is being used for something its name says it isn't.
- Zero blog-post records exist in the Content Pipeline, even after the sitemap rebuild added 18 blog pages. No blog content was found anywhere else in Notion either — as far as this session could tell, none has been drafted yet.
- There's no single Notion view that answers "what's actually written and where" — you have to open individual records.

## Decisions

- **Content stays dual-stored**: full draft text pasted into the Notion page body, *and* linked to the GitHub source file. This is intentional, not a bug to fix.
- **The mismatched field name is NOT being resolved in this pass.** Flagged for Jason to decide: add a new, correctly-named field vs. keep reusing "GitHub Content-Type Definition" for draft links vs. something else. Out of scope here.
- **How Jason will actually hand content to Claude when building pages is still open** (copy-paste vs. Claude Code reading Notion/repo directly vs. an export bundle). Out of scope here — this pass only fixes Notion visibility, independent of that answer.

## Scope of this pass

1. Add Content Pipeline records for all 18 new blog posts from the sitemap rebuild (Content Type = `blog-post`, Status = `Idea`, Content Title/Target Keyword/Related ICPs populated from `canonical-url-inventory.md` section 9 and `sitemap-full-metadata.csv`). No content exists yet for these — the point is making them visible/trackable, not writing them.
2. Create a saved Notion view on the Content Pipeline database, filtered to `Status` in {In Production, In Review, Revision, Approved, Scheduled, Published} — i.e., pieces that have actually been drafted — so there's one place to check "what's written." (Excludes Idea, Briefed, Assigned — brief exists but no draft yet.)
3. Add a short note to the Content SOP (`paphos-advisor/sops/content/`) documenting where drafted content actually lives today (Notion page body + the mislabeled link field) so this isn't tribal knowledge, without renaming anything.

## Explicitly out of scope

- Renaming or repurposing the "GitHub Content-Type Definition" field (flagged for Jason).
- Building an export/bundle tool for the Claude hand-off (Approach C from the discussion) — deferred until the handoff method is confirmed.
- Writing any actual blog post or page content.

## Success criteria

- All 18 blog pages exist as Content Pipeline records with correct metadata.
- A saved view exists that shows only content with real drafts, with no manual cross-referencing needed.
- The SOP note exists so the next person (human or agent) knows where to look and where to put new drafts.
