---
id: PRMT-AGT-005
title: "Agent Skills Matrix"
type: system-reference
version: "1.0"
created: 2026-04-24
updated: 2026-05-01
owner: "lead-advisor"
source: "April 21 planning meeting — Paphos Advisor Guide, ICPs, Content Operations, Headless CMS Plan"
---

# Agent Skills Matrix

Master reference for all Paphos Advisors AI agents. Defines the modular skills library, each agent's role and capabilities, pipeline workflows, and human-in-the-loop gates.

This document governs how agents are built and combined. Individual agent instruction files (PRMT-AGT-*) must reference and conform to the skills defined here.

---

## Modular Skills Library

Skills are reusable modules that agents are assigned. An agent's capability is the sum of its assigned skills. Skills can be updated centrally without rewriting each agent.

| Skill ID | Skill Name | Description |
|---|---|---|
| `SKL-RES` | Research with Citations | Web research using Perplexity; every claim attributed to a named source with URL; no unsourced assertions |
| `SKL-TOV` | Tone of Voice | Applies the Paphos Advisors brand voice: knowledgeable, direct, honest; relatable to Brits (primary) and Germans (secondary); never condescending; never over-promising |
| `SKL-WRI` | Writing Style | Long-form structured content: British English, sentence-case headings, numbered steps for sequences, plain language for complex topics, no filler |
| `SKL-SEO` | Formatting & SEO | H1/H2/H3 hierarchy, meta title (50–60 chars), meta description (150–160 chars), HowTo/FAQ JSON-LD schema scaffolds, internal link placeholders, info boxes |
| `SKL-GRD` | Brand Guardrails | Enforces immovable truths (see section below): no falsehoods, flags unverified items, notes pending/new legislation, blocks publication language before human review |
| `SKL-SOC-IG` | Social: Instagram | Carousel and single-image caption style; 125–150 char captions; 5–10 hashtags; lifestyle-forward tone; visual brief included |
| `SKL-SOC-FB` | Social: Facebook | Community-appropriate tone; longer captions (150–300 chars); question-based engagement hooks; no hashtag overload |
| `SKL-SOC-TK` | Social: TikTok | Hook-first short video scripts (30–60 sec); spoken language, conversational; on-screen text cues included |
| `SKL-SOC-X` | Social: X/Twitter | Thread format or single post (≤280 chars); direct, opinion-adjacent; citation links when factual |
| `SKL-SOC-LI` | Social: LinkedIn | Professional register; 150–300 chars; authority-forward; links to full guides |
| `SKL-COM` | Community Research | Platform-specific monitoring rules for Reddit and Facebook groups; tone calibration for each community; authority cues; escalation triggers |
| `SKL-PR` | PR Research & Pitch Drafting | Identifies link/PR targets; researches site authority and relevance; drafts outreach email/pitch; does not send — human sends |
| `SKL-ADS` | Ads Analysis | Competitor creative scan; identifies positioning gaps; drafts ad copy suggestions; provides dashboards; does not launch campaigns — human manages campaigns |
| `SKL-BRF` | Brief Writing | Converts research output into a structured content brief: audience, keyword, angle, structure, source list, word count, internal links required |
| `SKL-EXT` | Knowledge Extraction | Processes partner interview transcripts into structured KB records; separates official facts from partner opinion; applies reuse risk classification (Safe / Caution / Internal Only / Do Not Use / Needs Verification); enforces DO_NOT_USE guardrails for corruption implications, unsupported guarantees, and confidential partner methods |
| `SKL-RAG` | Chatbot / RAG Safety | Filters KB records for chatbot delivery; only surfaces records classified Safe to Use; appends mandatory disclaimer on legal, tax, immigration, and financial topics; escalates out-of-scope questions to human; never presents partner opinion as official advice |

---

## Agent Registry

### 1. Research Agent
**ID:** PRMT-AGT-002 (existing)
**Stage:** Content Pipeline — Step 1
**Purpose:** Produce a sourced research package for a given content topic or ICP question.

