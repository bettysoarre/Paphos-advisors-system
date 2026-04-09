# Partner Onboarding Checklist

This is the canonical checklist for onboarding a new partner into the Paphos Advisor network. Every partner must complete all seven stages before being activated. Do not skip stages or move a partner to "active" without completing the preceding steps.

**How to use this checklist:**
- Open the partner's Notion record alongside this checklist
- Work through each task in order — stages are sequential, not parallel
- Record findings, dates, and notes directly in the Notion Partner record as you go
- Only advance to the next stage when all tasks in the current stage are complete

---

**Partner Name:** ___________________________
**Partner Category:** ___________________________
**Onboarding Started:** ___________________________
**Onboarding Completed:** ___________________________
**Onboarding Owner:** ___________________________

---

## Stage 1 — Initial Assessment

*Objective: Determine whether this partner is worth pursuing before making contact. Avoid wasting time on partners with red flags or poor fit.*

- [ ] **Search the partner online** — review their website, Google reviews, LinkedIn, and any professional directory listings. Note overall web presence and professionalism.
- [ ] **Check regulatory status** — confirm they hold any required licences or professional registrations for their category (e.g. lawyers: Cyprus Bar Association; accountants: ICPAC; property agents: RICS or Land Registry agent licence). Note the registration number.
- [ ] **Search for any complaints or negative reports** — check Google reviews, Trustpilot, expat forums, and Cyprus Bar Association/ICPAC complaint registers where applicable.
- [ ] **Assess geographic coverage** — confirm they operate in Paphos or the district(s) where we need coverage. Note if they are Paphos-specific, multi-district, or island-wide.
- [ ] **Assess service gap fit** — identify which of our current service gaps this partner would fill. Is this a high-priority gap or a nice-to-have?
- [ ] **Document initial findings in the Notion Research Log** — create a Research Log entry with type `partner-research`, status `Captured`, and a Key Findings Summary covering: what they do, web presence, reputation, regulatory status, and fit assessment.
- [ ] **Make go/no-go decision** — is this partner worth pursuing? If yes, proceed to Stage 2. If no, document the reason in the Notion Partner record and archive the record.

**Stage 1 complete — date:** _______________

---

## Stage 2 — First Contact

*Objective: Make initial contact, introduce Paphos Advisors, and gauge whether the partner is interested in and suitable for the network.*

- [ ] **Identify the right contact person** — find the name and direct contact details for the most appropriate person to approach (senior partner, business development, owner-manager).
- [ ] **Send introductory message or email** — brief, professional introduction explaining who Paphos Advisors is, what we do, and why we are reaching out. Do not oversell or over-explain at this stage.
- [ ] **Book an introductory call or meeting** — aim for a 20–30 minute conversation. In-person preferred for Paphos-based partners.
- [ ] **Conduct introductory call/meeting** — cover:
    - [ ] What Paphos Advisors does and who our clients are
    - [ ] Our referral model and what we are looking for in a partner
    - [ ] What we can offer them (qualified, well-briefed referrals)
    - [ ] Their current capacity and interest in receiving referrals
- [ ] **Assess interest and fit** — do they understand our model? Are they interested? Do they communicate clearly and professionally? Would you trust them with a client?
- [ ] **Document outcome in Notion Partner record** — note: date of contact, who you spoke to, their reaction, any red or green flags, and whether to proceed.
- [ ] **Make go/no-go decision** — proceed to Stage 3 if interest and fit are confirmed. If not, update Onboarding Status to `not-started` and note the reason.

**Stage 2 complete — date:** _______________

---

## Stage 3 — Information Gathering

*Objective: Collect the factual information needed to populate the Notion Partner record and understand how to position this partner for referrals.*

- [ ] **Collect company/individual details:**
    - [ ] Full legal name of the firm or individual
    - [ ] Registered address and operating address(es)
    - [ ] Website URL
    - [ ] Primary contact name, email, and phone
    - [ ] Professional registration number(s)
    - [ ] Year established / years of experience
- [ ] **Document service areas in detail:**
    - [ ] Exactly which services do they offer? (Map to service-types.yaml values)
    - [ ] Which ICP segments do they typically work with?
    - [ ] Are there any services they do not offer or actively avoid?
