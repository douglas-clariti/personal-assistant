---
date: "2026-10-09"
weekday: "Friday"
author: "douglas-clariti"
quality: "partial"
sources_used:
  - google_calendar
  - slack
sources_empty:
  - gmail
  - google_drive
open_loops_carried: 0
tags:
  - project-surf
  - qa
  - product-acceptance
  - sprint-planning
  - devops
  - t3
  - database
  - onboarding
---

# Daily Summary — Friday, October 9, 2026

## Summary

End-of-sprint Friday for Project Surf: a packed afternoon of sprint ceremonies (demo, stand-up, planning), a QA hand-off post asking product to accept 24 stories, two 1:1 knowledge-transfer sessions, and a new DevOps sync Douglas set up with Dipak Parmar. Gmail could not be read this run (re-authentication needed), so email activity is missing.

- Helped Tasmia Shefa with her T3 account in "Douglas / Tasmia - Quick sync on T3", 10:00–11:00 AM EDT (transcript available).
- Attended "Project Surf - End of Sprint Demo/Check-in" with the Surf team, 12:30–1:00 PM EDT (transcript available; recording and chat in Drive).
- "Project Surf Stand-up" was on the calendar, 1:00–1:30 PM EDT, with Douglas's RSVP still unanswered (transcript available).
- Attended "Surf Build - Sprint Planning" with Karan Kapoor, Craig Stickel, Amrita Patra, Eric McClelland, Ryan Huang, Shrey Kumar and others, 1:30–2:30 PM EDT (transcript available).
- Posted in #project-surf-build that QA is ready for product acceptance, tagging Timothy Meyer and Thom Oguntoyinbo with 6 batches / 24 stories (workflow engine 109.x, workflow & review, uploads, design system foundations, operations screens, config & admin screens); batches 3–5 went to Tasmia Shefa / Karan Kapoor.
- Told Thom Oguntoyinbo in a DM that 3.39 is not included and 109.20 is already done.
- Told Shrey Kumar in #project-surf-build that the issue could be fixed during their Onboard Part 2 session, then held "Douglas <> Shrey - Continuing proj walkthrough", 3:00–4:00 PM EDT (transcript available).
- Told Samuel Couture Brochu in a DM about a coming meeting on hard deletes in the database, which agents are doing because of instructions in the PRD; already flagged to Timothy Meyer, and the instructions need to change.
- Told Samuel Couture Brochu that a disputed call was an engineering decision rather than a product one, though Timothy Meyer was not happy about it.
- Asked Samuel Couture Brochu in a DM to move Douglas's day off to the Monday after Thanksgiving.
- Gave Samiha Nusrat initial positive feedback in a DM about a person Douglas evaluated, pending a debrief with Craig Stickel.
- Organized and held "Sync on DevOps Project Surf" with Dipak Parmar, 4:00–4:30 PM EDT (transcript not available).

## Decisions & Rationale

- **Agent hard deletes must be addressed at the source**: Agents use hard deletes because the PRD tells them to, so the PRD instructions need updating; flagged to Timothy Meyer, and a meeting is planned.
- **Engineering owns the disputed call**: Douglas told Samuel Couture Brochu that this was an engineering decision, not a product one, even though Timothy Meyer disagreed.
- **Sprint work handed to product acceptance**: 24 QA'd stories were split into 6 batches so product reviewers can each claim a batch and test it on dev.

## Open Loops

No open loops carried (no prior summary within 10 days; last summary was 2026-04-17).

- **Product acceptance of 24 stories**: Waiting for Timothy Meyer, Thom Oguntoyinbo, Tasmia Shefa and Karan Kapoor to claim batches and move stories to done or send them back.
- **Holiday swap**: Waiting for Samuel Couture Brochu to approve moving the day off to the Monday after Thanksgiving.
- **Debrief with Craig Stickel**: Still pending, before Douglas finalizes feedback for Samiha Nusrat.
- **PRD hard-delete instructions**: Still need updating; the meeting is not yet booked.

## Blockers

No blockers identified.

## Next Steps

- Book the meeting on hard deletes and update the PRD instructions.
- Debrief with Craig Stickel and send final feedback to Samiha Nusrat.
- Follow up on the product acceptance thread in #project-surf-build as reviewers claim batches.
- Continue Project Surf knowledge transfer with Shrey Kumar.
- Follow up on the DevOps Project Surf work with Dipak Parmar.
- Start the next sprint's Surf Build work as planned in today's sprint planning.

## Transcript Source (Cleaned)

My morning started with a one-hour sync Tasmia Shefa set up to get my help with her T3 account; Gemini notes are attached. Around 11 AM I caught up on a #project-surf-build thread and apologized for joining late, because I was in deep work finishing my stories the day before. I told Shrey Kumar we could try to fix the issue in our Onboard Part 2 session. In a DM with Sam Couture Brochu I said I'll book a meeting about hard deletes in the database: agents are using them because of instructions in the PRD, I've already flagged it with Tim, and those instructions need updating. I also told Sam that Tim wasn't happy about a separate call, but it's an engineering decision, not a product one. Separately, I told Samiha Nusrat my first impression was positive, but I still need to debrief with Craig Stickel.

The afternoon was Project Surf end-of-sprint ceremonies: the End of Sprint Demo/Check-in at 12:30 (recording, chat and Gemini notes in Drive), the Surf Stand-up at 1:00, and Surf Build Sprint Planning from 1:30 to 2:30. Around those, I answered Thom Oguntoyinbo on story scope (3.39 no, 109.20 already). Then I posted the QA-ready announcement in #project-surf-build: six batches of stories for product acceptance, covering the workflow engine (routing rules, step authoring, portal form confirmation, recreation mode, form routing), workflow and review, simplified uploads, design system foundations, operations screens, and configuration and admin screens. Batches 3–5 were assigned to Tasmia Shefa and Karan Kapoor.

Later I asked Sam to move my holiday to the Monday after Thanksgiving, since I enjoy working when nobody else is around. From 3:00 to 4:00 I continued the project walkthrough with Shrey Kumar (Gemini notes available) and FYI'd him in #project-surf-how-we-build. I closed the day with a "Sync on DevOps Project Surf" with Dipak Parmar, which I set up that morning; no transcript was linked. Other Slack DMs that day (with Onildo Aguiar, Karan Kapoor, Craig Stickel, Ryan Huang and Dipak Parmar) were short acknowledgements and aren't captured.