| Field | Value |
|---|---|
| Skills | `SKL-RES`, `SKL-GRD` |
| Input | Topic brief: keyword/question, ICP, key questions to answer, known sources |
| Output | Research document: claims, citations, conflicting sources flagged, knowledge gaps flagged |
| Human gate | Human approves research package before it passes to Brief Writer |
| Guardrails | Never present unverified claims as fact; flag `[NEEDS SOURCE]` explicitly; note if Perplexity result is AI-generated vs. cited |

---

### 2. Content Brief Writer
**ID:** PRMT-AGT-006 *(to be created)*
**Stage:** Content Pipeline — Step 2
**Purpose:** Convert a research package into a structured content brief that the Writer agent can execute without ambiguity.

| Field | Value |
|---|---|
| Skills | `SKL-BRF`, `SKL-SEO`, `SKL-TOV`, `SKL-GRD` |
| Input | Approved research document + target ICP + target keyword + content type + word count target |
| Output | Completed content brief (using content-brief-template.md): audience, angle, structure, key points, SEO targets, internal links required, sources to cite |
| Human gate | Human reviews brief before passing to Writer — editorial angle and scope confirmed here |
| Guardrails | Brief must reference only approved source material; flag if research package has gaps that would prevent a complete draft |

---

### 3. Writer (Content Agent)
**ID:** PRMT-AGT-001 (existing, see content-agent-instructions.md)
**Stage:** Content Pipeline — Step 3
**Purpose:** Draft website content from an approved brief.

| Field | Value |
|---|---|
| Skills | `SKL-WRI`, `SKL-TOV`, `SKL-SEO`, `SKL-GRD` |
| Input | Approved content brief + source material referenced in brief |
| Output | Full draft in Markdown with frontmatter, meta title, meta description, editorial flags |
| Human gate | Human editorial review before any content is published |
| Guardrails | Source-first only; `[NEEDS SOURCE]` not `[I think]`; British English; no regulated-advice language; standard disclaimer on all process content |

---

### 4. Social Repurposing Agent
**ID:** PRMT-AGT-007 *(to be created)*
**Stage:** Social Pipeline — Step 1
**Purpose:** Atomise a published or approved long-form piece into platform-specific social assets.

| Field | Value |
|---|---|
| Skills | `SKL-TOV`, `SKL-GRD`, `SKL-SOC-IG`, `SKL-SOC-FB`, `SKL-SOC-TK`, `SKL-SOC-X`, `SKL-SOC-LI` |
| Input | Approved Markdown article + target platforms + social angle/theme instruction |
| Output | Per-platform draft set: caption(s), hashtag suggestions, visual brief for Canva, posting notes |
| Human gate | Human approves all drafts before scheduling or posting — no auto-publish |
| Guardrails | Never extract and publish a partial claim without full context; add link to full article; respect brand voice per platform; no posting without human sign-off |

---

### 5. Platform Social Agents (Instagram / Facebook)
**ID:** PRMT-AGT-008, PRMT-AGT-009 *(to be created — phase 2)*
**Stage:** Social Pipeline — Scheduled drafting
**Purpose:** Generate draft posts on a schedule for their respective platform, ready for human approval.

| Field | Value |
|---|---|
| Skills | Instagram: `SKL-SOC-IG`, `SKL-TOV`, `SKL-GRD` / Facebook: `SKL-SOC-FB`, `SKL-TOV`, `SKL-GRD` |
| Input | Content calendar entry + approved source article or research package |
| Output | Draft post: caption, hashtags, visual brief; saved to review queue — NOT published |
| Human gate | Mandatory human approval before any post goes live — draft-only in phase 1 |
| Guardrails | Draft only; no auto-schedule or auto-post until human-approval workflow is validated over 4–8 weeks |

*Note: Build after Social Repurposing Agent (PRMT-AGT-007) is validated.*

---

### 6. Community / Reactive Agent
**ID:** PRMT-AGT-010 *(to be created — phase 2)*
**Stage:** Community engagement
**Purpose:** Monitor Reddit, Facebook groups, and WhatsApp communities for relevant conversations and draft response suggestions.