- [ ] **Document geographic coverage:**
    - [ ] Which districts do they serve?
    - [ ] Do they have offices or do they work remotely?
    - [ ] Are there areas where their capacity is limited?
- [ ] **Document languages spoken:**
    - [ ] Which languages can they work in? (Client-facing, not just administrative)
    - [ ] Any languages they are particularly strong or weak in?
- [ ] **Understand pricing and commercial structure:**
    - [ ] How do they charge? (Fixed fee, hourly, percentage, retainer)
    - [ ] Do they have standard fee schedules they can share?
    - [ ] Are they open to discussing referral fee arrangements?
- [ ] **Understand turnaround times and capacity:**
    - [ ] What is their typical response time to new enquiries?
    - [ ] What is their current capacity for new clients?
    - [ ] Do they have busy/slow seasons that affect availability?
- [ ] **Request example client scenarios:**
    - [ ] Ask them to walk through 2–3 typical client cases they handle — this gives insight into their process knowledge and how they work in practice.
- [ ] **Update Notion Partner record** with all information gathered. All fields should be at least partially populated after this stage.

**Stage 3 complete — date:** _______________

---

## Stage 4 — Formal Interview

*Objective: Conduct a structured, recorded interview to extract deep process knowledge, practical tips, and field intelligence that will feed into the Paphos Advisor knowledge base.*

- [ ] **Explain the interview purpose to the partner** — frame it as a knowledge-sharing session that helps us send them better-qualified referrals. Be transparent that notes will be used internally.
- [ ] **Schedule the interview** — aim for 45–60 minutes. Video call or in-person. Use Plaud Note or equivalent for recording.
- [ ] **Prepare interview guide** — review the extraction prompt at [prompts/extraction/interview-extraction-prompt.md](../../prompts/extraction/interview-extraction-prompt.md) and prepare specific questions based on the partner's category and service areas. Tailor questions to the gaps in our current process documents.
- [ ] **Confirm recording consent** — obtain verbal confirmation on the recording that the partner consents to being recorded and to their knowledge being used internally by Paphos Advisors.
- [ ] **Conduct the interview** — ensure you cover:
    - [ ] Their services in detail — how each works step by step
    - [ ] Their process knowledge — what happens at each stage, what documents are required, what the government departments are like to deal with
    - [ ] Practical tips — what do clients commonly get wrong, what makes the process harder or easier
    - [ ] Common client issues — what problems do they see most often, how are they resolved
    - [ ] Current regulatory landscape — any recent changes, known upcoming changes, or areas of uncertainty
    - [ ] Paphos-specific field intelligence — anything specific to the Paphos offices or market that differs from the rest of Cyprus
- [ ] **Save the recording** — store in `assets/transcripts/` with filename format: `[YYYY-MM-DD]-[partner-slug]-interview.[format]`
- [ ] **Update Notion Partner record** — set Interview Completed checkbox to true. Note date and interviewer.

**Stage 4 complete — date:** _______________

---

## Stage 5 — Knowledge Extraction

*Objective: Convert the interview recording into structured, usable knowledge assets in GitHub and Notion.*

