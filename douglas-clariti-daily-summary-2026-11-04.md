---
date: "2026-11-04"
weekday: "Wednesday"
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
  - staging-release
  - ci-cd
  - aws
  - conditions
  - flags
  - dashboard
  - qa
---

# Daily Summary — Wednesday, 2026-11-04

## Summary

- Douglas met with Thom Oguntoyinbo in "Sync on 14.3". They paused the separate supervisor dashboard (story 14.3), agreed to accept AI-generated UI stories at about an 85% design match, and agreed to ship the simplest beta version of record flags (story 10.16) (transcript available).
- Douglas attended the Project Surf Stand-up and reported dev fixes landed for Aseem and Eric, Karan's QA feedback being addressed, pentest support for Craig, and staging-release testing in progress (transcript available).
- Douglas ran the Progress Check-In with Samuel Couture, Justin LaBrash, and Ankit Mittal (transcript not available).
- Douglas joined "Conditions: how they hold a Workflow" with Thom, Justin, and Timothy. He pushed back on tying Conditions to canonical phases, questioned whether a separate Conditions library is needed, and asked sales for concrete examples before design decisions are made (transcript available).
- Douglas fixed the release workflow's Git authentication failure in project-surf PR #4385 and sent Dipak Parmar a written status of what was done and what is still missing, plus a standalone HTML dependency graph of the staging release (Story 9.27).
- Douglas found that the latest release run fails at the AWS credentials step because `SURF_RELEASE_ROLE_ARN` is missing, and asked Dipak for the value.
- Douglas handed the AWS-account part of staging-release testing over to Dipak in #project-surf-build, and told the channel that the latest dev changes would be deployed to staging soon.
- Douglas asked Dipak to migrate the deprecated Pulumi `s3.BucketV2` resources, and confirmed the agreed staging deployment cadence of Wednesday and Friday, end of day, until the PMs say otherwise.
- Douglas asked Samuel to review super-bmad PR #1251 and offered to upgrade super-bmad on a separate release branch.
- Douglas asked Onildo Aguiar to approve project-surf PR #4048, sent Timothy Meyer PR #4340, and noted in #cdi-alerts-dev that Onildo is handling the open alert.
- Douglas told #surf-compliance that his compliance item is blocked until the new staging deployment goes out.

## Decisions & Rationale

- **Pause the separate supervisor dashboard (14.3) and close its PR**: It may duplicate the standard user dashboards, and Thom will check with Tim and Ken.
- **Accept UI design stories at about an 85% match**: AI agents can't reliably reproduce exact font weights and spacing, and chasing 100% causes endless refinement rounds with Karen.
- **Build the simplest beta version of record flags (10.16)**: Testing every record-locking edge case costs too much in QA and CI time for the user value it adds.
- **Simplified V1 for Conditions (block only the next phase or issuance)**: This covers an estimated 80% of use cases. The final phase-blocking model waits until the team has reviewed the Salesforce flow with sales.
- **Hand AWS-account release testing to Dipak**: Dipak is already creating the AWS accounts, so it is easier for him to test.
- **Staging deploys twice a week (Wednesday and Friday, end of day)**: This holds until the PMs say otherwise.

## Open Loops

- Waiting on Dipak or DevOps for `SURF_RELEASE_ROLE_ARN`, plus the release and approval IAM roles, OIDC trust, release-store infrastructure, `SURF_RELEASE_PUSH_ROLE_ARN`, and `SURF_RELEASE_STORE_BUCKET`.
- Signing still needs checking: AWS Signer profile `surf_release_images`, ECR managed signing, and candidate signature verification.
- Waiting on Thom to confirm with Tim and Ken whether the supervisor dashboard story is a duplicate.
- Waiting on Thom to set up the sales demo of the Salesforce Conditions flow and to share examples before the Conditions architecture is decided.
- PR reviews are still pending: super-bmad #1251 (Samuel), project-surf #4048 (Onildo), and #4340 (Timothy).

## Blockers

- The staging release is blocked because the latest release run fails at the AWS credentials step: `SURF_RELEASE_ROLE_ARN` is missing.
- The #surf-compliance item and the Lakewood and Southampton staging checks are blocked until the new staging deployment goes out.

## Next Steps

- Close the 14.3 dashboard PR, saving the work, and schedule a follow-up on dashboard status for next week.
- Audit and close the redundant 98-series stories in QA (about 5 are actually needed).
- Talk with Thom about the status of the four pending stories.
- Give Justin and the team a staging update timeline, together with Samuel.
- Finish the staging deploy once Dipak has provisioned the AWS role and accounts.

## Transcript Source (Cleaned)

I started the morning in DMs with Dipak about the staging deployment. We confirmed the Wednesday/Friday end-of-day cadence, and I asked him to migrate the deprecated Pulumi S3 BucketV2 resources while he's in there. I sent Sam super-bmad PR #1251 for review and offered to upgrade super-bmad on a separate release branch.

At 10:00 I synced with Thom on story 14.3. We paused the separate supervisor dashboard because it may duplicate the user dashboards, agreed that UI stories are done at about an 85% design match, and agreed to build the simplest beta version of record flags (10.16). I'm closing the 14.3 PR and cleaning up the 98-series stories in QA.

Late morning I flagged another GitHub outage in #project-surf-build and announced that I'm testing the staging deploy process. I also told #surf-compliance that my item is blocked on staging, asked Onildo to approve PR #4048, and sent Tim PR #4340.

Around noon I worked through Sam's release workflow for the first time. I fixed the Git authentication failure in PR #4385 and found that the release run fails because SURF_RELEASE_ROLE_ARN is missing. I sent Dipak a write-up of what's done and what's missing (based on Story 9.27 and AD-D131), plus an HTML dependency graph, and then handed the AWS-account side over to him.

At the 12:30 Project Surf Stand-up I reported the fixes that landed on dev, my pentest support for Craig, and the staging-release testing. Sam and I owe the team a staging timeline. After that I ran the Progress Check-In with Sam, Justin, and Ankit.

At 14:45 I joined Thom, Justin, and Tim on how Conditions hold a Workflow. I pushed back on tying Conditions to canonical phases, questioned whether a separate library is needed (sales wants it for reuse), and asked for concrete sales examples before we decide. The group leaned toward a simplified V1 that blocks only the next phase or issuance.