| Field | Value |
|---|---|
| Skills | `SKL-COM`, `SKL-TOV`, `SKL-GRD` |
| Input | Platform feed / monitored thread list + community rules document |
| Output | Flagged threads + suggested response drafts; escalation recommendations when appropriate |
| Human gate | Human reviews all drafted responses and approves before posting; no autonomous engagement |
| Guardrails | Platform-specific moderation rules must be validated before first engagement; no posting on behalf of the business without human; escalate anything involving legal or financial advice |

*Note: Requires community rules playbook (Gratian, due 2026-05-05) before building.*

---

### 7. PR / Link Research & Pitch Agent
**ID:** PRMT-AGT-011 *(to be created — phase 2)*
**Stage:** PR and link building
**Purpose:** Identify link and PR targets; research their authority and relevance; draft outreach pitches.

| Field | Value |
|---|---|
| Skills | `SKL-RES`, `SKL-PR`, `SKL-GRD` |
| Input | Target topic / content piece to promote + site selection criteria |
| Output | Target list with rationale + draft email/pitch per target |
| Human gate | Human reviews pitch drafts and sends manually — agent never sends outreach |
| Guardrails | Do not pitch on behalf of the business without human review; clearly mark all pitches as drafts; include site authority reasoning so human can sanity-check targets |

---

### 8. Ads Analysis Agent
**ID:** PRMT-AGT-012 *(to be created — phase 3)*
**Stage:** Paid advertising support
**Purpose:** Scan competitor creatives, identify positioning gaps, and draft ad copy suggestions and dashboard summaries.

| Field | Value |
|---|---|
| Skills | `SKL-ADS`, `SKL-TOV`, `SKL-GRD` |
| Input | Campaign brief + competitor list + performance data (if available) |
| Output | Competitor creative summary + positioning gap analysis + draft ad copy variants + dashboard summary |
| Human gate | Human manages all campaign setup and activation; agent is analysis and draft only |
| Guardrails | No access to ad platforms; no budget decisions; copy drafts are suggestions only |

---

### 9. Partner Knowledge Extraction Agent
**ID:** PRMT-AGT-014 *(to be formally built — currently run manually)*
**Stage:** Knowledge Pipeline — Step 1
**Purpose:** Process partner interview transcripts into structured KB records with reuse risk classification.

| Field | Value |
|---|---|
| Skills | `SKL-EXT`, `SKL-GRD` |
| Input | Interview transcript + partner name, role, date, service area |
| Output | KA-FLD records in Notion Knowledge Base: Title, KB ID, Claim, Detail, Source, Reuse Classification, Confidence, Topic Area, Tags, Partner Source relation |
| Human gate | Human reviews any records classified Internal Only or Do Not Use before downstream use |
| Guardrails | DO_NOT_USE triggers: corruption or improper influence implications; unsupported outcome guarantees (visas, tax, approvals); confidential partner methods or client data; tax evasion or regulatory bypassing; content that could create legal/reputational risk if surfaced by a chatbot |

---

### 10. Chatbot Knowledge Agent
**ID:** PRMT-AGT-015 *(to be built — Phase 2)*
**Platform:** chatbot.ai
**Stage:** Customer-facing
**Purpose:** Answer customer questions using KB records classified Safe to Use; route complex or sensitive queries to a human adviser.

| Field | Value |
|---|---|
| Skills | `SKL-RAG`, `SKL-GRD`, `SKL-TOV` |
| Input | Customer question → retrieves relevant KB records from Notion Knowledge Base (Reuse Classification = Safe to Use) |
| Output | Direct answer with source caveat; disclaimer on all legal, tax, immigration, and financial topics; escalation prompt when question is out of scope |
| Human gate | No real-time gate on individual responses — safety is enforced upstream via Reuse Classification on all KB records; chatbot configuration reviewed by human before go-live |
| Guardrails | Only consumes records with Reuse Classification = Safe to Use; never surfaces Internal Only, Do Not Use, or Needs Verification records; always appends standard disclaimer; never presents partner opinion as official legal, tax, or immigration advice; escalates anything involving specific personal circumstances |

