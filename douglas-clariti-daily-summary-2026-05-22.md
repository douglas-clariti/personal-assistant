---
date: "2026-05-22"
weekday: "Friday"
author: "douglas-clariti"
quality: "partial"
sources_used:
  - google_calendar
  - slack
sources_empty:
  - gmail
  - google_drive
open_loops_carried: 1
tags:
  - project-surf
  - super-bmad
  - bmad
  - sprint-planning
  - how-track
  - primer
  - loom
  - what-track
  - clariti
---

# Daily Summary — Friday, May 22, 2026

## Summary

Sprint review and planning day: organized a Phase 2 prototype sync with Justin Labrash, attended the How Track weekly review with the full team, and ran sprint planning. Updated the sprint summary primer with two Loom demo recordings and shared them in #project-surf-how-track. Advised Justin Labrash on the correct super-bmad skill update workflow, reinforcing the BMAD sprint cycle as the required process for maintaining audit context. Confirmed `_bmad-output` as the right home for what track "capture findings" artifacts. Justin wrapped the week with positive feedback.

- Organized and led "Sync: Phase 2 Prototype" with Justin Labrash at 9:30–9:45 AM EDT via Google Meet (transcript not available).
- Attended "How Track - Weekly Review" (organizer: Justin Labrash) at 12:00–12:30 PM EDT with Justin Labrash, Samuel Couture Brochu, Aman Bhalla, Timothy Meyer, and Herman Chan (transcript not available).
- Attended "Sprint planning" at 1:30–2:00 PM EDT with Justin Labrash and Samuel Couture Brochu via Google Meet (transcript not available).
- Updated the sprint summary primer (sprint-summary-2026-05-21.html) and published two Loom demo recordings (Part 1, Part 2) in #project-surf-how-track in response to Justin Labrash's request to attach demo links to the presentation.
- Shared the BMAD roadmap link in #project-surf-how-track and noted that the sprint's evals and agent tests work aligns with upcoming BMAD releases; discussed "bmad in a box" (self-hosted/managed with SSO) with Justin Labrash and Herman Chan.
- Advised Justin Labrash via DM to use the full BMAD sprint cycle (PRD → stories → PR) for updating the design skill and cost tracking rather than using Claude directly, to preserve documentation context in the super-bmad repo.
- Confirmed with Justin Labrash via DM that moving "capture findings" from docs to `_bmad-output` is the right approach for the what track.
- Trivia Social hosted by Kate Dearness and the Community & Culture Committee at 6:00 PM EDT, solo-format trivia competition with a $75 prize for top 3 (attendance not confirmed).

## Decisions & Rationale

- **`_bmad-output` designated for what track "capture findings"**: Justin Labrash proposed moving these artifacts out of docs; Douglas confirmed no issues and directed them to `_bmad-output` — consistent with how the how track manages output artifacts.
- **BMAD sprint cycle required for super-bmad skill updates**: When Justin asked whether to use Claude directly or run a BMAD sprint to update the design skill and cost tracking, Douglas recommended the full BMAD cycle (PRD → stories → test → PR) so that future maintainers — including Claude when updating skills — have full context in the super-bmad repo rather than undocumented changes.

## Open Loops

- **Expensify access**: Requested from accounting@claritisoftware.com on 2026-04-17 — no update captured in any subsequent summary (carried from 2026-04-17; 35+ calendar days without resolution).
- **Primer image rendering**: Samuel Couture Brochu flagged in #project-surf-how-track that the primer skill needs to save images as base64 rather than in an asset folder, as images don't render in the current HTML output — assigned implicitly to the team for the next sprint.

## Blockers

No blockers identified.

## Next Steps

- Follow up with accounting@claritisoftware.com on Expensify access (opened 2026-04-17, no resolution captured).
- Coordinate with Samuel Couture Brochu to fix primer skill to save images as base64 (flagged in #project-surf-how-track today).
- Justin Labrash to proceed with design skill and cost tracking update via BMAD sprint cycle — Douglas to support when skill update context is needed.
- Continue sprint cadence next week: daily standups, mid-sprint check-ins, and next Friday review/planning.

## Transcript Source (Cleaned)

Friday began with a short Phase 2 Prototype sync at 9:30 AM that Douglas organized with Justin Labrash (15 min, Google Meet, no transcript linked). At noon, the full How Track team — Justin Labrash, Samuel Couture Brochu, Aman Bhalla, Timothy Meyer, and Herman Chan — joined the weekly review meeting organized by Justin (30 min, no transcript linked).

Before the sprint planning meeting, Justin had tagged Douglas in #project-surf-how-track asking him to update the sprint primer draft (PR #329) by adding the Loom demo link to slide 2. Samuel Couture Brochu also asked Douglas to share the demo link in the channel. Douglas confirmed, updated the primer, and shared both the published HTML presentation (sprint-summary-2026-05-21.html in `_bmad-output`) and two Loom demo recordings in the thread at 12:39 PM. Samuel then flagged that the primer skill needs to save images as base64 since the asset folder approach doesn't render them in the HTML output. Sprint planning ran at 1:30 PM with Justin and Samuel (30 min, no transcript).

In a separate DM thread, Justin asked Douglas whether updating the design skill and cost tracking warranted a full BMAD sprint or could just be done with Claude. Douglas recommended the BMAD route — explaining that the super-bmad repo is the "product/brain" of their agents, and that PRDs and stories are necessary so future skill maintainers have the context of what was changed and why. Justin accepted the recommendation.

At 4:23 PM, Douglas posted the BMAD roadmap link in #project-surf-how-track, noting that the evals and agent tests work done last sprint is coming in upcoming BMAD releases — validating the sprint direction against upstream. This kicked off a brief discussion with Justin and Herman Chan about "bmad in a box" (self-hosted or managed) and why SSO is on the BMAD roadmap. Later, Justin asked Douglas in DM if moving "capture findings" out of docs would cause any issues for the what track; Douglas said no problem and directed them to `_bmad-output`. Justin closed the week with "Once again awesome week dude!" and Douglas agreed. A Community & Culture Trivia Social was on the calendar for 6:00 PM EDT (Kate Dearness, Russell Zwicker, and the broader employee group), but Douglas's attendance was marked as not responded.
