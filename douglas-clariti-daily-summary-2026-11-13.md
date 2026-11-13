---
date: "2026-11-13"
weekday: "Friday"
author: "douglas-clariti"
quality: "partial"
sources_used:
  - google_calendar
  - slack
sources_empty:
  - gmail (connector needs re-authentication)
  - google_drive (local_path not configured)
open_loops_carried: 0
tags:
  - project-surf
  - pentest
  - super-bmad
  - aws
  - staging
  - telemetry
  - claude-code
---

# Daily Summary — Friday, 2026-11-13

## Summary
- Invited to the Project Surf Stand-up (12:30–13:30 ET, organized by Timothy Meyer) via Google Meet; RSVP was still pending (transcript available — "Notes by Gemini").
- Asked Dipak Parmar in Slack DM for a separate AWS account to run super-bmad servers, kept apart from Surf; recommended the "CDI Internal Dev" option.
- Shared project-surf PR #4949 with Dipak and explained the new account will host a small server to sync super-bmad data, starting with custom telemetry.
- Posted in #surf-compliance asking Simone Giacomel and Dipak Parmar to restore Craig Stickel's staging access for the `pentest@` and `pentest+admin@` accounts, whose RPass passwords no longer worked.
- Clarified in #surf-compliance that pentest accounts must stay enabled, suggesting MFA be left un-set-up so testers get the full experience.
- Handed pen-test account sharing over to Dipak's team in DM after getting three different requests for how to share them, and noted that posting in the channel helps settle the approach.
- Coached Karan Kapoor in DM on opening PRs through the agent using the `pr-open.yml` guideline rather than his own user, and asked for the PR to review.
- Discussed AI tooling with Onildo Aguiar in DM (Claude running slow, switched to OpenAI for planning; usually Opus for planning and "sol" for implementation), and confirmed dev, not staging, is the target environment.

## Decisions & Rationale
- **Separate AWS account for super-bmad**: Keeps super-bmad servers isolated from Surf infrastructure; "CDI Internal Dev" proposed as the best option.
- **Pentest accounts stay enabled with MFA left un-set-up**: Accounts must be usable for pentesting, and incomplete MFA gives testers the full onboarding experience.
- **Pen-test account sharing handed to Dipak's team**: Three conflicting requests came in, so ownership moved to the infra/compliance side and the discussion moved to the channel.
- **Dev is the target environment (not staging)**: Communicated to Onildo Aguiar.

## Open Loops
- Dipak Parmar to set up the super-bmad AWS account (confirmation of account type/app details was provided via PR #4949).
- Simone Giacomel / Dipak Parmar to confirm current pentest account credentials and restore Craig Stickel's staging access.
- Karan Kapoor to send the PR for review.

## Blockers
- Craig Stickel blocked from staging pentest accounts until credentials are confirmed.

## Next Steps
- Follow up with Dipak on AWS account provisioning and begin testing the super-bmad telemetry sync server.
- Review Karan Kapoor's PR once shared.
- Confirm Craig regains pentest account access on staging.
- Review the Gemini notes from the Project Surf Stand-up.

## Transcript Source (Cleaned)
Today I had the Project Surf Stand-up on the calendar from 12:30 to 1:30, which has Gemini meeting notes attached. Earlier in the morning I asked Dipak for a separate AWS account to run super-bmad servers, separate from Surf, and said CDI Internal Dev seemed like the best option. Later I sent him PR #4949 in project-surf and explained it's a small server to sync super-bmad info, starting with our custom telemetry, with more to move once tested.

Around midday I posted in #surf-compliance asking Simone and Dipak to help Craig Stickel get into staging with the pentest and pentest+admin accounts, since the RPass passwords no longer worked after the new environment was set up. When asked whether pentest accounts should be left un-set-up or disabled, I clarified they need to stay enabled, probably with MFA setup incomplete. In DM I told Dipak I'd received three different requests on how to share the pen-test accounts, so I was handing it to his team and had posted in the channel to settle the approach.

In the afternoon I helped Karan Kapoor with opening PRs through the agent using the pr-open.yml guideline instead of his own user, and asked him for the PR so I could check it. I also chatted with Onildo about Claude being slow, switching to OpenAI for planning, and my usual setup of Opus for planning and "sol" for implementation, and told him dev is our target, not staging.
