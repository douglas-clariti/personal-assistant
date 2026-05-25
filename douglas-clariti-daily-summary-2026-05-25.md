---
date: "2026-05-25"
weekday: "Monday"
author: "douglas-clariti"
quality: "complete"
sources_used:
  - google_calendar
  - slack
sources_empty:
  - gmail
  - google_drive
open_loops_carried: 1
tags:
  - project-surf
  - cell-architecture
  - byoc
  - aws
  - bmad
  - cloudflare
  - base64
  - clariti
---

# Daily Summary — Monday, May 25, 2026

## Summary

Day focused on advancing the Project Surf cell architecture proposal — shared the final design document and PR #113 with Samuel Couture, Herman Chan, and Justin LaBrash in #project-surf-how-track, got team alignment to remove the BYOC use case (Scenario C), and committed to that change being in progress. Two meetings: the recurring Douglas/Justin Daily [bmad] standup and a Progress Check-In organized by Douglas with Aman Bhalla, Samuel Couture, and Justin LaBrash.

- Attended "Douglas / Justin Daily [bmad]" with Justin LaBrash (organizer) via Google Meet, 9:30–9:45 AM EDT (transcript not available).
- Organized and attended "Progress Check-In" with Aman Bhalla (optional), Samuel Couture, and Justin LaBrash via Google Meet, 1:00–1:20 PM EDT (transcript not available).
- Shared final cell architecture proposal for the week in #project-surf-how-track, tagging Samuel Couture, Herman Chan, and Justin LaBrash — linked PR #113 and cells-byoc-and-customer-paced-releases.md; asked team to sanity-check scope and the 4-day implementation plan.
- Confirmed with Samuel Couture and Justin LaBrash that BYOC is not a requirement in the RFPs; committed to removing BYOC (Scenario C) from the proposal, confirming the change is already in progress.
- Posted FYI update in #project-surf-how-track that the prime was updated to use base64 images; noted remaining challenge with handling images pasted directly into chat (Claude working on the solution).
- Replied to Dipak Parmar in DM that the Cloudflare request has not yet been tried.
- Confirmed with Justin LaBrash via DM that the PRD for Surf was merged to main.

## Decisions & Rationale

- **BYOC (Scenario C) removed from cell architecture proposal**: Samuel Couture confirmed no BYOC requirement exists in the RFPs; Justin LaBrash corroborated; Douglas committed to removing it, already in progress — keeps scope realistic and aligned with actual RFP constraints.
- **Cell architecture 4-day plan approved for the week**: Samuel Couture reviewed the plan and confirmed it looks good with BYOC scenario removed — enables focused execution this week.

## Open Loops

- **Expensify access** (carried from 2026-04-17) (stale — consider closing or escalating): Requested from accounting@claritisoftware.com; no update received today.
- **AWS dedicated account per customer onboarding**: Douglas asked in #project-surf-how-track whether Clariti creates dedicated AWS accounts per customer under its AWS Organization — Samuel Couture is unsure; needs clarification from infrastructure team.
- **Cloudflare request**: Dipak Parmar followed up today; Douglas has not yet attempted the request — needs to be tried.
- **Base64 image paste in chat**: Prime updated to use base64 images, but the workflow for handling images copied directly into the chat is still unsolved.

## Blockers

No blockers identified today.

## Next Steps

- Complete the BYOC removal in PR #113 and push the updated cells-byoc-and-customer-paced-releases.md.
- Clarify whether Clariti uses dedicated AWS accounts per customer during onboarding (follow up with Samuel Couture or Justin LaBrash).
- Try the outstanding Cloudflare request (follow up with Dipak Parmar).
- Continue resolving the image-paste-to-chat workflow for the prime (track Claude's solution).
- Escalate or close Expensify access request with accounting@claritisoftware.com.

## Transcript Source (Cleaned)

The day started with the recurring Douglas/Justin Daily [bmad] standup at 9:30 AM EDT (15 minutes, Justin LaBrash organizer, Google Meet — no transcript linked). At 1:00 PM EDT Douglas organized the Progress Check-In with Aman Bhalla (optional), Samuel Couture, and Justin LaBrash (20 minutes, Google Meet — no transcript linked).

The main Slack activity was in #project-surf-how-track. At 4:30 PM EDT, Douglas posted his final cell architecture proposal for the week, tagging Samuel Couture (Samuel CB), Herman Chan, and Justin LaBrash, sharing PR #113 and the cells-byoc-and-customer-paced-releases.md document. He asked the team to assess whether the scope was meaningful and whether the 4-day implementation plan was too conservative. Samuel Couture quickly confirmed there's no BYOC requirement in the RFPs, and Justin LaBrash corroborated. Samuel reviewed the plan and said it looks good with BYOC (Scenario C) removed. Douglas responded that he would remove BYOC and that the change was already in progress. Douglas also raised a separate question about whether Clariti creates dedicated AWS accounts per customer during onboarding — Samuel Couture said he was unsure.

Earlier in the day (1:20 PM EDT), Douglas posted an FYI in #project-surf-how-track that the prime had been updated to support images as base64, but that handling images pasted directly into the chat remains an open problem (with Claude working on a solution).

In a DM with Dipak Parmar (2:00 PM EDT), Dipak followed up on a Cloudflare request; Douglas replied that he hadn't yet tried it. In a DM with Justin LaBrash (10:33–10:35 AM EDT), Douglas confirmed the Surf PRD changes were merged to main. No outbound emails were identified today (action_only mode; Gmail returned no results).
