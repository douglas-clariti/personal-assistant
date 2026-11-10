---
date: "2026-11-10"
weekday: "Tuesday"
author: "douglas-clariti"
quality: "partial"
sources_used:
  - google_calendar
  - slack
  - google_drive (Gemini meeting notes via Drive connector)
sources_empty:
  - gmail (connector needs re-authentication)
  - google_drive_local (local_path not configured)
open_loops_carried: 10
tags:
  - project-surf
  - super-bmad
  - sprint-11
  - ga-planning
  - observability
  - cloudwatch
  - staging
  - authz
---

# Daily Summary — Tuesday, 2026-11-10

## Summary
- In the Douglas <> Sam 1:1, Sam and Douglas agreed that Douglas will split his time 50/50 between Super BMAD (improvements, DevOps and developer coaching) and core work. Douglas also committed to an architecture decisions document for the repo by next week (transcript available).
- Also in that 1:1, Douglas took on several Super BMAD skills: a shorter, PR-referenced "ask team member" skill, an SBMAD debug skill that shows state, logs and AWS links for a PR, and an update to the development process doc (transcript available).
- At the Project Surf Stand-up, Tim presented the post-beta plan: beta closed at 593 stories, the CORG pilot is on Dec 4, EPR beta is on Dec 18, Core R1 is on Jan 31, and Ankit and Douglas form the Super BMAD hardening team (transcript available).
- At the stand-up, Douglas reported on his story 113.1 work and offered to seed conditions so QA can close condition-dependent tasks. He also agreed to pick up Ryan's story 25.21 and its design story for Sprint 11.
- In the 1:1 with William, Douglas confirmed that William stays on Surf until the end of December and moves to Super BMAD in January. They agreed that stories must name the UI components to use, and Douglas committed to starting a Super BMAD V7 migration branch (transcript available).
- In the "Logs" meeting with Dipak, they agreed on CloudWatch for logs (with S3 long-term retention) and Grafana for metrics and alerts. They also agreed on per-cell subdomain URLs, and Douglas will open a SOC 2 sign-off ticket for copying the E2E data to the staging sales environment (transcript available).
- Douglas held his recurring Progress Check-In with Samuel, Justin and Ankit (transcript not available).
- In a Slack DM, Douglas helped Dipak with dev access. He asked whether he has the `cdi-nonprod-dev-us-east-2` profile, traced a workflow-library save failure to missing roles, and granted Dipak system-admin with `authz:grant-system-administrator` on `cell-pooled-dev`.
- In the same DM, Douglas told Dipak that the admin and implementation roles must be applied every time the user seed runs (`bun run command seed:users <ENV>`), that he needs to check why it didn't run, and that some of his PRs were never merged.
- In #project-surf-build, Douglas told Thom and Aseem that the "Containing Project on terminal records" fix is done and that "Mark Satisfied with no evidence" stays blocked until there is a story for an evidence screen. He later confirmed nothing more is needed on Mark Satisfied for now.
- Douglas asked Thom in #project-surf-build to assign him the GA tasks so he can start right away. He told Shrey in a DM that story 113.1 was missing parts and isn't deployed yet because of a CI issue.

## Decisions & Rationale
- **Douglas splits his time 50/50 with Super BMAD**: Super BMAD is the long-term base for scaling the team, while Surf is day-to-day feature delivery. Non-urgent stories get delegated.
- **AI communications go through PRs and repos, and Slack is for people**: This lets agents find decisions in the codebase instead of searching Slack.
- **Architecture review is required before new epics**: About 80% of architecture decisions are currently made after the code is built.
- **Staging deployments follow the formal SOC 2 release process**: Only designated release managers cut and merge releases, and proof-of-concept deployments are handed to Simone and Dipak.
- **CloudWatch for logs, Grafana for metrics and alerts**: CloudWatch logs are cheaper and S3 makes long-term retention easy, while Grafana provides Kubernetes dashboards and alerting.
- **Each cell gets its own subdomain URL**: This is the simplest way to route tenants across cloned cells.
- **Copy staging data through a controlled SOC 2 exception, not a custom script**: It is a one-time transfer and the exception creates an audit trail.
- **Stories must name their UI components**: Vague stories led to duplicate components and map styling errors.
- **"Mark Satisfied with no evidence" stays blocked**: There is no screen yet for adding evidence or links.

