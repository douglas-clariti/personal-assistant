---
date: "2026-04-24"
weekday: "Friday"
author: "douglas-clariti"
quality: "complete"
sources_used:
  - google_calendar
  - slack
sources_empty:
  - gmail
open_loops_carried: 1
tags:
  - project-surf
  - super-bmad
  - project-what-track
  - sprint-review
  - sprint-planning
  - kanban
  - expensify
  - clariti
---

# Daily Summary — Friday, April 24, 2026

## Summary

Sprint 1 review and Sprint 2 planning day. Ran three back-to-back meetings (Weekly Review, Sprint Planning, Engineering Monthly), shipped the project-what-track repo with sbmad pre-installed, created and shared a Sprint Review document, and continued progressing the Expensify expense ticket with Samuel.

- Attended Weekly Review (2:30–3:15 PM EDT) via Google Meet with Justin Labrash (organizer), Aman Bhalla, Herman Chan, Samuel Couture, and Timothy Meyer — Sprint 1 review and demo session (transcript not available).
- Attended Sprint Planning (3:15–4:00 PM EDT) via Google Meet with Justin Labrash (organizer) and Samuel Couture (optional) — scoped Sprint 2 work (transcript not available).
- Attended Engineering Monthly (4:00–5:00 PM EDT) via Google Meet organized by Herman Chan — monthly engineering knowledge-sharing session with the broader Clariti Engineering, DevOps, and QA team (transcript not available).
- Added Justin Labrash and Aman Bhalla as GitHub administrators of the Project What Track repo (clariti-labs/project-what-track) and confirmed the repo works out of the box.
- Pushed sbmad setup to project-what-track so no manual install is required; confirmed board is functional via DM with Justin Labrash (no static URL yet).
- Created Sprint Review Document (Google Slides) and shared it with the team in #project-surf-how-track ahead of the Weekly Review; noted Kanban board as primary Sprint 1 deliverable and proposed adding BMAD/Claude Design screenshots as visuals.
- Shared super-bmad PR #58 (skill integration) in #project-surf-how-track during the sprint review slide discussion.
- Weighed in on product briefs repo question in #project-surf-how-track: no strong preference between a third repo or project-surf; Justin decided to demo in Surf for now and create a separate repo when needed.
- Provided Via Rail expense breakdown to Samuel Couture via DM: $64.62 (modified first leg) + $113.66 (new return ticket) = $178.28 total; noted inability to edit or delete the existing Expensify item.

## Decisions & Rationale

- **Product briefs repo: use project-surf for now**: Douglas signaled no strong preference; Justin resolved to demo in the project-surf repo and defer a third repo until the interaction model with super-bmad is clearer.
- **Sprint review visuals: screenshots of Kanban + BMAD/Claude Design interactions**: Sprint 1 had no visual artifacts beyond the Kanban board; Douglas proposed adding interaction screenshots to make the review presentation more concrete for non-technical stakeholders.
- **project-what-track ships with sbmad pre-installed**: Pushed the setup so admins can use the repo right out of the box without a separate install step.

## Open Loops

- **Expensify access / train ticket expenses** (carried from 2026-04-17): Detailed expense breakdown communicated to Samuel Couture today ($178.28 total: $64.62 + $113.66). Cannot edit or delete the existing Expensify item; accounting@claritisoftware.com response still pending.
- **Static URL for project-management board**: Board is functional but no stable public URL yet; noted to Justin Labrash in DM.

## Blockers

- Cannot edit or delete the existing Expensify item to correct the train ticket entry — waiting on accounting@claritisoftware.com to grant access or resolve it directly.

## Next Steps

- Follow up with accounting@claritisoftware.com on Expensify access and the train ticket expense submission.
- Resolve static URL for the project-management board.
- Work on Sprint 2 epics following today's sprint planning (Justin Labrash flagged this before the planning session).
- Have Justin Labrash and Aman Bhalla test and confirm Project What Track is working after being added as admins.
- Continue improving Sprint Review slide format: incorporate BMAD/Claude Design interaction screenshots for next review.

## Transcript Source (Cleaned)

The day consisted of three consecutive meetings in the afternoon. The Weekly Review (2:30–3:15 PM EDT) brought together the full project-surf pod — Justin Labrash, Aman Bhalla, Herman Chan, Samuel Couture, and Timothy Meyer — for Sprint 1 review and demo via Google Meet. It was immediately followed by Sprint Planning (3:15–4:00 PM EDT) with Justin Labrash and Samuel Couture to scope Sprint 2. The final meeting was Engineering Monthly (4:00–5:00 PM EDT), a recurring Herman Chan-organized session for the broader Clariti Engineering, DevOps, and QA group covering engineering direction and team knowledge-sharing. No transcripts were linked for any of these meetings.

Earlier in the day, Douglas drove several delivery actions in Slack. In #project-surf-how-track, he responded to Justin's question about where to store product briefs, offered a neutral take (third repo or project-surf), and Justin resolved to use project-surf for now. Douglas then added Justin Labrash and Aman Bhalla as GitHub administrators of project-what-track and confirmed the repo is functional with sbmad pre-installed. He confirmed the project-management board is working in a DM with Justin, with the only remaining gap being a static URL. Ahead of the Weekly Review, Douglas created and shared a Sprint Review Document (Google Slides) in #project-surf-how-track, flagging that Sprint 1 visuals are limited to the Kanban board and proposing BMAD/Claude Design screenshots as supplements. During that thread, he also shared super-bmad PR #58 adding the skill component. Post-review, he sent Samuel a DM acknowledging some nervousness during the demo and expressing confidence for Sprint 2.

In a separate DM with Samuel Couture in the morning, Douglas explained the Via Rail ticket history in detail: the original $130.68 ticket was modified (removing the return leg) to $64.62, and a new return was purchased separately for $113.66, bringing the total to $178.28 across two receipts — due to how Via Rail handles modifications. He noted he cannot edit or delete the Expensify item himself.
