---
date: "2026-06-22"
weekday: "Monday"
author: "douglas-clariti"
quality: "complete"
sources_used:
  - google_calendar
  - slack
  - google_drive
sources_empty:
  - gmail
open_loops_carried: 1
tags:
  - project-surf
  - super-bmad
  - sprint-planning
  - onboarding
  - epr-module
  - repo-migration
  - prd-merge
  - token-optimization
---

# Daily Summary — Monday, June 22, 2026

## Summary

Sprint planning week opened with three productive meetings covering onboarding prep, repository governance, EPR architecture, and Super BMAD team structure. In parallel, Douglas completed the migration of the project-surf repositories into `clariti-labs/project-surf`, sent GitHub invitations to four new teammates, and is actively merging PRDs ahead of Wednesday's onboarding session.

- Attended Sprint Planning with Justin LaBrash and Samuel Couture Brochu (Google Meet, 9:30–10:00 AM EDT) — prioritized What Track repo linting/artifact integrity cleanup and confirmed joint Wednesday onboarding session for Craig and Ronaldo (transcript available).
- Organized and ran Progress Check-In (Google Meet, 1:00–1:20 PM EDT) with Samuel, Justin, and Aman Bhalla — decided EPR module stays in Surf repo using feature flags, finalized Wednesday onboarding structure as self-serve sandbox + afternoon Q&A, and confirmed Douglas will merge multiple PRDs into a single master version before Wednesday (transcript available).
- Attended 1:1 with Samuel Couture Brochu (Google Meet, 2:00–2:30 PM EDT) — received positive performance feedback; team structure clarified (Douglas owns Super BMAD technical vision; new pod under Craig); token spend flagged at ~$8,950/month; roadmap prioritized over new feature requests (transcript available).
- Declined recurring Douglas/Justin Daily (9:30 AM) — coverage provided by Sprint Planning.
- Completed `clariti-labs/project-surf` repo migration via Slack Group DM with Timothy Meyer and Justin LaBrash; sent GitHub invitations to Karan Kapoor, Edwin Leong, Craig, and Ronaldo.
- Proposed lint-rule-based `docs/` folder governance to Timothy and Justin in Group DM; asked Justin to document folder structure via `tree` so PMs can confirm before encoding into Super-BMAD.
- Directed Karan Kapoor in #project-surf-what-track on onboarding setup: accept GitHub invitation, install `bun` — other local setup steps optional.
- Created "WIP Docs" folder in Google Drive; "00 Overview" and "RFI Working Documents" folders modified today.

## Decisions & Rationale

- **EPR module built inside Surf repository**: The EPR system will be developed as a module within the existing Surf repo using feature flags so it can be sold with or without permitting functionality — avoids repo fragmentation and maintains architectural consistency.
- **Wednesday onboarding structure confirmed**: Self-serve sandbox session in the morning (clone repo and walk through PRD-to-completion), followed by 30-min Surf/Super-BMAD context and 30-min Q&A in the afternoon — joint session covers Craig and Ronaldo simultaneously to avoid repeated explanations.
- **docs/ folder structure pending lint enforcement**: `docs/` is a Super-BMAD convention, not canonical BMAD; Justin to run `tree` with per-folder annotations, PMs to confirm, then Douglas encodes into Super-BMAD via lint rule.
- **Super BMAD team structure defined**: Douglas owns technical vision and framework; Justin leads product and external-facing aspects; new pod (Craig, Anildo, TBD third developer) reports to Craig; Enterprise Precheck pod to be led by Eric.
- **Token cost optimization strategy**: Developers use professional judgment to stop tasks when output meets quality criteria — reduces unnecessary token consumption; ~$8,950 current monthly spend flagged as above-average but manageable during scale-up.
- **Roadmap prioritized over new tooling**: In-app feedback tool idea (Douglas) deferred — team to stay focused on established roadmap and current bottlenecks.
- **Self-descriptive onboarding strategy adopted**: Developer questions during onboarding will be used to auto-generate FAQ documentation committed to the repo for future contributors.

## Open Loops

- **Expensify access** *(carried from 2026-04-17)* — Requested from accounting@claritisoftware.com for Lévis offsite train ticket expenses; no resolution found in today's data. (stale — consider closing or escalating)
- **Justin LaBrash: `tree` folder annotation** — Douglas asked Justin to run `tree` with one-line per-folder notes; pending confirmation from PMs before lint rule is created and repo is reorganized.
- **GitHub invitation acceptance** — Karan Kapoor, Edwin Leong, Craig, and Ronaldo need to accept invitations to `clariti-labs/project-surf`.
- **Eric / EPR architecture consult** — Eric to contact Justin LaBrash to clarify architecture and repo structure for the EPR module (assigned in Progress Check-In).
- **PRD merge** — Douglas consolidating multiple product requirement documents into a single master PRD aligned with Super BMAD standards; must be complete before Wednesday onboarding session.