## Open Loops
- Sign-off from Sam or Craig on the staging E2E data copy, and Dipak to confirm the data-copy requirements.
- Douglas to send Thom and Timothy (and Justin, if available) a meeting invite for follow-ups.
- Thom to set up the conditions session with Karen from the enterprise team (Justin and Douglas invited).
- Douglas to contact PNT about holiday group membership.
- Find out why the user seed didn't apply the admin and implementation roles in dev.
- Douglas's old PRs that were never merged.
- Thom to assign the GA tasks to Douglas (asked in #project-surf-build).
- Story 113.1 deployment, waiting on the CI fix.
- Dipak to ping Douglas to verify the cluster setup once the staging migration steps are done (carried from 2026-11-09).
- Dipak to check with Eric on Blue Beam credential management (carried from 2026-11-09).
- Dipak to provide the scoped Grafana IAM role (carried from 2026-11-09).
- Review of Ankit's pending work (carried from 2026-11-09).
- Staging release blocked on Dipak's remaining infra PRs for story 9.97 (carried from 2026-11-06).
- Confirmation from Onildo that the project-surf `app-deploy.yml` run for 80.21 succeeded (carried from 2026-11-06).
- Thom to create clock rules and send links for seeding the SLA test records (carried from 2026-11-06).
- Tasmia Shefa's request (carried from 2026-11-06).
- PR reviews pending: super-bmad #1251, project-surf #4048 and #4340 (carried from 2026-11-06).
- Thom to confirm with Tim and Ken whether 14.3 is a duplicate (carried from 2026-11-06).

## Blockers
- Story 113.1 can't be deployed until the CI problem is fixed.
- The staging data copy needs SOC 2 sign-off from Sam or Craig.
- Pulumi layer dependencies and Aurora migration-script failures are slowing cell provisioning (Dipak).

## Next Steps
- Create the SOC 2 tracking ticket for the staging E2E data copy, then run the copy once it is approved.
- Pick up story 25.21 and its design story for Sprint 11.
- Seed conditions data in dev so QA can close condition-dependent tasks.
- Start the Super BMAD V7 migration branch.
- Draft the architecture decisions document for the repo (due next week).
- Update the "ask team member" skill, build the SBMAD debug skill, and update the development process doc.
- Send the follow-up invite to Thom and Timothy, and contact PNT about holidays.
- Find out why the user seed skipped the role assignment, and revisit the unmerged PRs.
- Remove the hardcoded WorkOS organization IDs (carried from 2026-11-09).

## Transcript Source (Cleaned)
I started the morning in #project-surf-build, telling Thom and Aseem that the "Containing Project on terminal records" fix is done. "Mark Satisfied with no evidence" has to stay blocked because we don't have a screen for adding evidence yet. I also told Thom the fixes would be in dev soon. I spent part of the morning in DMs with Dipak about dev access and K8s errors whose logs I couldn't see. I also told Shrey that story 113.1 was missing parts and isn't deployed yet because of a CI problem.

In my 1:1 with Sam, we agreed I'll spend half my time on Super BMAD: improvements, DevOps and coaching developers. I'll write an architecture decisions document for the repo by next week. We agreed that AI-generated communication should point to PRs and repos instead of cluttering Slack, so I'll update the "ask team member" skill and build an SBMAD debug skill. Sam also asked me to hand over proof-of-concept deployments to Simone and Dipak, because staging now follows the SOC 2 release process. He reminded me that architecture reviews need to happen before new epics. Sam explained that the Super BMAD shift is about leverage, not a step back from Surf.

Then I had my 1:1 with William. He's moving tickets through QA and has learned T3 and Super BMAD. He'll stay on Surf until the end of December and then join Super BMAD in January. We agreed that stories must name the UI components to use, and I'm going to start a Super BMAD V7 migration branch.

At the Project Surf Stand-up, Tim walked through the post-beta plan: beta closed with 593 stories, the CORG pilot is on Dec 4, EPR beta is on Dec 18, Core R1 is on Jan 31, and there's a pause and reset the week of Dec 14. Ankit and I are now the Super BMAD hardening team. I gave my update on 113.1, offered to seed conditions so QA can close those tasks, and said I'd pick up Ryan's 25.21 and its design story. I also need to talk to PNT about the holiday group and send Thom and Tim a follow-up invite. Right after, I had my Progress Check-In with Samuel, Justin and Ankit.

In the afternoon, Dipak and I met about logs. We settled on CloudWatch for logs with S3 retention and Grafana for metrics and alerts, and on per-cell subdomain URLs. I'll create a ticket for SOC 2 sign-off on copying the E2E data to the staging sales environment and offered to do the copy myself. Afterwards, I helped Dipak in DMs: his workflow-library save was failing because his user was missing roles. I granted him system-admin on cell-pooled-dev and explained that the seed script should apply the admin and implementation roles. I need to check why it didn't run, and I admitted a few of my PRs were never merged. I finished by asking Thom to assign me the GA tasks so I can start right away.
