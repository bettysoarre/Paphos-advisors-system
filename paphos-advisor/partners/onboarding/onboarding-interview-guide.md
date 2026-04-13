# Partner Onboarding Interview Guide

## Purpose
A structured guide for conducting the formal partner knowledge interview (Stage 4 of the partner onboarding checklist). This interview has two goals:
1. Extract practical, field-level knowledge that updates our process documentation
2. Establish the relationship and understand how the partnership will work in practice

## Setup

**Recording:** Use Plaud Note to record the interview. Confirm the partner has consented to recording at the start of the call.

**Transcript:** Export the recording and save to `assets/transcripts/transcript-[partner-slug]-[YYYY-MM-DD].txt`

**Post-interview:** Run `prompts/extraction/interview-extraction-prompt.md` (PRMT-EXT-001) against the transcript.

**Duration:** 45-60 minutes

---

## Opening (5 minutes)

Introduce the structure:
> "Thanks for taking the time. The goal today is twofold — I want to understand your practice in depth so we can make smart referrals, and I want to capture your practical knowledge about the processes you handle, because we document everything so our advisors give clients accurate information. I'll be taking notes and recording for our own documentation. Is that OK?"

---

## Section 1: Their Practice (10 minutes)

Understand what they do day to day — not their website blurb, but what cases they actually handle.

Questions:
1. Walk me through the typical case you handle — what kind of client, what process, how it works.
2. What percentage of your clients are expats vs local Cypriots?
3. What nationalities do you most commonly work with?
4. What do you NOT do — what would you refer to someone else?
5. What does your usual fee structure look like? (Not exact figures — just fixed fee, hourly, etc.)

---

## Section 2: Process Knowledge — Deep Dive (25 minutes)

This is the core intelligence extraction. Focus on the processes most relevant to their category. Use the question bank below; do not try to cover all of them — go deep on 3-4 key areas.

### Immigration (for immigration lawyers)
- What are the most common mistakes people make when applying for a Yellow Slip?
- What does the Paphos CRMD actually require that is NOT on their official website?
- How long is it REALLY taking at the moment at the Paphos office?
- What documentation do you see rejected most often, and why?
- Do they still require a Tax-stamped rental agreement now that stamp duty is abolished?
- What income evidence do officers actually look for, even though there is no official minimum?
- Any recent changes you have noticed in how the office is processing applications?

### Tax (for tax advisors)
- Walk me through how you establish Cyprus tax residency for a new client under the 60-day rule.
- What do clients most commonly get wrong about the 60-day rule?
- Is the "no other tax residency" condition genuinely no longer required since the 2026 change?
- What does the Non-Dom clock start from, in your experience?
- What documentation does the tax office actually ask for vs what is officially required?
- Any nuances around GHS/GESY and Non-Dom clients that clients are usually surprised by?

### Property (for property agents)
- What is the real picture on title deeds in Paphos right now?
- What should a buyer absolutely check before signing a purchase contract?
- For EU nationals renting — what do landlords typically require, and what is realistic in the current market?
- Are landlords cooperative about getting contracts stamped at the tax office?
- What is the realistic timeline from offer to completion?
- Any areas of Paphos you would steer certain client types towards or away from?

### Business (for company formation specialists)
- What does a director need to have in place to demonstrate economic substance?
- What are the most common delays in the HE company formation process?
- What do you see going wrong with IP Box applications?

---

## Section 3: Practical Partnership Questions (10 minutes)

1. How do you prefer to receive referrals? (Warm introduction email? Call first?)
2. What information do you need about a client before your first call with them?
3. How quickly can you typically take on a new client enquiry?
4. What capacity do you have at the moment for new clients?
5. How would you let us know if you have a client who could benefit from our services? (Referral back)
6. Are you happy for us to add you to our partner network and eventually feature you on our website?

---

## Section 4: Open Questions (5 minutes)

- Is there anything about your area of practice that you find our kind of clients are consistently confused about?
- What would make your ideal referral from us?
- Anything you want to ask us about how we work?

---

## Closing

Thank them for their time. Confirm next steps:
- You will share a draft of their partner profile before publishing anything
- You will be in touch when you have a relevant client to refer
- Agree the referral introduction format

---

## After the Interview

1. Save transcript to `assets/transcripts/`
2. Run PRMT-EXT-001 on the transcript
3. Create KB articles from extracted intelligence
4. Update relevant process documents
5. Update Research Log to `Integrated`
6. Proceed to Stage 6 (Record Completion) of the onboarding checklist
