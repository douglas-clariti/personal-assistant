---
date: "2026-07-17"
weekday: "Friday"
author: "douglas-clariti"
quality: "complete"
sources_used:
  - google_calendar
  - slack
sources_empty:
  - gmail
  - google_drive
open_loops_carried: 0
tags:
  - project-surf
  - typescript
  - sprint-planning
  - super-bmad
  - ci
  - build
  - end-of-sprint
  - epics
---

# Daily Summary — Friday, July 17, 2026

## Summary

A sprint-planning-heavy Friday with six meetings and significant infrastructure work. Douglas announced the team's migration from the TypeScript native-preview package to stable TypeScript 7 in #project-surf-build, with PR #715 fully merged and CI green. The afternoon featured the Project Surf End of Sprint Demo, Stand-up, SBMAD Sprint planning, an Epics: Open Decisions meeting Douglas organized himself, and the Project Surf Build Sprint Planning — five back-to-back sessions. CI budget was topped up by $100. A detailed naming analysis for a new blob-copy worker component was shared with Onildo Aguiar.

- Attended "Douglas / Justin Daily" with Justin LaBrash (organizer) via Google Meet, 9:30–9:45 AM EDT (transcript available).
- Announced migration to stable TypeScript 7 (`typescript@7`) in #project-surf-build: native tsc@7 is now the sole type-checker across all 13 workspaces; `@typescript/native-preview` and the pinned dev-channel removed; PR #715 merged with CI fully green.
- Attended "Project Surf - End of Sprint Demo/Check-in" organized by Timothy Meyer, 12:30–1:00 PM EDT, optional attendee (transcript available).
- Attended "Project Surf Stand-up" organized by Timothy Meyer, 1:00–1:30 PM EDT, optional attendee (transcript available).
- Joined stand-up late and followed up with Eric McClelland via DM to share context on current architecture and infra (Douglas is the original author).
- Attended "SBMAD Sprint planning" organized by Justin LaBrash with Samuel Couture, 2:00–2:30 PM EDT (transcript available).
- Organized and hosted "Epics: Open Decisions" with Onildo Aguiar and Amrita Patra, 2:30–3:00 PM EDT (transcript available).
- Attended "Project Surf - Build - Sprint Planning" organized by Timothy Meyer, 3:00–4:00 PM EDT, with Onildo Aguiar, Amrita Patra, Justin LaBrash, Karan Kapoor (transcript available).
- Added $100 to CI budget and notified Samuel Couture and Onildo Aguiar via #project-surf-build and a group DM with Colin John.
- In #project-superbmad, directed Justin LaBrash to open a PR for an interaction type fix; noted losing 2 events is non-critical.
- Shared a detailed naming-options analysis with Onildo Aguiar for the new blob-copy worker component (options: materializer, content-worker, clone-blob-worker, copy-worker, object-worker, and others).

## Decisions & Rationale

- **Migrate to stable TypeScript 7**: Adopted `typescript@7` as a direct dependency across all 13 Project Surf workspaces, replacing `@typescript/native-preview` — stable release provides the same Go-native speed without pinning to a pre-release channel.
- **apps/api retains scoped TS5 devDep**: `apps/api` keeps a scoped classic `typescript@5` only as a library for `openapi-typescript` codegen (incompatible with TS7); its typecheck still explicitly invokes native tsc@7, no regression.
- **Interaction type fix via async PR**: Directed Justin to open a PR for the interaction type issue in project-superbmad rather than blocking; losing 2 events in the interim is acceptable.
- **CI budget top-up of $100**: Added more CI minutes proactively after running low; communicated to Samuel Couture, Onildo Aguiar, and Colin John.

## Open Loops

No open loops carried from previous summary (last summary was 2026-04-17 — 91-day gap; prior loops considered stale and not carried forward).

- **Worker naming decision**: Shared a detailed analysis of naming options for the blob-copy worker with Onildo Aguiar — awaiting alignment/decision.
- **Interaction type PR in project-superbmad**: Justin LaBrash asked to open a PR; not yet confirmed as opened.

## Blockers

No blockers identified.

## Next Steps

- Team to run `bun install` after pulling TypeScript 7 changes from PR #715.
- Justin to open PR for the interaction type fix in project-superbmad.
- Monitor CI pipeline after TypeScript 7 migration — watch for any codegen issues with `openapi-typescript`.
- Finalize worker naming decision with Onildo Aguiar (clone-blob-worker, materializer, or content-worker).
- Follow up on sprint commitments from today's SBMAD Sprint planning and Project Surf Build Sprint Planning.

## Transcript Source (Cleaned)

Today was a sprint-planning-heavy Friday with six meetings and significant infrastructure work. The day started with the regular 15-minute 1:1 with Justin LaBrash (9:30–9:45 AM EDT); Douglas messaged ahead that he'd be 5 minutes late. Immediately after, at 10:01 AM, he posted an announcement to #project-surf-build describing the team's move to stable TypeScript 7 — replacing `@typescript/native-preview` with the official `typescript@7` — explained the one exception for `apps/api`, linked PR #715 (CI fully green ✅), and instructed the team to run `bun install` after pulling.

The afternoon was back-to-back meetings: Project Surf End of Sprint Demo (12:30–1:00 PM EDT, organized by Timothy Meyer, optional attendee; recording and Gemini notes available), immediately followed by Project Surf Stand-up (1:00–1:30 PM EDT). Douglas joined the stand-up a bit late and followed up over DM with Eric McClelland to share context on architecture decisions, noting he was the original author of the current architecture and infra.

SBMAD Sprint planning ran from 2:00–2:30 PM EDT with Justin LaBrash and Samuel Couture. Douglas then organized and ran "Epics: Open Decisions" (2:30–3:00 PM EDT) with Onildo Aguiar and Amrita Patra (Craig Stickel was OOO/declined). The day closed with the Project Surf Build Sprint Planning (3:00–4:00 PM EDT, Timothy Meyer organizing, with Onildo, Amrita, Justin, and Karan).

Between meetings, Douglas added $100 to CI and notified Samuel and Onildo via #project-surf-build and a group DM with Colin John and Onildo. He also shared a thorough naming analysis with Onildo for a new blob-copy worker component, covering content-worker, materializer, clone-blob-worker, copy-worker, object-worker, and others — no decision confirmed yet. In #project-superbmad, he directed Justin to open a PR for an interaction type fix and noted that losing 2 events is not critical.

No emails were sent today. Google Drive is not configured (local_path is empty in config.yaml).
