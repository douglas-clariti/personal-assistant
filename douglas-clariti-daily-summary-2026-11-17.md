---
date: "2026-11-17"
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
  - workflow-engine
  - architecture
  - cdi-steerco
  - townhall
  - qa
  - slack
---

# Daily Summary — Tuesday, 2026-11-17

## Summary
- Douglas sent build 25.21 to QA in #project-surf-build, tagging Timothy M. and Thom Oguntoyinbo.
- Douglas advised Tasmia Shefa (Slack DM) to test file uploads and email communications by running a real workflow end to end, not mocks, so she and Karan can see their components working on the platform.
- Douglas pushed back on Samuel Couture Brochu's architecture claim (Slack DM), explaining from the code that the workflow engine already compiles Phases, Activity Groups and Steps into a node graph (workflowStates and workflowTransitions).
- Douglas proposed a uniform per-Step contract to Samuel covering inputs, result, who decides (person, rule or AI), what it changes, safe rerun and audit log, so new AI Steps can plug in without engine changes.
- Douglas told William Veldhuis (Slack DM) to put all current work on Surf now and work together on Q1 items later.
- Douglas asked Ankit M in #pod-superbmad to hold the pod daily today.
- Douglas attended the Clariti Townhall | Quarterly, hosted by HR (transcript available).
- Douglas ran the Progress Check-In with Samuel Couture, Justin Labrash and Ankit Mittal (transcript available).
- Douglas attended the CDI Build Priority Squad Steerco, organized by Aman Bhalla, covering priorities, key results, blockers and risks (transcript available).
- Douglas had a #clariti-intros Donut chat with Amandeep Kaur (transcript not available).
- Douglas was invited to the Project Surf Stand-up (Timothy Meyer), which overlapped with the Townhall, and had not responded to the invite (transcript not available).

## Decisions & Rationale
- **Extend the existing engine, don't build a new node model**: the engine already runs a state-machine and node graph with conditional transitions. The real gap is the missing standard contract for what happens inside each Step.
- **QA uses real workflows, not mocks**: running the real scenario shows how the platform behaves today and checks the new file-upload and communication components from end to end.
- **William's focus is Surf now**: all current work goes to Project Surf, and joint work with Douglas moves to Q1.

## Open Loops
- Samuel Couture Brochu has not yet answered the per-Step contract proposal or the corrections to the architecture write-up.
- Douglas still needs to check the model benchmarks Samuel raised (whether Opus is still best overall).
- Build 25.21 is waiting for QA from Timothy M. / Thom Oguntoyinbo (Thom is out of office).
- Tasmia Shefa and Karan still need to test file upload and email triggers through a real workflow.

## Blockers
- None recorded today.

## Next Steps
- Write up the per-Step contract (inputs, result, decider, side effects, idempotency, audit) as a proposal for the workflow engine.
- Follow up with Samuel on the architecture document and finish the code review behind the "inaccurate statements" concern.
- Track QA results for build 25.21.
- Review the Gemini notes from the Progress Check-In and the CDI Steerco for action items.

## Transcript Source (Cleaned)
I started the morning helping Tasmia on Slack. I told her the flow had no sub-flow, and that to test file uploads and communications she and Karan should start a new application and run the real scenario rather than rely on mocks, so they can see their components working on the platform. I then posted build 25.21 for QA in #project-surf-build for Timothy or Thom.

Around midday I had a Donut intro with Amandeep Kaur, then joined the quarterly Clariti Townhall. The Project Surf stand-up overlapped with it. I asked Ankit to run the superbmad pod daily, and told William to put everything on Surf for now and that we'd work together in Q1.

In the afternoon I ran our Progress Check-In with Samuel, Justin and Ankit, then attended the CDI Build Priority Squad Steerco. In between, I spent time with Samuel on the workflow engine architecture. I read the code and explained that the engine is already a node graph: the journey compiler turns Phases, Activity Groups and Steps into a state machine with parallel tracks, conditional transitions and a worker that runs it. What's missing is a uniform contract for what happens inside a node. I described that contract as six parts (inputs, output, who decides, what it changes, safe to rerun, what it records), so new AI Steps can plug in without engine changes. Samuel also asked about new model benchmarks, and I still need to look at them.
