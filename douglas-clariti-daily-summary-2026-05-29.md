---
date: "2026-05-29"
weekday: "Friday"
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
  - workos
  - engineering-monthly
  - sprint-planning
  - cells-architecture
  - clariti
  - onildo
  - ian-driscoll
---

# Daily Summary — Friday, May 29, 2026

## Summary

A full-meeting day anchored by the Engineering Monthly presentation, sprint ceremonies, and a WorkOS access investigation. Douglas updated the How Track final presentation with cells-MVP-architecture diagrams, confirmed with Justin LaBrash he was ready to present Surf's cell architecture at the Engineering Monthly, and attended four meetings. In the afternoon, Samuel Couture Brochu raised that Onildo should be onboarded sooner; Douglas committed to reaching out today. Late in the day Douglas hit a WorkOS access blocker — Clariti has an existing claritisoftware.com WorkOS account with no known owner — and investigated via DMs with Dipak Parmar, Craig Stickel, and Colin John, landing on a recovery path through archival mailboxes.

- Attended "Douglas / Justin Daily" standup with Justin LaBrash, 9:30–9:45 AM EDT (transcript not available); Justin praised CLI progress; Douglas briefly delayed due to a family interruption.
- Updated the How Track final presentation per Justin LaBrash's request and shared the cells-MVP-architecture GitHub link (`project-surf/docs/cells-mvp-architecture.md`) in #project-surf-how-track, tagging Samuel Couture Brochu and Justin LaBrash.
- Confirmed with Justin LaBrash via DM that he was prepared to present Surf's cell architecture at the Engineering Monthly.
- Attended "How Track - Weekly Review" with Justin LaBrash, Timothy Meyer, Samuel Couture Brochu, and Ian Driscoll (tentative), 12:00–12:30 PM EDT (transcript not available); Herman Chan declined (OOO).
- Noticed Samuel Couture Brochu's "Career Development & Coaching" session conflicted with Sprint Planning, offered to shift the time; Samuel opted out of Sprint Planning instead.
- Agreed with Samuel Couture Brochu that Onildo should be engaged as soon as phase 0 completes; committed to reaching out to Onildo today to gauge interest, start date, and expectations.
- Made first contact with Ian Driscoll via DM; expressed interest in his Claude + Codex + agents work; Ian offered to book calendar time.
- Attended ad-hoc "Douglas / Justin" sync, 1:15–1:45 PM EDT (transcript not available); initiated by Douglas to align on Engineering Monthly content.
- Attended "Sprint Planning" with Justin LaBrash and Samuel Couture Brochu, 2:00–2:30 PM EDT (transcript not available).
- Attended "Engineering Monthly" with the Clariti Engineering team, 4:00–5:00 PM EDT (transcript not available); Herman Chan was organizer but was OOO.
- Investigated WorkOS access blocker for Surf project: DMed Dipak Parmar (referred to Craig Stickel), contacted Craig Stickel (no vault credentials found; traced history to Camino/Auth0 era), then pulled Dipak and Colin John into a group DM; Dipak directed Colin to search archival mailboxes (Mike, Joel, Nick) for the original WorkOS account owner.

## Decisions & Rationale

- **Onildo to be engaged sooner**: Samuel Couture Brochu and Douglas aligned that Onildo should be brought in at the end of phase 0, or earlier, to avoid a resourcing gap; Douglas will reach out today to check interest and start expectations.
- **WorkOS recovery via archival mailboxes**: Since no vault credentials exist for the claritisoftware.com WorkOS account, account recovery through archival inboxes of former DevOps/EM team members (Mike, Joel, Nick) was identified as the path forward — creating a new account would conflict with the existing tenant.

## Open Loops

- **Expensify access** (carried from 2026-04-17): Requested from accounting@claritisoftware.com for train ticket expenses from the Lévis offsite — no evidence of resolution today.
- **WorkOS account recovery**: Colin John searching archival mailboxes (Mike, Joel, Nick) to identify the original claritisoftware.com WorkOS account owner; unresolved as of end of day.
- **Outreach to Onildo**: Douglas committed to contact Onildo today to gauge interest and expectations — not yet confirmed done.
- **Meeting with Ian Driscoll**: Ian Driscoll to schedule calendar time to discuss Claude + Codex + agents work — pending calendar invite.

## Blockers

- **WorkOS access for Surf**: No known owner of the claritisoftware.com WorkOS account; progress blocked pending Colin John's search of archival mailboxes.

## Next Steps

- Follow up with Colin John and Dipak Parmar on WorkOS account recovery results.
- Reach out to Onildo to gauge interest, availability, and expectations for joining the Surf team.
- Accept or confirm meeting with Ian Driscoll on Claude + Codex + agents.
- Confirm Expensify access resolution with accounting@claritisoftware.com (open since 2026-04-17).
- Continue Surf phase 0 execution; plan phase 1 resourcing once Onildo is confirmed.

## Transcript Source (Cleaned)

The day opened with the "Douglas / Justin Daily" at 9:30 AM EDT — Justin praised Douglas's CLI progress and asked to sync quickly; Douglas joined a few minutes late due to a family interruption (daughter's diaper incident). In #project-surf-how-track, Justin asked Douglas to link a video of the prototype to the How Track final presentation; Douglas updated the presentation and also posted the cells-MVP-architecture GitHub diagram link for Samuel Couture Brochu and Justin. Via DM, Justin confirmed Douglas was prepared to present Surf's cell architecture at the Engineering Monthly — Douglas confirmed.

At 12:30 PM, Douglas noticed Samuel Couture Brochu's "Career Development & Coaching" session conflicted with the 2:00 PM Sprint Planning and offered to shift the time; Samuel said he wouldn't attend Sprint Planning. Samuel then raised that Onildo should be brought on as soon as phase 0 is done, or sooner — Douglas agreed and committed to reaching out to Onildo that day. Samuel also mentioned Jessica is now joining the team.

Also at 12:30 PM, Douglas introduced himself to Ian Driscoll via DM, asked about Ian's Claude + Codex + agents work, and agreed to schedule time to connect.

At 1:13 PM Douglas DMed Justin asking for a moment; Justin immediately created the "Douglas / Justin" ad-hoc meeting at 1:15 PM. Sprint Planning with Justin and Samuel followed at 2:00 PM.

Between 4:05 and 4:32 PM, Douglas investigated a WorkOS access blocker: Clariti has an active claritisoftware.com WorkOS account with no known owner. He first DMed Dipak Parmar, who directed him to Craig Stickel. Douglas reached out to Craig for the first time, explained the Surf WorkOS setup need, and shared a screenshot. Craig checked the vault (nothing), did Slack archaeology (found WorkOS was explored as an Auth0 replacement historically; the Camino founders knew WorkOS founders), and directed back to Dipak and Colin since the claritisoftware.com domain suggests a post-acquisition migration. Douglas then opened a group DM with Dipak and Colin John, sharing Craig's findings; Dipak recommended Colin search archival mailboxes of former team members (Mike, Joel, Nick) for the original account owner. The Engineering Monthly ran 4:00–5:00 PM with the Clariti engineering team; Herman Chan organized but was out of office.