*Note: KB Reuse Classification field must be fully populated before chatbot is trained on the Knowledge Base.*

---

### 11. Monthly Blog Refresh Agent
**ID:** PRMT-AGT-013 *(to be created — phase 2)*
**Stage:** Content maintenance (automated on schedule)
**Purpose:** Review published Markdown articles on a monthly cadence, verify facts against current sources, update where needed, and add/update the "Latest update as of {date}" info box.

| Field | Value |
|---|---|
| Skills | `SKL-RES`, `SKL-WRI`, `SKL-GRD` |
| Input | Published Markdown file + scheduled trigger (monthly) |
| Output | Updated Markdown file with tracked changes + summary of what changed and why + updated info box |
| Human gate | Human reviews diff before committing update; triggers site recrawl after approval |
| Guardrails | Only update facts that are verified against a named source; never silently remove disclaimers; flag any regulatory changes that may require broader content revision |

---

## Scheduled Remote Automations

These agents run automatically on a cron schedule via Claude Code Remote (CCR) at claude.ai/code/routines. They do not require manual activation.

| Name | Routine ID | Schedule | Status | Output |
|---|---|---|---|---|
| Weekly Content Pipeline Hygiene | trig_017VhqGhm6Uuj1GtwZjitLqp | Every Friday 6am UTC | Active | Hygiene report page created in PA-Marketing and Branding in Notion |
| Weekly Knowledge Lint (PRMT-AGT-004) | trig_01V16x3BTyDvrwgGJVZbnqDw | Every Monday 6am UTC | Active | Lint report committed to `paphos-advisor/research/lint-reports/` |

**Dependencies:**
- Both routines require the Claude GitHub App installed on the repo (bettysoarre/Paphos-advisors-system)
- Hygiene routine requires Notion MCP connector
- Lint routine requires repo access only

*Monthly Blog Refresh Agent (PRMT-AGT-013) will be added here as a scheduled routine once the website is live.*

---

## Pipeline Workflows

### Content Production Pipeline
```
[Topic / Brief Request]
        ↓
  Research Agent (PRMT-AGT-002)
  — Perplexity research, source citations
        ↓
  [Human: approve research package]
        ↓
  Brief Writer Agent (PRMT-AGT-006)
  — Structured brief, SEO targets, angle
        ↓
  [Human: approve brief, confirm scope]
        ↓
  Writer Agent (PRMT-AGT-001)
  — Full Markdown draft with flags
        ↓
  [Human: editorial review, accuracy check]
        ↓
  Publish → GitHub (MD source) → Notion sync
```

### Social Repurposing Pipeline
```
[Published / Approved Article]
        ↓
  Social Repurposing Agent (PRMT-AGT-007)
  — Per-platform drafts + visual briefs
        ↓
  [Human: approve each platform draft]
        ↓
  Manual post via Canva + scheduler
  (Phase 1 — manual)
  (Phase 2 — platform agents post to draft queue, human approves)
```

### Partner Knowledge Pipeline
```
[Partner Interview Transcript — Google Drive]
        ↓
  Save to repo (paphos-advisor/assets/transcripts/)
  Create Notion Interview record + Partner record
        ↓
  Knowledge Extraction Agent (PRMT-AGT-014)
  — KA-FLD records created in Notion KB
  — Reuse Classification applied to each record
        ↓
  [Human: review Internal Only + Do Not Use records]
        ↓
  Safe records available to Research Agent + Content Pipeline
  Safe records available to Chatbot (PRMT-AGT-015) once live
```

### Content Refresh Pipeline
```
[Monthly scheduled trigger]
        ↓
  Blog Refresh Agent (PRMT-AGT-013)
  — Fact-check, update, add info box
        ↓
  [Human: review diff, approve update]
        ↓
  Commit to GitHub → recrawl trigger
```

---

## Human-in-the-Loop Gates (Centralized)

