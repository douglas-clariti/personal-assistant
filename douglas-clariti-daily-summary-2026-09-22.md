---
date: "2026-09-22"
weekday: "Tuesday"
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
  - dev-environment
  - staging
  - rpass
  - gis
  - super-bmad
  - ci
---

# Daily Summary — Tuesday, September 22, 2026

## Summary

A Project Surf day focused on keeping the environments healthy. I ran the availability cutover on the dev tenant to unblock PM QA, asked the team to check dev issues against fresh data before reporting bugs, and weighed in on staging access for the POC and training groups. I also attended the Surf stand-up, ran my Progress Check-In, and joined a GIS design meeting.

- Attended "Project Surf Stand-up" (organizer Timothy Meyer), 12:30–1:30 PM EDT (transcript available — Notes by Gemini).
- Organized and ran "Progress Check-In" with Samuel Couture, Justin LaBrash and Ankit Mittal, 1:30–1:50 PM EDT (transcript not available).
- Attended "GIS Connections per Tenant" with Amrita Patra (organizer) and Onildo Aguiar, 2:15–3:00 PM EDT (transcript available — Notes by Gemini).
- Asked Ankit Mittal to merge PR #2462 (durable bootstrap + CLI command), then ran the dev tenant availability cutover and confirmed it was done in #project-surf-build, unblocking PM QA for stories 99.10/99.11.
- Posted a heads-up in #project-surf-build to Eric McClelland, Edwin Leong, Timothy Meyer, Justin LaBrash and Thom Oguntoyinbo: dev has no data migrations, so repro bugs with fresh data before reporting them; asked Justin to recreate a Recordtype from scratch.
- Flagged in #project-surf-build that dev needs a data cleanup because old tests and demos left bad data in the database.
- Offered Justin LaBrash to restrict staging RPASS access, and argued in #project-surf-build that a separate POC org alone won't isolate it, because anyone at Clariti can request platform access.
- Coached Ryan Huang via DM to watch CI, make sure it's green before merging, and check develop after the merge.
- Told Ankit Mittal via DM to ask Colin or Dipak for developer access to the develop environment.
- In #pod-superbmad, said I'd test Opus 5.5 on one of my tasks to measure cost after Samuel Couture announced it was enabled for the org.

## Decisions & Rationale

- **Dev bug reports need a fresh-data repro first**: Dev skips data migrations and gets big changes often, so stale data creates false bug reports and wastes debugging time.
- **Ran the dev availability cutover right after PR #2462 merged**: PM QA was blocked by a 503 on manual document generation.

## Open Loops

- Staging isolation for the POC group vs. the training group is still open; Timothy Meyer and Edwin Leong favor a dedicated POC org, and Justin LaBrash is checking how staging is being used.
- PM QA still needs to retest stories 99.10/99.11 after the cutover.
- Opus 5.5 cost check on one of my tasks has not been done yet.

## Blockers

- None reported today.

## Next Steps

- Plan and run a dev database cleanup of old test and demo data.
- Test Opus 5.5 on a task and report the cost to #pod-superbmad.
- Follow up on the staging RPASS access and POC environment decision with Justin LaBrash, Timothy Meyer and Edwin Leong.
- Check that Ryan Huang's merge to develop stayed green.

## Transcript Source (Cleaned)

Today I attended the Project Surf stand-up, ran my Progress Check-In with Samuel, Justin and Ankit, and joined Amrita and Onildo to talk about GIS connections per tenant. Gemini notes exist for the stand-up and the GIS meeting.

In #project-surf-build, Ankit reported that PM QA for stories 99.10 and 99.11 was blocked: the dev tenant hadn't finished the availability cutover, so manual document generation returned a 503. I asked him to merge PR #2462, then I ran the cutover and confirmed it was done. Separately, when a bug came up, I asked Justin to recreate the Recordtype from scratch. I reminded the wider team that dev has no data migrations, so they should retest with fresh data before reporting bugs, and I noted that dev needs a cleanup of old test and demo data.

On staging access, Justin wants to limit RPASS credentials so the POC group has a clean environment. I offered to restrict access if he sends me the list. I also pointed out that a separate org wouldn't fully fix this, because anyone at Clariti can request platform access. Timothy and Edwin prefer to set up a dedicated POC environment.

In DMs, I reminded Ryan Huang to watch CI and check develop after merging, and I pointed Ankit to Colin or Dipak for developer access to the develop environment. In #pod-superbmad, after Samuel said Opus 5.5 was enabled for the org, I said I'd test it on a task to see what it costs.