## Blockers

No blockers identified today.

## Next Steps

- **Douglas**: Review human orchestration architecture in PRD; draft user stories with Justin (today or tomorrow morning, per Sprint Planning).
- **Douglas**: Finish PRD merge into master version aligned with Super BMAD standards before Wednesday session.
- **Douglas**: Prepare onboarding materials for Anildo and Tim (new team members).
- **Douglas**: Implement testing/CI improvements for skills and workflows to guard against regressions when new models are released.
- **Douglas**: Create lint rule and reorganize repo structure once Justin's `tree` annotations are confirmed by PMs.
- **Justin LaBrash**: Create onboarding guidance documentation for Wednesday implementation call.
- **Justin LaBrash**: Run `tree` command with per-folder annotations for PM sign-off.
- **Samuel Couture Brochu**: Schedule Wednesday onboarding session with Craig, Ronaldo, and Tim; send onboarding questions list to Justin.

## Transcript Source (Cleaned)

Monday opened with Sprint Planning (9:30–10:00 AM EDT, Google Meet) with Justin LaBrash (organizer) and Samuel Couture Brochu. The team identified What Track repository cleanup — specifically linting and artifact integrity — as the top priority for the week. Douglas confirmed the linter is implemented and integrated into the Git hook, blocking problematic artifact commits. The team confirmed a joint Wednesday onboarding session for two new developers (Craig and Ronaldo); Samuel will coordinate scheduling. Douglas was tasked with reviewing the human orchestration architecture in the PRD and drafting user stories with Justin. The team adopted a self-descriptive onboarding philosophy where developer questions auto-generate FAQ documentation.

Douglas then organized and ran the Progress Check-In (1:00–1:20 PM EDT, Google Meet) with Samuel, Justin, and Aman Bhalla. Discussion covered repository document folder structure — Justin proposed isolating human-facing documents (roadmaps, planning artifacts) from agent access using lint configuration, which Douglas confirmed is implementable. Wednesday onboarding structure was finalized: morning self-serve sandbox with Surf/Super-BMAD walkthrough, afternoon Q&A. Douglas reported progress on PRD cleanup (consulted with Ching on what to merge or remove) and committed to finishing the reorganization and master PRD merge today. The EPR module — a second Super-BMAD pod to be led by Eric — was confirmed to be built inside the existing Surf repo as a feature-flagged module; Eric will consult Justin on architecture.

In the afternoon 1:1 with Samuel Couture Brochu (2:00–2:30 PM EDT, Google Meet), Samuel delivered positive performance feedback on Douglas's Super BMAD work. Team structure was clarified: Douglas and Justin remain dedicated to the Super BMAD framework; a new "What Track" pod of Craig, Anildo, and a third future developer will report to Craig; an Enterprise Precheck pod will be managed by Eric. Token spend was flagged at approximately $8,950 for the current month — above other teams but within acceptable range during scale-up; future developers will be observed to identify inefficiencies. Douglas raised a desire to integrate an in-app user feedback tool that auto-creates GitHub stories for agents; Samuel advised staying on roadmap. Douglas also raised concerns about regression testing when new AI models are released; the team discussed CI improvements. Samuel set an expectation for Douglas to act as the primary technical reference for Super BMAD — the "velocity engine" of Clariti — and advised Douglas to develop judgment on when to stop late-night AI sessions and let agents run independently.

Concurrently, on Slack, Douglas completed the migration of the project-surf repositories into `clariti-labs/project-surf`, confirmed in a Group DM with Timothy Meyer and Justin LaBrash. Douglas sent GitHub invitations to Karan Kapoor, Edwin Leong, Craig, and Ronaldo. Timothy raised a post-merge concern about the divergent use of the `docs/` folder (his team used it for cross-session reference material; merged content also includes research and sprint artifacts). Justin proposed a three-folder structure: `docs/` (always-on agent context), `research/` (agent-consumed), `workspace/` (human scratchpad). Douglas clarified `docs/` is a Super-BMAD convention, not canonical BMAD, and offered to encode the final agreed structure via a lint rule after Justin documents each folder's purpose via `tree` and PMs confirm. In #project-surf-what-track, Douglas directed Karan Kapoor to accept his GitHub invitation and confirmed only `bun` is required to get started — other local setup steps optional. Douglas warmly welcomed the new teammates in the channel.
