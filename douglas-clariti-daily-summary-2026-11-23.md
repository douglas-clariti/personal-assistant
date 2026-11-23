---
date: "2026-11-23"
weekday: "Monday"
author: "douglas-clariti"
quality: "partial"
sources_used:
  - google_calendar
  - slack
sources_empty:
  - gmail (connector needs re-authentication)
  - google_drive (local path not configured)
open_loops_carried: 0
tags:
  - project-surf
  - super-bmad
  - devops
  - ci
  - templates
  - qa
  - gis
---

# Daily Summary — Monday, 2026-11-23

## Summary
- Douglas was invited to the **Project Surf Stand-up** (12:30–13:30, organized by Timothy Meyer, ~20 attendees) on Google Meet (transcript available).
- Douglas ran his recurring **Progress Check-In** (13:30–13:50) with Samuel Couture, Justin Labrash and Ankit Mittal on Google Meet (transcript available).
- Douglas met Marnix Faes 1:1 about the **workflow engine** (14:00–15:00) on Google Meet (transcript available).
- Douglas unstuck Samuel Couture's stuck CI run in a Slack DM ("on it" → "done"), with Samuel noting the team needs more GitHub Actions capacity.
- Douglas found a real bug behind Tasmia Shefa's missing "User" tab under PLATFORM in the side nav (it was blocking her ticket QA) and started fixing it.
- Douglas told Aseem Gupta in a Slack DM to go ahead and merge his PR without waiting for Douglas's ignore-file changes.
- Douglas took on Aseem Gupta's #project-surf-build report of a 503 in the dev template picker (`/generation/records/{id}/templates?source=modern`; 5 of 40 Records fail every time, which breaks Story 99.10 AC2).
- Douglas told Ankit Mittal in #pod-superbmad that super-bmad PR #1236 (bmad-ux skill) isn't released because it fixes the wrong place, and he moved the discussion to their daily.
- Douglas tested the Project Surf application flow in a DM with Timothy Meyer: the UI is "way better," but GIS isn't working (likely an account issue), his address can't be found, and the map is out.
- Douglas added Timothy Meyer's request for guidance on PR #4772 (the `roadmap/` planning PR failing the `work-item` check) to his todos.
- Douglas told Ankit Mittal that Aseem Gupta needs to start using `/bmad-testarch-test-design`.
- Douglas helped Onildo Aguiar get set up on the project-surf access in a Slack DM.

## Decisions & Rationale
- **Aseem can merge his PR without waiting for the ignore-file additions**: Douglas didn't want his pending ignore-list change to hold up Aseem's work.
- **super-bmad PR #1236 is not released**: it appears to fix the wrong place, so it was moved to the daily for discussion.
- **Aseem Gupta should adopt `/bmad-testarch-test-design`**: Douglas wants test design to go through the BMAD test-architecture workflow.
- **Address-not-found UX**: Douglas suggested the app tell users an address is "not supported" or "out of range" instead of failing silently, and left the exact wording to Timothy's team.

## Open Loops
- Give guidance on project-surf PR #4772: how planning-only PRs should pass `work-item`, whether `roadmap/**` belongs on the planning-only list, and whether `package.json`/`.oxfmtrc.json` changes need a work item. Timothy Meyer is waiting on this.
- Investigate the template-picker 503 on dev (example REC-2026-0088, request id `ad2b5e73-c756-4e16-842d-88d8208c0404`) by checking the server log. Aseem Gupta is waiting on this.
- Finish the fix for the missing "User" tab under PLATFORM, which is blocking Tasmia Shefa's QA.
- Settle the status and fix location of super-bmad PR #1236 with Ankit Mittal.
- Douglas still has to add files to the ignore list (mentioned to Aseem Gupta).
- Aseem shared project-surf PR #5432 "for your reference" at 14:02. It's unclear whether a review is expected.

## Blockers
- Tasmia Shefa's ticket QA is blocked by the missing "User" tab bug.
- The template-picker 503 is failing Story 99.10 AC2 in the Templates E2E.
- GIS/address lookup in the Project Surf application flow isn't working (possibly an account problem).
- CI capacity: runs are getting stuck, and Samuel noted the team needs more GitHub Actions runners.

## Next Steps
- Reply to Timothy Meyer on PR #4772 with a recommendation for the `work-item` check and planning-only paths.
- Pull the server logs for the 503 request id and find the trigger behind the 5 failing Records.
- Ship the fix for the PLATFORM "User" tab and let Tasmia know.
- Raise super-bmad PR #1236 at the next daily with Ankit Mittal.
- Follow up on GIS/address search and the error messaging for unsupported addresses.

## Transcript Source (Cleaned)
I joined the Project Surf stand-up this afternoon, then ran my Progress Check-In with Samuel, Justin and Ankit, and spent an hour with Marnix on the workflow engine. Gemini notes are attached to all three meetings.

On Slack, the morning started with Samuel's CI being stuck, which I unblocked right away. Mia (Tasmia) was blocked on QA because the "User" tab wasn't showing under PLATFORM. I checked it, confirmed it's a genuine bug, and started fixing it. Aseem reported a 503 in the template picker on dev that's failing Story 99.10 AC2, and I said I'd look at it. I also told him he could merge his PR without waiting on my ignore-file changes.

In #pod-superbmad I told Ankit that the bmad-ux PR #1236 isn't released because it looks like it fixes the wrong place, and we'll discuss it on our daily. I also told him Aseem should start using `/bmad-testarch-test-design`.

With Timothy, I went through the Project Surf application process. The UI is way better now, with a few points to fix: GIS isn't working (probably an account issue), I couldn't find my address, and the map seems to be out. I suggested we tell users the address isn't supported or is out of range. Timothy also pinged me about his roadmap planning PR #4772 and the DevOps `work-item` check. I'd missed it, so it's now on my todos.

I also helped Onildo get set up on the project-surf access.
