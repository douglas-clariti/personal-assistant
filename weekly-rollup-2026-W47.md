---
week: "2026-W47"
date_range: "2026-11-16 to 2026-11-22"
author: "douglas-clariti"
days_covered: 5
days_expected: 5
days_missing: []
tags:
  - project-surf
  - workos
  - local-dev
  - architecture-docs
  - test-data-seeding
  - design-system
  - conditions-of-approval
  - telemetry
  - workflow-engine
  - architecture
  - cdi-steerco
  - townhall
  - qa
  - slack
  - hiring
  - interviews
  - surf-discovery
  - model-evaluation
  - orchestrator
  - bmad
  - qa-testing
  - ai-gateway
  - cdi
  - audit-history
  - citizen-portal
  - backoffice-roles
  - wiz
  - sprint-planning
---

# Weekly Rollup — 2026-W47

**2026-11-16 to 2026-11-22** | **5/5 days covered**

## Themes & Focus Areas
- **Workflow engine architecture**: Douglas showed Samuel Couture Brochu from the code that the engine already compiles Phases, Activity Groups and Steps into a node graph. The missing piece is a uniform per-Step contract, and Douglas committed to a PR adding that contract, a task-kind registry, diagrams, schemas and AI guardrails.
- **BMAD orchestrator & agent tooling**: Douglas added async test-design/QA steps to the orchestrator, landed the biox change and built two debug skills (session-level and BMAD system-level). He also restricted process/repo changes to himself and Ankit Mittal after non-BMAD test files were committed directly.
- **Project Surf delivery & QA**: Builds 25.21 and 113.25 went to QA. Douglas took on Karan Kapoor's two 113.25 fixes, started investigating the missing `assign-activity` Backoffice role, and agreed to reassign the audit-history follow-up and Story 0.124 away from Ankit.
- **Testing strategy**: QA should run real workflows, not mocks. The team prioritized environment-agnostic E2E automation on all PRs, agreed on a repo skill for API test-data seeding, and found that the canonical-structure linter had deleted Aseem's 20 screen tests on Nov 13.
- **Hiring**: Douglas interviewed a Senior Software Developer candidate (Mon, with Craig Stickel) and Saeed Pouryazdian for Senior MLOps (Thu, with Marnix Faes). He gave low-confidence feedback on Verne and a "wait and evaluate others" view on another candidate, and submitted a friend referral.
- **Model evaluation**: Sol 6.2 medium appears to beat Opus 5.5 medium at about a sixth of the cost per task ($0.41 vs $2.45). Opus still leads at xhigh/max effort, and a head-to-head test is planned.
- **Team changes & process**: Thom Oguntoyinbo resigned (last day Friday). Ankit now owns discovery and Douglas owns implementation, and the team agreed on quarterly code-health cleanup epics and on keeping every design element in the shared library.

## Key Accomplishments
- Halved the Surf architecture doc and cleaned up the Super BMAD architecture docs, which gives agents a clearer reference.
- Corrected the workflow-engine architecture write-up, steering the team toward extending the existing engine instead of building a new node model.
- Proposed a six-part per-Step contract (inputs, result, decider, side effects, safe rerun, audit) so new AI Steps can plug in without engine changes.
- Updated the orchestrator with async test-design/QA steps and merged the biox orchestrator change.
- Introduced two debug skills that separate harness/CLI/model problems from code-level BMAD problems.
- Sent builds 25.21 and 113.25 to QA, and took ownership of the 113.25 follow-up fixes.
- Found the root cause of Aseem's lost screen tests (the linter enforcing the canonical structure) and agreed on a linter-ignored test folder.
- Unblocked local Project Surf testing with a WorkOS setup that works with dev.
- Ran two technical interviews and gave structured feedback to hiring managers.
- Produced a cost/quality comparison that could cut agent costs at medium effort.

## Decisions Made
**Architecture & tooling**
- **Extend the existing workflow engine and don't build a new node model**: the engine already runs a state machine with conditional transitions. The gap is the per-Step contract.
- **Address workflow engine gaps through a PR, not a meeting**: an async review of concrete diagrams and schemas is faster.
- **Add test design/QA steps to the orchestrator before story creation**: async epics had no structured test design.
- **Split debugging into session-level and BMAD system-level skills**: this keeps harness/model problems separate from code problems.
- **Only Ankit and Douglas may change process/repo structure**: this prevents drift after non-BMAD test files were committed directly.
- **Local WorkOS uses the simplest option that works with dev for now**: the long-term setup can wait for the Keycloak direction.
- **Telemetry files are still pushed to the repo for now**: they stay until Douglas finishes removing them.
- **Test Sol 6.2 medium against Opus 5.5 medium**: it may give similar quality at about a sixth of the cost.

