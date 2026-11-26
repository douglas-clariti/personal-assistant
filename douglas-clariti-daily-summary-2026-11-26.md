---
date: "2026-11-26"
weekday: "Thursday"
author: "douglas-clariti"
quality: "partial"
sources_used:
  - google_calendar
  - slack
sources_empty:
  - gmail (connector needs re-authentication)
  - google_drive (local folder not configured)
open_loops_carried: 0
tags:
  - project-surf
  - hiring
  - rec-2026-0064
  - openfga
  - super-bmad
  - pulumi
  - qa
  - compliance
---

# Daily Summary — Thursday, 2026-11-26

## Summary
- Douglas conducted the Technical Interview with Marnix Faes for Sowmiyaa Chakravarthy Vasan (Senior Applied AI Engineer) on Google Meet (transcript available).
- Douglas joined a debrief with Marnix and a Senior Applied AI Engineer debrief panel with Samiha Nusrat, Samuel Couture and Marnix to assess the candidate (transcript available).
- Douglas hosted the Progress Check-In with Samuel Couture, Justin Labrash and Ankit Mittal (transcript available).
- Douglas skipped the Project Surf Stand-up and posted in #project-surf-build that they were focusing on bug fixes and platform optimization, with QA tasks posted in the channel and stories (stand-up transcript available).
- Douglas retested the Admin Review (ETW) claim on DEV for REC-2026-0064 and shared in #project-surf-build that it returned 200 after joining ETW Admin Reviewers; the cause of Mia's earlier 503 is still open.
- Douglas identified and fixed why Tasmia Shefa (Mia) was missing from Another Reviewer on REC-2026-0064: the backend filtered out staff accounts that still carry the legacy citizen role (Story 2.38).
- Douglas told Dipak Parmar the latest fix was deployed, asked how to test the Pulumi changes on DEV before merging, and asked about the compliance waiting period before upgrading to new library versions.
- Douglas shared project-surf PR #5674 with Simone Giacomel, noting the coding agent's misbehavior there.
- Douglas responded to a Sentry alert in #cdi-alerts-sentry-backoffice ("On it").
- Douglas asked Tasmia Shefa (Mia) to test the fix again by DM.
- Douglas was locked out of his Google account and worked with Marnix Faes and Colin John to reset the password.

## Decisions & Rationale
- **Remove the legacy-role check from the reviewer list and the Assign to Yourself write path**: valid staff accounts that still had the old citizen role were filtered out or rejected with a 403; OpenFGA permission, active staff status, department membership and reviewer qualification checks still apply.
- **Skip the Project Surf daily stand-up**: to focus on bug fixes and platform optimization.

## Open Loops
- Root cause of Mia's earlier 503 on the REC-2026-0064 Admin Review claim is still unknown; Douglas is waiting for Mia's retry time and request ID.
- Legacy-role reviewer fix (Story 2.38) passed local regression tests and is pending DEV deployment; Mia needs to retry Assign to Yourself after the deploy.
- Waiting on Dipak Parmar for the compliance-required waiting period before library upgrades.
- Waiting on Dipak Parmar for guidance on testing Pulumi changes on DEV before merging.
- Hiring decision for Sowmiyaa Chakravarthy Vasan (Senior Applied AI Engineer) after the debriefs; Greenhouse scorecard submission not confirmed.
- Sentry alert in #cdi-alerts-sentry-backoffice that Douglas picked up; resolution not confirmed.

## Blockers
- Google account password lockout in the morning blocked login to company Google services until it was reset with Colin John's help.

## Next Steps
- Release a new super-bmad version and share the release notes with #project-surf-build.
- Confirm the Story 2.38 fix is deployed to DEV and that Mia's Assign to Yourself retry succeeds.
- Submit the Greenhouse scorecard for the Technical Interview if it is still pending.
- Follow up on the Sentry backoffice alert and the PR #5674 agent issues.

## Transcript Source (Cleaned)
I started the morning on the REC-2026-0064 Admin Review issue. I retested the claim on DEV and posted an update in #project-surf-build: my first attempt returned 403 because I wasn't in ETW Admin Reviewers, but after I joined, the claim returned 200 and assigned the review to me, so I returned it to the pool. I couldn't tie Mia's earlier 503 to the Temporal worker rollout, so that cause is still open and I asked her to retry with a request ID. I also told Dipak I had deployed the last fix.

My Google password got locked, so I couldn't log in normally. I told Marnix I would join the interview with my personal account, and Colin John helped me reset the password. From 10:00 to 11:15 I ran the technical interview with Marnix for Sowmiyaa Chakravarthy Vasan for the Senior Applied AI Engineer role, followed by a quick debrief with Marnix. Later, Samiha, Samuel, Marnix and I held the formal debrief for the role.

Around midday I asked Mia or Ryan to debug the reviewer issue with me. We found that the backend was filtering out valid staff accounts that still carried the old citizen role, which hid Mia from Another Reviewer and could reject Assign to Yourself with a 403. I removed the legacy-role check, explained the fix in the thread with a link to Story 2.38, and later asked Mia to test it again. I skipped the Project Surf stand-up to focus on bug fixes and platform optimization, posted the QA tasks, and said I'd release a new super-bmad version with release notes later today.

I hosted my Progress Check-In with Samuel, Justin and Ankit. I asked Dipak how to test the Pulumi changes on DEV before merging and what compliance waiting period applies before upgrading library versions. I also shared PR #5674 with Simone because the agent behaved badly there, and I took on a Sentry alert in the backoffice alerts channel.
