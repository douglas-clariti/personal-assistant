---
week: "2026-W48"
date_range: "2026-11-23 to 2026-11-29"
author: "douglas-clariti"
days_covered: 5
days_expected: 5
days_missing: []
tags:
  - project-surf
  - super-bmad
  - bmad
  - devops
  - ci
  - templates
  - qa
  - gis
  - sales-int
  - sentry
  - error-handling
  - observability
  - esri
  - code-review
  - incident-response
  - aws-cloudwatch
  - eks
  - pulumi
  - cdi
  - hiring
  - rec-2026-0064
  - openfga
  - compliance
  - temporal
  - postgresql
  - aurora
  - cognito
  - ai-models
---

# Weekly Rollup — 2026-W48

**2026-11-23 to 2026-11-29** | **5/5 days covered**

## Themes & Focus Areas
- **Project Surf 5xx errors & reliability**: Recurring 503/500 errors (template picker, sales-int portal submit, Record/Admin Review claim) ran through the whole week. Douglas corrected misused 500 status codes and committed to an error-response schema rewrite. He was still debugging the claim 503 on Friday, after DEV Temporal UI access came back.
- **DEV platform incident & observability**: The pooled DEV API lost its only pod and produced 801 HTTP 503s in seven minutes. Douglas wrote it up (PR #5613), recommended Story 0.58 (split liveness from DB readiness), and proposed CloudWatch Container Insights via Pulumi. Sentry was set up for the dev cluster (PR #5492), with a request to split alerts across more channels.
- **QA unblocking & bug fixes**: Douglas fixed the missing PLATFORM "User" tab and the legacy-citizen-role filter that hid staff from reviewer lists (Story 2.38). Both had been blocking Tasmia Shefa (Mia)'s QA on REC-2026-0064.
- **Super BMad & dev process**: Douglas held back super-bmad PR #1236 because it fixes the wrong place, pushed `/bmad-testarch-test-design` adoption, set the story-renumbering rule (Epic 78 precedent), and planned a new super-bmad release.
- **Infrastructure upgrades & access**: Douglas opened the PostgreSQL 18.6 upgrade (PR #5748) jointly with Dipak Parmar, with Temporal compatibility still to be validated. He has a pending request for Pulumi DEV testing guidance and read-only Temporal CLI access.
- **Hiring**: Douglas ran the technical interview and debriefs for Sowmiyaa Chakravarthy Vasan (Senior Applied AI Engineer).
- **CDI & company events**: Douglas attended CDI Session 1 (Product Vision & All-in-one Ecosystem). Friday was the office-closed Q4 Team Appreciation Day.

## Key Accomplishments
- Fixed the legacy-role reviewer filter (Story 2.38), so valid staff accounts are no longer hidden from Another Reviewer or rejected with a 403 on Assign to Yourself.
- Found and started fixing the missing PLATFORM "User" tab bug that was blocking Mia's ticket QA.
- Analyzed the pooled DEV API incident (801 × 503, 367 Sentry events in 7 min) and published the write-up and three remediation paths in PR #5613.
- Backed the Sentry rollout for the dev cluster (US region) and received PR #5492; approved Dipak's manual-run evidence PR #5509.
- Proposed CloudWatch Container Insights on DEV EKS through the Pulumi data-plane-platform stack, plus a runbook, to close the metrics gap the incident exposed.
- Opened the CDI PostgreSQL 18.6 upgrade PR #5748.
- Got DEV Temporal UI access back through the Cognito DEV pool invite, unblocking the Record claim 503 investigation (PR #5742).
- Unstuck Samuel Couture's CI run and helped Onildo Aguiar get access to project-surf.
- Ran the technical interview and two debriefs for the Senior Applied AI Engineer candidate.
- Gave UX feedback on the Project Surf application flow (GIS, address lookup, "not supported / out of range" messaging).

## Decisions Made
**Reliability & observability**
- **Story 0.58 first for DEV API resilience**: Splitting liveness from DB readiness and bounding graceful shutdown takes Temporal out of both health checks. A second replica stays an option, pending a Story 0.56 scope change.
- **Set up Sentry now (US region, dev cluster only)**: Dev bugs need visibility right away. CA data residency and the staging/prod rollout are deferred.
- **Keep the `trace_parent` column**: The choice is easy to reverse.
- **PostgreSQL 18.6 upgrade goes ahead as a joint effort with Dipak**: Temporal compatibility gets validated as part of PR #5748.

**Product & bug fixes**
- **Remove the legacy-role check from the reviewer list and Assign to Yourself**: OpenFGA, active-staff, department and qualification checks still apply.
- **Address-not-found UX**: Tell users an address is "not supported" or "out of range" instead of failing silently.

**Process & tooling**
- **super-bmad PR #1236 not released**: It fixes the wrong place.
- **Aseem Gupta adopts `/bmad-testarch-test-design`**: Test design should go through the BMAD test-architecture workflow.
- **Story-number collisions follow the Epic 78 precedent; use a CI guard, not a local warning**: Renumbering is the practical fix, and a local warning is overkill.
- **Aseem can merge without waiting on Douglas's ignore-file changes**: Avoids blocking his work.
- **Pick 2 of 3 options (with Samiha Nusrat and Marnix Faes)**: Limited time available.
- **Skip Thursday's Project Surf stand-up**: To focus on bug fixes and platform optimization.

## Open Loops (End of Week)
- PR #5748 (CDI PostgreSQL 18.6) is awaiting review from Dipak Parmar and Simone Giacomel, including upgrade/rollback steps and Aurora parameter-group handling.
- Read-only Temporal CLI access in DEV (`CDIDeveloper` profile is denied port-forward/exec) was requested from Dipak, with no response yet.
- The Record claim 503 investigation (PR #5742) still needs the workflow history pulled from `cell-pooled-dev` around 18:43:22 UTC on Nov 26.

## Carried Into Next Week
- Root cause of the Record/Admin Review claim 503 on REC-2026-0064 (waiting on Mia's request ID); confirm the Story 2.38 fix is on DEV and Mia's retry succeeds.
- Template-picker 503 on dev (5/40 Records; breaks Story 99.10 AC2): check the server log for request `ad2b5e73-…`. *Open since Mon; no resolution recorded.*
- Guidance to Timothy Meyer on PR #4772 (`work-item` check for planning-only / `roadmap/**` PRs). *Open since Mon; no resolution recorded.*
- Settle super-bmad PR #1236 with Ankit Mittal; release the new super-bmad version with release notes.
- Review Sentry PR #5492; split Sentry alerts into more channels; confirm the backoffice Sentry alert from Thursday was resolved.
- Rewrite the API error-response schema and audit the remaining wrong 5xx codes.
- Root cause of the sales-int/staging 503/500s (waiting on Timothy's request details); PR #5538 (currency/finance-settings fix) awaits review.
- DEV API remediation choice: Story 0.58 alone or plus a second replica. Also pending: approval and rollout window for CloudWatch Container Insights, and Onildo's approval of PR #5613.
- Dipak's guidance on testing Pulumi changes on DEV, and on the compliance waiting period before library upgrades.
- Ankit's priority triage of bugs filed by devs/product.
- Hiring decision for Sowmiyaa Chakravarthy Vasan; confirm the Greenhouse scorecard was submitted.
- Add files to the ignore list; follow up on GIS/address search in the Project Surf application flow; UI walkthrough with Onildo before implementation.

## Meetings & Collaboration
- About 13 meetings on the calendar (3 Progress Check-Ins, 3 Project Surf stand-ups including Mon (invited) and Wed (tentative), the 1:1 with William Veldhuis, the workflow-engine 1:1 with Marnix Faes, CDI Session 1, the technical interview, and 2 hiring debriefs). Douglas skipped Thursday's stand-up and declined Wednesday's End of Sprint Demo. Friday's office was closed.
- Key collaborators: Dipak Parmar, Timothy Meyer, Tasmia Shefa (Mia), Ankit Mittal, Samuel Couture, Justin Labrash, Marnix Faes, Aseem Gupta, Simone Giacomel, Onildo Aguiar, Samiha Nusrat, William Veldhuis, Colin John

## Data Source Coverage
| Day | Calendar | Gmail | Slack | Drive |
|-----|----------|-------|-------|-------|
| Mon | ✅ | ❌ needs re-auth | ✅ | ❌ not configured |
| Tue | ✅ | ❌ empty | ✅ | ❌ empty |
| Wed | ✅ | ❌ empty | ✅ | ❌ empty |
| Thu | ✅ | ❌ needs re-auth | ✅ | ❌ not configured |
| Fri | ✅ | ❌ empty | ✅ | ❌ empty |

**Systemic gaps:**
- Gmail returned no data all week because the connector needs re-authentication.
- Google Drive returned no data all week because `google_drive.local_path` is empty in config.yaml.
- Every daily was marked `quality: partial`.
- The daily summaries are pushed to separate `claude/*` branches, not to `main`, so they never reach main. This rollup was built from those branches.
