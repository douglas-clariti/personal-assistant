---
date: "2026-11-27"
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
  - temporal
  - postgresql
  - aurora
  - cdi
  - cognito
  - ai-models
---

# Daily Summary — Friday, November 27, 2026

## Summary

Light day — the office was closed for the Q4 Team Appreciation Day. Activity was limited to follow-ups in #project-surf-build and a DM with Dipak Parmar on DEV Temporal access and the PostgreSQL 18.6 upgrade PR.

- Calendar shows "Office Closed: Q4 Team Appreciation Day" (HR, all employees) for today.
- "Project Surf Stand-up" (organizer Timothy Meyer, declined/out of office) was on the calendar at 12:30 PM ET; RSVP was not responded to and attendance is not confirmed (transcript not available).
- Confirmed receipt of Dipak Parmar's Cognito DEV pool invite in #project-surf-build, restoring DEV Temporal UI access needed for the Record claim 503 investigation (PR #5742).
- Replied to Dipak Parmar in #project-surf-build and via DM on PR #5748 (CDI PostgreSQL 18.6 upgrade), acknowledging his note that Temporal compatibility kept Aurora on Postgres 16 and that the upgrade had long been on the plan.
- Reacted to Vitaliy K.'s Gemini 4 Neon announcement in #tech-learn-and-share.

## Decisions & Rationale

- **Continue with the PostgreSQL 18.6 upgrade (PR #5748) jointly with Dipak**: Dipak flagged that Temporal compatibility with newer Postgres versions was never validated, which is why Aurora stayed on 16; Douglas framed it as a shared effort rather than a reversal.

## Open Loops

No open loops carried from a previous summary (most recent daily summary on file is 2026-04-17).

- **PR #5748 review (CDI PostgreSQL → 18.6)**: Awaiting review from Dipak Parmar and Simone Giacomel, including upgrade/rollback steps and Aurora parameter group handling.
- **Temporal CLI read-only access in DEV**: Requested from Dipak Parmar (EKS denies port-forward to `temporal-frontend` and exec into `temporal-admintools` for the `CDIDeveloper` profile); no response yet.

## Blockers

- Temporal compatibility with Postgres 18 is unverified and needs investigation and testing before PR #5748 can safely ship.

## Next Steps

- Accept the Cognito DEV pool invite and pull the claim workflow history in `cell-pooled-dev` around 18:43:22 UTC on Nov 26 for the Record claim 503 investigation (PR #5742).
- Validate Temporal against Postgres 18.6 as part of PR #5748.
- Follow up with Dipak Parmar on an approved path for read-only Temporal CLI access in DEV.

## Transcript Source (Cleaned)

Today was the Q4 Team Appreciation Day, so the office was closed and I kept things light. The Project Surf Stand-up was still on my calendar for 12:30, but Timothy was out and I never RSVP'd.

In #project-surf-build I thanked Dipak for sending the Cognito DEV pool invite. That gets me back into the DEV Temporal UI, which I lost after the move to `cdi-nonprod`, so I can keep digging into the Record claim 503 issue. I had also asked him for read-only Temporal CLI access in DEV, and that one is still open.

On my PostgreSQL 18.6 upgrade PR (#5748), Dipak said he kept Aurora on Postgres 16 because he couldn't confirm Temporal would work on newer versions. I told him in the thread and by DM not to worry: the upgrade had been on my list for a long time and we're doing it together.

In #tech-learn-and-share I reacted to Vitaliy's post about Google's Gemini 4 Neon models.