**Testing & QA**
- **QA runs real workflows, not mocks**: this tests the file-upload and communication components end to end.
- **Prioritize E2E automation that is environment-agnostic and runs on all PRs**: the critical permitting/planning paths need early break detection.
- **Add a repo skill for on-demand test-data seeding through the API**: this replaces shared accounts and fills QA data gaps.

**Team & process**
- **Ankit owns discovery and Douglas owns implementation**: Ankit can work on design/QA pain points with Karan and Tim.
- **Reassign the audit-history follow-up and Story 0.124 away from Ankit**: Ankit is focusing on sbmad discovery, and Ryan Huang or another available engineer was suggested.
- **William Veldhuis focuses on Surf now**: joint work with Douglas moves to Q1.
- **Pre-generate epic explains before sprints, and run quarterly code-health cleanup epics**: this catches product gaps early and keeps the codebase healthy.
- **Every design element lives in the shared library**: this stops agents from building duplicate components.

**Hiring**
- **Verne: low confidence, and Craig's view should carry more weight**: the candidate would report to Craig, so a second round was suggested.
- **Marnix's candidate: hire only if the role is urgent**: otherwise keep evaluating candidates.

## Open Loops (End of Week)
- The `assign-activity` role is missing from Backoffice. This blocks Tasmia Shefa from testing the review flow.
- Story 113.25 fixes: exclude drafts from the attention summary and right-align the bell notice's View button.
- The audit-history follow-up and Story 0.124 need a new owner and sprint placement (0.124 is not in sprint 12).
- Dipak Parmar is still compiling the dev audit recovery notes in PR #5277.
- Douglas's referral is with Samiha Nusrat and Samuel Couture Brochu, waiting for next steps.
- Workflow engine PR (contract, task-kind registry, diagrams, schemas, guardrails): committed to Samuel on 11-18 and not yet opened.
- Hiring: the scorecard for Saeed Pouryazdian is due in Greenhouse, and the decision on Verne is waiting on Craig Stickel.
- Aseem needs to restore the 20 deleted screen tests into a linter-ignored folder. Timothy Meyer needs to create the tickets for the permitting E2E automation job.
- Undecided: an intermediate QA environment between dev and staging, and how to manage multiple test user accounts for E2E tests.
- **Possibly stale (not mentioned since 11-16, first raised on 11-13)**: the super-bmad AWS account setup (Dipak, PR #4949) and Karan Kapoor's PR review. The long-term local WorkOS environment decision and Amrita Patra's story 572 questions were also not mentioned again.

## Carried Into Next Week
- Ship the 113.25 fixes and ask Karan to recheck them on dev.
- Fix the `assign-activity` role mapping and grant the role to Tasmia.
- Release the new version with the debug skills, run a Surf story with Ankit shadowing, and target a Monday/Tuesday release.
- Make the orchestrator run the test-design skill during epic creation.
- Open the workflow engine PR for Samuel to review.
- Hold the Workflows conversation with Marnix Faes on Monday.
- Run the Sol 6.2 medium vs Opus 5.5 medium test.
- Share the architecture cleanup doc with team leads, and review Samuel's PR on testing environments and module configuration.
- Document test-data seeding and create the seeding skill (Douglas or Dipak). Finish removing the telemetry files from the repo.
- Catch up with Ryan Huang. Confirm the owners for the audit-history follow-up and 0.124, and plan the handover now that Thom has left.

## Meetings & Collaboration
- About 21 meetings attended, including 4 Surf stand-ups, 4 Progress Check-Ins, 2 technical interviews, the quarterly Townhall, the CDI Steerco, Testing on CDI, Surf Build Sprint Planning, a 1:1 with William and Wiz onboarding
- Key collaborators: Samuel Couture Brochu, Ankit Mittal, Justin LaBrash, Timothy Meyer, Thom Oguntoyinbo, Dipak Parmar, Karan Kapoor, Tasmia Shefa, Marnix Faes, Samiha Nusrat, Craig Stickel, Aseem Gupta, William Veldhuis, Ryan Huang, Onildo Aguiar

## Data Source Coverage
| Day | Calendar | Gmail | Slack | Drive |
|-----|----------|-------|-------|-------|
| Mon | ✅ | ❌ needs re-auth | ✅ | ✅ Gemini notes via connector (local sync not configured) |
| Tue | ✅ | ❌ empty | ✅ | ❌ empty |
| Wed | ✅ | ❌ empty | ✅ | ❌ empty |
| Thu | ✅ | ❌ empty | ✅ | ❌ empty |
| Fri | ✅ | ❌ empty | ✅ | ❌ empty |

**Systemic gaps:** Gmail returned no data all week. The connector needs re-authentication. Drive returned data only on Monday, and `google_drive.local_path` is not configured. All five dailies are marked `quality: partial`. The dailies were committed to separate `claude/*` branches, not `main`.