- [ ] **Transcribe the interview** — use Plaud Note's transcription, a transcription tool, or manual transcription. Save cleaned transcript to `assets/transcripts/` alongside the recording.
- [ ] **Run the interview extraction prompt** — use [prompts/extraction/interview-extraction-prompt.md](../../prompts/extraction/interview-extraction-prompt.md) with Claude. Paste the full transcript and follow the output format to generate draft knowledge article entries.
- [ ] **Review all extracted knowledge drafts** — check each KB-DRAFT entry for accuracy. Correct any misinterpretations of the interviewee's words. Flag any claims that require official source verification.
- [ ] **Verify claims flagged as `requires_verification: true`** — before promoting to knowledge articles, run verification against official sources using the process research prompt.
- [ ] **Investigate any contradictions flagged** — for any KB-DRAFT marked `contradicts_existing: true`, review the existing process document and determine which version is correct. Update the process document if the partner's field intelligence supersedes the existing guidance.
- [ ] **Create GitHub knowledge articles** — for each approved KB-DRAFT:
    - [ ] Use [knowledge/_templates/knowledge-article-template.md](../../knowledge/_templates/knowledge-article-template.md)
    - [ ] Assign the correct KB-[AREA]-[###] ID from [system/standards/id-registry.md](../../system/standards/id-registry.md)
    - [ ] Save to the correct `knowledge/[area]/` folder
    - [ ] Update id-registry.md with the new sequence numbers used
- [ ] **Update existing process documents** where the interview provides new field notes or corrects existing information — update the Field Notes or Common Issues section of the relevant PROC-XXX file.
- [ ] **Commit and push all new/updated files to GitHub.**
- [ ] **Update the Notion Research Log entry** — change status from `Captured` to `Integrated`. Update Key Findings Summary if new significant insights were added during extraction.

**Stage 5 complete — date:** _______________

---

## Stage 6 — Record Completion

*Objective: Ensure the Notion Partner record is complete and ready for active use by the team.*

- [ ] **Complete all Notion Partner record fields** — check every field is populated or deliberately left blank with a reason:
    - [ ] Partner Name, Category, Subcategory
    - [ ] Contact Person, Email, Phone, Website
    - [ ] Location, Service Areas
    - [ ] Languages
    - [ ] Interview Completed (should be checked)
    - [ ] Active Since (date the partner relationship began)
- [ ] **Set Trust Level to `probationary`** — all new partners start as probationary regardless of reputation. Trust level is upgraded after the first successful referral outcomes and the 90-day review.
- [ ] **Document Commercial Terms** — record agreed fee arrangements, commission rates, referral terms, or any special arrangements in the Commercial Terms and Referral Fee Structure fields. If no commercial arrangement exists yet, note "informal arrangement — to be formalised."
- [ ] **Document any known caveats** — note in Internal Trust Notes anything the team should know: areas of weakness, capacity limits, communication style notes, or anything that affects how we work with this partner.
- [ ] **Set Contract on File checkbox** — check if a formal written agreement exists. If not, note the current arrangement and flag for formalisation.
- [ ] **Add GitHub Profile Path** — link to the partner's GitHub profile page (if created) or note the path where their knowledge articles are stored.
- [ ] **Set Onboarding Status to `onboarded`** — do not set to active until Stage 7 is complete.
- [ ] **Peer review the record** — have a second team member review the completed record for accuracy and completeness before activation.

**Stage 6 complete — date:** _______________

---

## Stage 7 — Activation

*Objective: Make the partner operational — visible to the team for referrals, with content and review infrastructure in place.*

- [ ] **Create referral workflow entry if needed** — if this partner handles a specific referral type that requires a documented workflow, create or update the relevant workflow file in `workflows/referral-pipeline/`.
- [ ] **Add partner to relevant process documents** — update the `related_partners` field in the relevant PROC-XXX process documents to include this partner's category.
- [ ] **Plan partner page content** — create a Content Pipeline entry in Notion for a partner profile page (content type: `partner-page`) linked to this partner's record. Set status to `idea` or `briefed` depending on priority.
- [ ] **Brief the team** — if the partner fills a significant gap or will receive a high volume of referrals, brief relevant team members on who they are, what they do, and how to refer clients to them.
- [ ] **Set Onboarding Status to `active`** — the partner is now live in the network.
- [ ] **Set Last Contact Date** to today's date.
- [ ] **Schedule the 90-day review** — set Next Review Date to 90 days from today. The 90-day review assesses: have we referred any clients, how did the partner perform, should trust level be upgraded from probationary, are there any issues to address.

**Stage 7 complete — date:** _______________

---

## Onboarding Sign-Off

| | Name | Date |
|---|---|---|
| **Onboarding Owner** | | |
| **Reviewer** | | |

**Partner activated and ready for referrals:** ☐ Yes

---

## Related Documents

- [Partner Onboarding SOP](../../sops/partners/) — the SOP governing this checklist and who is responsible for each stage
- [Interview Extraction Prompt](../../prompts/extraction/interview-extraction-prompt.md) — used in Stage 5
- [Knowledge Article Template](../../knowledge/_templates/knowledge-article-template.md) — used in Stage 5
- [ID Registry](../../system/standards/id-registry.md) — for assigning KB article IDs
- [Notion Partners Database](https://www.notion.so/) — the live partner record
- [Review Cadences](../../system/governance/review-cadences.md) — for setting the 90-day review schedule
