---
id: PRMT-ANL-003
title: ICP Needs Analysis Prompt
type: analysis
tool: claude
version: "1.0"
created: 2026-04-13
updated: 2026-04-13
output_format: Updated ICP segment profile with data-driven insights
use_with: icps/segments/, icps/mapping/
---

# ICP Needs Analysis Prompt (PRMT-ANL-003)

## Purpose
Analyse case data, client questions, and content performance to update an ICP segment profile with real-world intelligence. Used quarterly to keep ICP profiles grounded in actual client behaviour.

## Tool
Claude

---

## Prompt

```
You are updating the ICP profile for [ICP SEGMENT NAME] for Paphos Advisors based on real data from cases, client questions, and content performance.

CURRENT ICP PROFILE:
[PASTE THE CURRENT icps/segments/[segment].md CONTENT]

DATA TO ANALYSE:

CASE DATA (last [N] months):
[PASTE RELEVANT CASE NOTES, ANONYMISED — client type, processes needed, questions asked, pain points noted]

CLIENT QUESTIONS CAPTURED (from case notes and content comments):
[LIST ACTUAL QUESTIONS CLIENTS OF THIS SEGMENT HAVE ASKED]

CONTENT PERFORMANCE (if available):
[WHICH PAGES DO PEOPLE IN THIS SEGMENT LAND ON / CONVERT FROM]

INSTRUCTIONS:
1. Compare the current ICP profile against the actual data
2. Identify:
   a. Profile elements that are confirmed by data (mark with ✓)
   b. Profile elements that are contradicted or need updating (mark with ⚠)
   c. New insights that are not in the current profile (mark with ★ NEW)
3. Draft the updated sections of the ICP profile with changes highlighted
4. Update the "Processes Required" list if cases show different process combinations than assumed
5. Update the "Content They Are Looking For" list with actual questions from the data
6. Add any new service package ideas based on patterns in the case data
7. Note the data sample size and any limitations on the analysis

OUTPUT:
- Summary of key changes
- Updated ICP profile sections (only sections that changed)
- Data confidence note: how much data was this based on?
```

---

## How to Use

1. Run quarterly, or after 10+ cases from a specific ICP segment have been closed
2. Pull anonymised case notes from Notion
3. Run in Claude
4. Update the ICP segment file in GitHub
5. Review ICP-to-service and ICP-to-content mappings for any needed updates
