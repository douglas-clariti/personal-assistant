---
date: "2026-11-25"
weekday: "Wednesday"
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
  - incident-response
  - aws-cloudwatch
  - eks
  - pulumi
  - bmad
  - sentry
  - cdi
---

# Daily Summary — Wednesday, 2026-11-25

## Summary
- Attended CDI "Session 1: Product Vision & All-in-one Ecosystem" (Four Weeks of CDI series) via Google Meet (transcript available).
- Was invited to the Project Surf Stand-up with Timothy Meyer and the Surf team (marked tentative) (transcript available).
- Hosted the Progress Check-In with Samuel Couture, Justin Labrash and Ankit Mittal (transcript not available).
- Posted the pooled DEV API incident analysis in #cdi-alerts-sentry-backoffice: losing the only API pod caused 801 HTTP 503s and 367 Sentry events in seven minutes, and proposed three remediation options with the write-up in PR #5613.
- Proposed to Dipak Parmar and Simone Giacomel in #team-devops enabling AWS CloudWatch Container Insights on the DEV EKS cluster (Ohio) through the Pulumi data-plane-platform stack, with a new runbook.
- Asked Dipak Parmar in #cdi-alerts-sentry-backoffice to split Sentry alerts into more channels and asked the team to watch the channel during deploys.
- Recommended in #project-surf-build that the story-number collision follow the Epic 78 precedent (keep 1.25 active, move the profiler story to 1.41 via /sbmad-change), and said a CI check is possible but a local warning is overkill.
- Asked Onildo Aguiar to approve project-surf PR #5613 and shared the app-deploy workflow and sgiacomel's GitHub profile.
- Asked Ankit Mittal to triage bugs filed by devs/product for priority, after finishing the "capture finding" change.
- Agreed with Samiha Nusrat and Marnix Faes to pick 2 of 3 options given the time available.
- Shared QA values (25.21, 14.3) with Timothy Meyer and confirmed a plan with Dipak Parmar in #project-surf-build, offering a PR review.
- Said in #project-surf-how-we-build that the architecture review for the task would likely finish today.
- Told #project-surf-build about an appointment from 2–6 PM (calendar "Appointment (OO)") and declined the Project Surf End of Sprint Demo.
- Offered to pause in-flight work for Dipak Parmar ("I can hold it until you finish"), with work to resume tomorrow.

## Decisions & Rationale
- **Recommended Story 0.58 first for DEV API resilience**: splitting liveness from DB readiness and bounding graceful shutdown removes Temporal from both health checks; a second DEV replica stays an open option pending scope change to Story 0.56.
- **Story renumbering follows the Epic 78 precedent**: collisions come from a story number claimed on a branch other branches can't see; BMad v7 only mitigates it, so renumbering is the practical fix.
- **No local warning for story-number collisions**: judged overkill; a CI job is the possible guard.
- **Pick 2 of 3 options (with Samiha Nusrat and Marnix Faes)**: limited time available.
- **Hold own in-flight work for Dipak Parmar**: let Dipak finish first, resume tomorrow.

## Open Loops
- Waiting on the team to choose between landing Story 0.58 alone or adding a second DEV API replica in parallel (needs Story 0.56 scope extension).
- Waiting on Dipak Parmar and Simone Giacomel to approve CloudWatch Container Insights on DEV EKS and pick a rollout window.
- Waiting on Onildo Aguiar to approve project-surf PR #5613 (incident write-up).
- Waiting on Ankit Mittal's priority triage of the bugs filed by devs/product.
- Waiting on Dipak Parmar's request about splitting Sentry alerts into more channels.
- Waiting on Dipak Parmar's "go" before resuming paused work.
- Root cause of the pooled DEV API slowdown before the health-check timeouts is still unknown, as is whether the later five-event burst was rollout-related.

## Blockers
- Own in-flight work paused until Dipak Parmar finishes.
- Historical memory/CPU-throttling metrics for the failed API pod were unavailable, which limited the incident investigation.

## Next Steps
- Resume paused work once Dipak Parmar gives the go (likely tomorrow).
- Finish the architecture review for the #project-surf-how-we-build task.
- Implement CloudWatch Container Insights (Pulumi index.ts, stack-settings.ts, DEV stack YAML, runbook) once approved.
- Move the completed profiler story to 1.41 via /sbmad-change after confirming the number is free.
- Plan a "Super BMad" demo with Ankit Mittal when the sprint allows.
- Review the Gemini notes and recording for CDI Session 1 and the Project Surf Stand-up.

## Transcript Source (Cleaned)
I started the day by telling #project-surf-build that I'd be at an appointment from 2 to 6 PM. Mid-morning I said in #project-surf-how-we-build that I was reviewing the architecture for a task and expected to finish today. Later I shared QA values with Timothy Meyer and confirmed a plan with Dipak Parmar, offering a PR review.

At noon I attended the first "Four Weeks of CDI" session on product vision and the all-in-one ecosystem; a recording and Gemini notes are attached. The Project Surf Stand-up followed (Gemini notes attached), and then I ran our Progress Check-In with Samuel, Justin and Ankit.

Most of my afternoon went to the pooled DEV API incident. In #cdi-alerts-sentry-backoffice I explained that AWS confirmed the biggest burst came from losing the only API pod: 801 HTTP 503s and 367 Sentry events in seven minutes. I proposed three paths and recommended starting with Story 0.58. In #team-devops I asked Dipak and Simone whether we could turn on CloudWatch Container Insights for DEV EKS through Pulumi, since we couldn't see historical memory or CPU throttling for the old pod. I also asked to split the Sentry alerts into more channels, and I asked Onildo to approve PR #5613.

In #project-surf-build I recommended renumbering stories following the Epic 78 precedent and said a CI job could guard against collisions. I asked Ankit to triage the bugs filed by devs and product now that my "capture finding" change is done. With Samiha and Marnix I agreed to pick two of three options given our time. At the end of the day I offered to hold my in-flight work until Dipak finishes and resume tomorrow.
