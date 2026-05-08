---
date: "2026-05-08"
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
  - compliance
  - bmad
  - eval-tests
  - how-track
  - sprint-planning
  - ai-native
  - clariti
---

# Daily Summary — 2026-05-08 (Friday)

## Summary

- Attended **Douglas / Justin Compliance** 1:1 (11:00–11:30 AM ET) with Justin LaBrash to present the compliance automation system built in super-bmad, covering rule catalog, smart tagging, evidence bundler, scorecard, and workflow integration (transcript not available).
- Before the meeting, flagged hardcoded Temporal tech-stack references in the Project Surf Product Brief and PRD via Slack DM with Justin, identified two specific file locations, and requested he scrub them — Justin confirmed the cleanup was completed.
- Requested Justin clean up the references so architecture research (`/bmad-technical-research`) can be run on clean artifacts.
- Attended **How Track – Weekly Review** (12:00–12:30 PM ET) with Aman Bhalla, Timothy Meyer, Samuel Couture, Justin LaBrash, and Herman Chan (transcript not available).
- Shared Project Surf Product Brief and PRD links with Herman Chan via DM as context for v0 goals and ongoing work.
- Identified that custom skills were altering BMAD's built-in skill behavior, causing broken workflows, and committed to building automated eval tests this weekend to prevent future regressions.
- Shared positive feedback on a prompt tested throughout the day in #clariti-eng-ai-native-development-learning; Herman Chan reacted positively.
- Attended **Sprint Planning** (3:00–3:30 PM ET) with Justin LaBrash and Samuel Couture (transcript not available).

## Decisions & Rationale

- **Remove hardcoded tech decisions (Temporal) from Product Brief and PRD**: Keeping implementation-specific references in planning artifacts causes them to leak into architecture research and design artifacts; artifacts should remain tech-agnostic to allow proper `/bmad-technical-research` to drive decisions.
- **Build BMAD skill eval tests this weekend**: Custom skills have been silently overriding BMAD's built-in skill behavior, resulting in broken workflows; automated eval tests are needed to catch regressions before they compound.
- **Frame compliance system for non-technical audience**: The compliance documentation shared with Justin was framed in plain language (rule catalog, scorecard, evidence bundler) to ensure accessibility beyond the engineering team.

## Open Loops

- **Architecture research on Project Surf** — waiting to run `/bmad-technical-research` now that Justin has confirmed Temporal references are scrubbed from Product Brief and PRD; can proceed.
- **BMAD eval test build** — committed to completing over the weekend; no external dependency.

## Blockers

- No active blockers at end of day. The BMAD skill conflict issue is acknowledged and queued for resolution via eval tests this weekend.

## Next Steps

- Build automated eval tests for BMAD skills this weekend (Microsoft Waza / Tea module flagged as a reference to investigate).
- Run `/bmad-technical-research` on Project Surf artifacts now that references are clean.
- Follow up post-sprint planning on any work items assigned.

## Transcript Source (Cleaned)

Today I had three back-to-back meetings: a compliance 1:1 with Justin at 11 AM, the How Track Weekly Review with the full team at noon, and sprint planning with Justin and Samuel at 3 PM. Before the compliance meeting I was active in Slack with Justin, flagging two files in the project-surf repo where Temporal was hardcoded into the Product Brief and PRD — I argued that those docs get loaded into BMAD's artifact planning, so even brainstorming references can pollute downstream architecture decisions. Justin scrubbed them and opened a PR. I then presented Justin with the compliance automation system via DM, walking through five components: a rule catalog covering SOC 2 and ISO 27001, smart tagging that auto-suggests rules on new work items, an evidence bundler that produces auditor-ready reports automatically, a compliance scorecard with pass/concerns/fail verdicts, and native integration into code reviews and design reviews. I framed it specifically for a non-technical reader. Separately I synced with Herman Chan on Project Surf v0 context and we got into a discussion about BMAD skill testing — I realized my custom skills had been silently changing BMAD's built-in behavior, which broke workflows. I committed to spending the weekend building eval tests. Herman mentioned Microsoft Waza has a module called Tea for tests, though I wasn't sure of the details. I also noted in the AI native learning channel that I'd been testing a prompt all day and was impressed with how it pushed back.
