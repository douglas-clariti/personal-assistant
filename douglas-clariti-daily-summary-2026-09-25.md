---
date: "2026-09-25"
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
  - surf-build
  - ci
  - sprint-planning
  - super-bmad
  - ai-tooling
  - aws
  - onboarding
---

# Daily Summary — Friday, September 25, 2026

## Summary

A heads-down Friday focused on unblocking the Surf Build team. Douglas took ownership of a failed CI seeding deploy, supported Craig Stickel on a PR and a dev backoffice issue, and declined or rescheduled several meetings so he could move stories to QA. He also set a guideline for which AI model to use for which kind of work, and argued that the team's bottleneck is story throughput, not headcount.

- Invited to "Project Surf - End of Sprint Demo/Check-in", organized by Timothy Meyer, 12:30–1:00 PM EDT; RSVP left unanswered (transcript available — recording, chat, and Gemini notes).
- Invited to "Project Surf Stand-up", organized by Timothy Meyer, 1:00–1:30 PM EDT; RSVP left unanswered (transcript available — Gemini notes).
- Accepted "Surf Build - Sprint Planning", organized by Timothy Meyer, 1:30–2:30 PM EDT; "POC Happy Path" doc attached (transcript available — Gemini notes).
- Flagged in #project-surf-build that Amrita P.'s seeding on task 72-1 failed to deploy and took ownership of the fix, cc Onildo Aguiar and Craig Stickel; later asked the team to announce who is touching CI so people don't overlap.
- Supported Craig Stickel via DM on his PR: asked whether 99.5 was tested locally, suggested testing on dev, and asked him to post the bug in the super-bmad pod channel.
- Troubleshot a template display issue on the dev backoffice (`backoffice.dev.clariti-surf.com/config/templates`) with Craig Stickel; it showed after an update, and Douglas suggested a cache issue on Craig's side.
- Walked Dheekshita Kumar via DM through local Surf setup (`bun run dev:local` auto-configures once AWS access exists) and pointed her to Colin or Dipak for read-only AWS access through Rippling.
- Told Dheekshita Kumar that work on more granular Surf access has started with Dipak's help, and that `_bmad-output` is mostly project-related but needs cleanup.
- Moved meetings with Dheekshita Kumar to Monday, dropped a meeting with Karan, and told Samuel Couture Brochu he would skip today's EM meeting to focus on workflow tasks and stories for QA.
- Told Justin LaBrash via DM that he prefers only full-time contributors on Surf, since the bottleneck is completing and validating stories rather than architecture, and new people need about 3 weeks to become productive.
- Told Timothy Meyer via DM he is "all in" on a proposal Timothy raised, noting he gave Justin the same idea last week.
- Told Craig Stickel via DM that the team should share more about in-flight work after the first delivery, and that his point in yesterday's meeting was about leadership adding scope, not about the team.
- Agreed with Onildo Aguiar via DM on model usage: Samuel approved Douglas using Opus for his stories, but CI, tests, and acceptance-criteria (AC) work should go to Luna for cost reasons.
- Helped Onildo Aguiar debug an issue on a machine (suspected license copy-paste error) and shared a new AI orchestration tool that wraps Claude Code and Codex and supports remote machines, with a plan to present it to the team Monday.

## Decisions & Rationale

- **Took ownership of the task 72-1 seeding deploy fix**: Announced it publicly in #project-surf-build so only one person works on it; also asked the team to announce CI changes to avoid collisions.
- **Model usage guideline — Opus for development, Luna for CI/tests/ACs**: Lower-effort tasks don't need a top-tier model, and using Opus to fix CI would burn too many tokens.
- **Cleared the calendar to focus on delivery**: Skipped the EM meeting, moved Dheekshita Kumar's meetings to Monday, and dropped a meeting with Karan to unblock the team and move stories to QA.
- **Prefer full-time contributors on Surf**: More part-time people add communication overhead, and ramp-up takes about 3 weeks; the real bottleneck is completing and validating stories.

## Open Loops

No previous summary within the lookback window (the most recent is from 2026-04-17), so nothing was carried forward.

- **Task 72-1 seeding deploy fix**: Douglas took ownership; completion not confirmed in today's data.
- **Craig Stickel's PR and the dev backoffice template issue**: Douglas committed to making the PR work; the template now shows, possibly a cache issue on Craig's side.
- **Dheekshita Kumar's AWS read-only access**: Waiting on Colin or Dipak to grant it through Rippling.
- **Granular Surf access model**: In progress with Dipak.
- **Rescheduled meetings with Dheekshita Kumar**: Moved to Monday.

## Blockers

- Team blocked on problems Douglas is working through today; he cited these as the reason for skipping meetings (details not captured in the data).

## Next Steps

- Monday: present the new AI orchestration tool (wraps Claude Code and Codex) to Onildo Aguiar and the team.
- Monday: hold the rescheduled meetings with Dheekshita Kumar.
- Finish the workflow tasks and move assigned stories to QA.
- Confirm the task 72-1 seeding deploy is fixed and Craig Stickel's PR is merged.
- Clean up `_bmad-output` in the Surf project.

## Transcript Source (Cleaned)

Friday's calendar was three back-to-back Project Surf sessions organized by Timothy Meyer: the End of Sprint Demo/Check-in (12:30–1:00 PM EDT), the Project Surf Stand-up (1:00–1:30 PM EDT), and Surf Build - Sprint Planning (1:30–2:30 PM EDT). Douglas accepted only the Sprint Planning invite. All three have Gemini notes attached, and the demo also has a recording and chat log.

Early in the day Douglas posted in #project-surf-build that Amrita P.'s seeding on task 72-1 had failed to deploy and that he was fixing it, cc'ing Onildo Aguiar and Craig Stickel so nobody else duplicated the work. When the topic came up again, he asked the team to announce who is touching CI.

Throughout the day Douglas supported Craig Stickel over DM on a PR, asking for the link, whether 99.5 had been tested locally, and suggesting testing on dev. He asked Craig to post the bug in the super-bmad pod channel. He also looked into a template on the dev backoffice that wasn't displaying for Craig; it showed after an update, and Douglas suggested a cache issue. In a separate exchange, Douglas said the team should share more about in-flight work after the first delivery. He clarified that his comment in yesterday's meeting was about leadership adding scope, not about the team.

With Dheekshita Kumar, Douglas explained that he set up the Surf environment himself. Local setup runs with `bun run dev:local` and auto-configures once AWS access exists, which she should request from Colin or Dipak through Rippling. He also mentioned that work on more granular Surf access has started with Dipak. Because he needed to unblock the team, he moved their meetings to Monday and dropped a meeting with Karan. He told Samuel Couture Brochu he would skip the EM meeting to focus on workflow tasks and stories to move to QA.

With Justin LaBrash, Douglas said he'd rather have only full-time contributors on Surf. More people means more communication and more opinions, the bottleneck is completing and validating stories rather than architecture, and new people need about 3 weeks to become productive. With Timothy Meyer, he said he is "all in" on a proposal Timothy raised and noted he had given Justin the same idea the week before.

In a long DM with Onildo Aguiar, Douglas said Samuel had approved him using Opus for his stories. He argued that Opus should be kept for development work, with CI, tests, and acceptance-criteria tasks going to Luna, because a top-tier model is overkill and costly for those. He helped Onildo debug an issue on a machine (suspected license copy-paste error). In the afternoon he shared a new AI orchestration tool he is testing: it runs Claude Code and Codex underneath, supports remote machines, and makes switching providers easy. He plans to present it to the team on Monday.

Gmail was unavailable this run because the connector needs to be re-authenticated. Google Drive has no local sync path configured.
