---
week: "2026-W46"
date_range: "2026-11-09 to 2026-11-15"
author: "douglas-clariti"
days_covered: 5
days_expected: 5
days_missing: []
tags:
  - project-surf
  - core-beta
  - sprint-11
  - ga-planning
  - workos
  - grafana
  - observability
  - cloudwatch
  - staging
  - super-bmad
  - sbmad
  - authz
  - surf-discovery
  - one-on-one
  - progress-check-in
  - standup
  - design-system
  - figma
  - ci-pipeline
  - devops
  - pentest
  - aws
  - telemetry
  - claude-code
---

# Weekly Rollup — 2026-W46

**2026-11-09 to 2026-11-15** | **5/5 days covered**

## Themes & Focus Areas
- **Post-beta transition & Sprint 11**: Beta closed at 593 stories, and all of Douglas's core-beta stories are in QA. Tim set the next dates: CORG pilot Dec 4, EPR beta Dec 18, Core R1 Jan 31. Douglas took 13.3, 25.21 (plus its design story), 113.1 and 98.81, and asked Thom for the GA tasks.
- **Shift to Super BMAD (50/50 split)**: Sam and Douglas agreed he spends half his time on Super BMAD (improvements, DevOps, coaching). Douglas and Ankit are now the hardening team, and William joins in January. Douglas committed to an architecture decisions doc, new skills (ask-team-member, SBMAD debug), a V7 migration branch, and a separate AWS account for a telemetry sync server (PR #4949).
- **Observability & infra with Dipak**: Settled on CloudWatch for logs (S3 for long-term retention) and Grafana for metrics and alerts, with per-cell subdomain URLs. Agreed to remove the hardcoded WorkOS org IDs. Dipak confirmed Kubernetes 1.37 and the Aurora migration, and Douglas fixed Dipak's dev access (missing roles).
- **CI performance & DevOps access**: CI averages about 14 min, with 22 min at the 90th percentile. Douglas proposed cleaning up the tests and trying blacksmith.sh, and joined the DevOps group to update super-bmad CI checks (infra changes still reviewed by Simone/Dipak). A CODEOWNERS bypass was spotted.
- **Design system & QA scope**: The applicant-portal "Action Required" bento became a new O-13 organism (PR #4868), unblocking Story 98.81. Douglas asked QA to keep fixes within each story's scope, and stories must now name the UI components they use.
- **Pen-test & SOC 2 process**: Staging now follows the formal SOC 2 release process, and the staging E2E data copy needs a SOC 2 exception sign-off. After the environment reset, Craig lost access to the pentest accounts. Douglas handed pen-test account sharing over to Dipak's team.

## Key Accomplishments
- Finished all core-beta stories (in QA) and moved onto Sprint 11 and GA work. The "Containing Project on terminal records" fix is done.
- Agreed a 50/50 Super BMAD role with Sam, which sets Douglas up as the base for scaling the team's AI-driven delivery.
- Settled the observability architecture (CloudWatch + S3 for logs, Grafana for metrics and alerts) and per-cell subdomain routing with Dipak.
- Unblocked Dipak in dev by tracing a workflow-library save failure to missing roles and granting system-admin on `cell-pooled-dev`.
- Got the O-13 Action Required organism specified and merged (PR #4868), so Story 98.81 is ready.
- Analysed CI performance, proposed a blacksmith.sh trial and test clean-up, and joined DevOps so he can update super-bmad CI checks himself.
- Started the super-bmad telemetry sync server (PR #4949) and requested an isolated AWS account ("CDI Internal Dev").
- Coached the team on Super BMAD usage: `/sbmad-pr-goal` for watching PRs (Shrey), and opening agent PRs via `pr-open.yml` (Karan).
- Clarified the pentest account policy (stay enabled, MFA left un-set-up) and moved ownership to infra/compliance.

## Decisions Made
**Role & process**
- **50/50 split with Super BMAD**: Super BMAD is the long-term base for scaling the team. Non-urgent Surf stories get delegated.
- **AI communications go through PRs/repos, and Slack is for people**: Agents can then find decisions in the codebase.
- **Architecture review before new epics**: About 80% of architecture decisions are currently made after the code is built.
- **Stories must name their UI components**: Vague stories led to duplicate components and styling errors.
- **Keep QA fixes within the current story's scope**: Temporary testing aids (e.g. the tooltip) are removed by later stories.
- **Use the existing `/sbmad-pr-goal` instead of a new `/sbmad-watch-pr`**: It already covers watching PRs.
- **Douglas joins the DevOps group**: So he can update super-bmad CI checks himself. Infra changes still go to Simone/Dipak for review.

**Infra & observability**
- **CloudWatch for logs, Grafana for metrics and alerts**: CloudWatch logs are cheaper with easy S3 retention, and Grafana gives Kubernetes dashboards and alerting. This narrows Monday's interim choice of AWS Managed Grafana, with Grafana work done in Surf Labs.
- **Per-cell subdomain URLs**: The simplest way to route tenants across cloned cells.
- **Multiple migration streams, one per cell**: Each cell applies the migrations for the products it runs.
- **Remove hardcoded WorkOS org IDs and retire the old WorkOS IDs**: Static prototype IDs break tenant-based auth.
- **Drop the Kubernetes-upgrade story**: The cluster is already on 1.37.
- **Separate AWS account for super-bmad servers**: Keeps them isolated from Surf infrastructure.
- **Dev is the target environment, not staging**: Communicated to Onildo.

**Compliance & pen-test**
- **Staging follows the formal SOC 2 release process**: Only release managers cut releases, and proof-of-concept deployments go to Simone/Dipak.
- **Copy staging E2E data through a SOC 2 exception, not a custom script**: It is a one-time transfer, and the exception creates an audit trail.
- **Pentest accounts stay enabled with MFA left un-set-up**: Testers get the full experience.
- **Pen-test account sharing handed to Dipak's team**: Three conflicting requests came in.

**Product**
- **Action Required bento becomes a new O-13 organism**: It is a new component, not part of O-11.
- **"Mark Satisfied with no evidence" stays blocked**: There is no evidence screen yet.

## Open Loops (End of Week)
From the latest daily (2026-11-13):
- Dipak to set up the super-bmad AWS account (details in PR #4949).
- Simone/Dipak to confirm the pentest credentials and restore Craig Stickel's staging access.
- Karan Kapoor to send his PR for review.

## Carried Into Next Week
- Super BMAD AWS account provisioning, and testing the telemetry sync server.
- Restore Craig's staging pentest access.
- Review Karan's PR.
- Story 98.81 (O-13 Action Required). Note: there is no data field for blocking fees, so flag it if that blocks.
- Finish story 25.21 and the PM story-creation change. Timothy still has to rebase from `develop` and retest.
- Operator console UI shell session with Timothy (stories 57.2, 57.10).
- Architecture decisions document (due this coming week, per the Nov 10 1:1 with Sam).
- Super BMAD V7 migration branch, the ask-team-member/SBMAD debug skills, and the development process doc update.
- Look into the CODEOWNERS bypass, and plan the blacksmith.sh trial and test clean-up with Samuel.
- Douglas's unmerged PRs (raised Nov 10, still open Nov 12).
- SOC 2 ticket and sign-off (Sam/Craig) for the staging E2E data copy.
- Remove the hardcoded WorkOS org IDs. Last listed Nov 10, with no update since.
- Find out why the user seed skipped the admin/implementation roles.
- Story 113.1 deployment, waiting on a CI fix (no update after Nov 10).
- **Stale (open since 2026-11-06 or earlier, last listed 2026-11-10, never marked resolved):** Dipak's remaining infra PRs for story 9.97, Onildo's confirmation of the 80.21 deploy, Thom's clock rules for the SLA test records, Tasmia Shefa's request, PR reviews (super-bmad #1251, project-surf #4048, #4340), and Thom's check on whether 14.3 is a duplicate.
- Other items last listed Nov 9–10 with no update: the scoped Grafana IAM role, Blue Beam credentials (Dipak with Eric), the cluster verification ping, reviewing Ankit's work, the conditions session with Karen, contacting PNT about holidays, and the follow-up invite to Thom/Timothy.

## Meetings & Collaboration
- About 17 meetings on the calendar: 14 confirmed attended, plus 3 with RSVP pending (Wed stand-up, Wed Surf Discovery sync, Fri stand-up).
- Key collaborators: Dipak Parmar, Samuel Couture, Thom, Timothy Meyer, Ankit Mittal, Justin Labrash, William Veldhuis, Karan Kapoor, Tasmia Shefa, Simone Giacomel, Craig Stickel, Ryan Huang, Shreyansh Kumar, Onildo Aguiar, Amrita Patra.

## Data Source Coverage
| Day | Calendar | Gmail | Slack | Drive |
|-----|----------|-------|-------|-------|
| Mon 11-09 | ✅ | ❌ re-auth needed | ✅ | ✅ Gemini notes (connector) |
| Tue 11-10 | ✅ | ❌ re-auth needed | ✅ | ✅ Gemini notes (connector) |
| Wed 11-11 | ✅ | ❌ not authorized | ⚪ no messages sent | ❌ no local path |
| Thu 11-12 | ✅ | ❌ re-auth needed | ✅ | ❌ (Gemini notes linked from calendar) |
| Fri 11-13 | ✅ | ❌ re-auth needed | ✅ | ❌ no local path |

**Systemic gaps:**
- **Gmail returned no data all week.** The connector needs re-authentication.
- `google_drive.local_path` is not configured in config.yaml, so Drive coverage depended on the connector (Mon/Tue only).
- **Carry-over chain broke on 11-11.** That daily found no previous summary and reset its open loops, likely because each daily is committed to its own unmerged `claude/*` branch rather than `main`. Many loops from Nov 6–10 have no resolution recorded and may be lost unless the dailies are merged to `main`.
