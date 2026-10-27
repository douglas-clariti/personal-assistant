---
date: "2026-10-27"
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
  - staging
  - pentest
  - compliance
  - bmad
  - onboarding
  - aws-bedrock
  - workflows
---

# Daily Summary — Tuesday, 2026-10-27

## Summary
- Douglas held a 1:1 with William Veldhuis (Google Meet), shared the BMAD method repo and docs with him, sent him repo invitations, and later ran a "Walkthrough CDI/Super Bmad" session with him (transcript available).
- Douglas attended Craig Stickel's "Secure Development Process/Compliance Discussion" as one of three required attendees raising execution-risk concerns about compliance guards in the dev pipeline (transcript available).
- Douglas attended the Project Surf Stand-up (transcript available) and ran his recurring Progress Check-In with Samuel Couture, Justin LaBrash and Ankit Mittal (transcript not available).
- Douglas sent Craig Stickel the Project Surf vendor list over Slack DM: AWS, WorkOS (to be replaced by Sam's solution), OnlyOffice, ArcGIS, Bluebeam, Temporal, Grafana, Pulumi, GitHub and Sentry, plus AWS Bedrock for AI.
- Douglas redeployed staging for the second time with fixes (#project-surf-build) for Justin LaBrash's Internal POC team, then started looking into Justin's report that new applications fail with invalid form/intake errors on staging.
- Douglas agreed in #project-surf-build to create pentester accounts on staging, after Samuel Couture proposed generic `pentest+<role>@claritisoftware.com` aliases (one per role plus a fake citizen) with credentials stored in an RPass vault.
- Douglas approved Ankit Mittal's implementation in #project-surf-build, noting that permissions, roles and the IdP will need revisiting later.
- Douglas told Onildo Aguiar in #project-surf-build that he would merge story 98.18 today, which unblocks Onildo's design component story 98.52.
- Douglas offered to pair with Timothy Meyer after the daily on the remaining 78.50 follow-ups: the misleading error state shown before save, and the Gate label requirement from 109.23.
- Douglas onboarded Simone Giacomel over Slack DM: treat `_bmad-output/` as the only source of truth (not `docs/`), use `/bmad-help`, and offered a 30-minute session on ticket handling and the dev cycle.
- Douglas shared Project Surf PR #3642 with Samuel Couture and mentioned a Docker image he built with all dependencies for testing on AWS.

## Decisions & Rationale
- **Approved Ankit's implementation as is**: no time for a deep review now; permissions, roles and the IdP will be revisited later anyway.
- **Pentest accounts via generic role-based aliases in an RPass vault**: Samuel's approach covers every role while keeping credentials centralized; Douglas took the task.
- **Use AWS Bedrock as the AI vendor**: shared with Craig as part of the vendor inventory for compliance.
- **`_bmad-output/` is the source of truth for new joiners**: `docs/` is not kept up to date while the process keeps changing.

## Open Loops
- Create the staging pentest accounts (one per role plus a fake citizen) and send the credentials to Craig Stickel; Samuel flagged this as urgent.
- Merge story 98.18, which blocks Onildo's 98.52.
- Find the cause of the staging bug where new applications show invalid form/intake errors (Justin LaBrash); Douglas suspects it is related to the workflow error-message bug he is fixing.
- 78.50 follow-ups with Timothy Meyer: the error state shown before save, and Gates that cannot be named but must have a label to publish (109.23).
- Simone Giacomel has been offered a 30-minute session on BMAD and the dev cycle; it is not yet scheduled.

## Blockers
- Staging: new applications cannot be started (invalid form/intake errors), which blocks the Internal POC team.
- Story 98.52 (Onildo Aguiar) is waiting on 98.18 to merge.

## Next Steps
- Prepare small starter tasks for William Veldhuis (promised for tomorrow).
- Set up the pentest accounts and RPass vault, then send the details to Craig.
- Merge 98.18 and check that the staging workflow fix resolves Justin's issue.
- Pair with Timothy on the 78.50 and 109.23 UI issues.
- Plan the scheduled Claude job that keeps project documentation up to date.

## Transcript Source (Cleaned)
I started the day with a 1:1 with William, where I pointed him to the BMAD method repo and docs and sent him invitations to our repos. Later in the afternoon I ran a walkthrough of CDI and Super Bmad with him, and I told him I'll prepare some small tasks for him tomorrow.

At 11:30 I joined Craig's Secure Development Process and Compliance discussion. Sam, Craig and I were the three people raising execution-risk concerns about adding compliance guards without slowing the pipeline down. Afterwards I sent Craig our full vendor list (AWS, WorkOS, OnlyOffice, ArcGIS, Bluebeam, Temporal, Grafana, Pulumi, GitHub, Sentry) and said we plan to use AWS Bedrock for AI. Then I attended the Project Surf stand-up and my Progress Check-In with Sam, Justin and Ankit.

In #project-surf-build, I redeployed staging with a second round of fixes for Justin's Internal POC team. Justin still can't start new applications on a newly configured workflow, so I'm checking whether it's related to the workflow error-message bug I'm fixing. Craig and Sam need pentester accounts on staging urgently. Sam proposed role-based generic aliases with credentials in an RPass vault, and I'm on it. I approved Ankit's implementation for now, with permissions, roles and the IdP to be revisited. I told Onildo I'd merge 98.18 today, and I offered Timothy a pairing session after the daily on the remaining 78.50 UI issues.

I also helped Simone get started with BMAD: `/bmad-help`, and `_bmad-output/` as the source of truth instead of `docs/`. I offered her a 30-minute session on how we handle tickets. With Sam, I shared PR #3642 and talked about the Docker image I'd built for testing on AWS.