| Gate | Agent | What human decides | What happens if skipped |
|---|---|---|---|
| Research approval | PRMT-AGT-002 | Research package is complete and reliable | Brief is built on bad or incomplete data |
| Brief approval | PRMT-AGT-006 | Angle, scope, and structure are correct | Writer drafts the wrong article |
| Content approval | PRMT-AGT-001 | Content is accurate, on-brand, ready to publish | Inaccurate or off-brand content reaches the site |
| Social approval | PRMT-AGT-007/008/009 | Post is accurate, appropriate, on-brand | Wrong, off-brand, or partial claims published publicly |
| PR outreach | PRMT-AGT-011 | Pitch is appropriate and sends from the right person | Agent sends unsolicited emails as the business |
| Refresh approval | PRMT-AGT-013 | Factual updates are correct and complete | Changed or removed content published without review |

---

## Brand Guardrails (Immovable Truths)

All agents must comply. These cannot be overridden by a prompt or brief.

1. **No falsehoods.** If a fact cannot be verified by a named source, write `[NEEDS SOURCE]` — never fill from assumption or general AI knowledge.
2. **Flag unverified items explicitly.** Use `[UNVERIFIED: describe what needs checking]` rather than writing around uncertainty.
3. **Note pending legislation.** Any reference to proposed, consulted, or transitional rules must be flagged: `⚠ This rule is subject to change — verify current status before publishing.`
4. **No regulated advice language.** Do not write "you should", "you must", or anything that implies legal, tax, or financial advice. Rephrase as process description.
5. **Strict brand rules before external publishing.** Tone, British English, and accuracy must be confirmed before any content goes live on the website or social platforms.
6. **Human sends PR outreach.** No agent initiates external communication on behalf of the business.
7. **Social is draft-only until validated.** No agent auto-publishes to any social platform until the human-approval workflow has been validated over 4–8 weeks of operation.

---

## Build Order

| Phase | Agents to build | Prerequisite |
|---|---|---|
| Phase 1 (now) | Brief Writer (PRMT-AGT-006) | Research Agent exists; content pipeline needs this link |
| Phase 1 (now) | Social Repurposing Agent (PRMT-AGT-007) | Content exists to repurpose; Canva templates needed |
| Phase 1 (now) | Knowledge Extraction Agent (PRMT-AGT-014) | Formalise current manual extraction into a repeatable agent; add Reuse Classification field to Notion KB schema |
| Phase 2 (May) | Blog Refresh Agent (PRMT-AGT-013) | Website live; GitHub–Notion sync in place; add as scheduled remote routine |
| Phase 2 (May) | Platform Social Agents IG/FB (PRMT-AGT-008/009) | Social Repurposing Agent validated; Canva templates built |
| Phase 2 (May) | Community Agent (PRMT-AGT-010) | Community playbook from Gratian (due 2026-05-05) |
| Phase 2 (May) | Chatbot Knowledge Agent (PRMT-AGT-015) | Platform: chatbot.ai; KB Reuse Classification fully populated; chatbot.ai connected as MCP or API source |
| Phase 3 (Jun+) | PR Agent (PRMT-AGT-011) | Core content pipeline stable; outreach templates ready |
| Phase 3 (Jun+) | Ads Analysis Agent (PRMT-AGT-012) | Campaign running; performance data available |

---

## ID Registry Updates Required

When creating new agents, increment the PRMT-AGT sequence in id-registry.md:

| Agent | ID to assign | Status |
|---|---|---|
| Brief Writer | PRMT-AGT-006 | Built |
| Social Repurposing | PRMT-AGT-007 | To build |
| Instagram Social | PRMT-AGT-008 | To build |
| Facebook Social | PRMT-AGT-009 | To build |
| Community/Reactive | PRMT-AGT-010 | To build |
| PR/Links | PRMT-AGT-011 | To build |
| Ads Analysis | PRMT-AGT-012 | To build |
| Blog Refresh | PRMT-AGT-013 | To build |
| Knowledge Extraction | PRMT-AGT-014 | To formalise |
| Chatbot Knowledge Agent | PRMT-AGT-015 | To build |
