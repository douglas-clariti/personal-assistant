---
date: "2026-11-12"
weekday: "Thursday"
author: "douglas-clariti"
quality: "partial"
sources_used:
  - google_calendar
  - slack
sources_empty:
  - gmail
  - google_drive
open_loops_carried: 1
tags:
  - project-surf
  - super-bmad
  - design-system
  - ci-pipeline
  - devops
  - figma
  - sbmad
---

# Daily Summary — Thursday, November 12, 2026

## Summary

A busy day on Project Surf: Douglas worked through design-system gaps for the applicant portal with the design team, looked at CI speed and cost options with Samuel Couture, joined DevOps for super-bmad CI work, and helped Amrita Patra fix an issue live. In the afternoon there were three meetings: the Project Surf stand-up, an SBMAD discussion and the Progress Check-In. Gmail could not be checked because the connector needs re-authentication, and no local Google Drive path is configured.

- Attended the "Project Surf Stand-up" (organizer Timothy Meyer, 12:30–1:30 PM EST, ~17 accepted) on Google Meet (transcript available — Notes by Gemini).
- Attended "SBMAD Discussion" (organizer Ankit Mittal, with Samuel Couture and William Veldhuis, 1:30–2:00 PM EST): current SBMAD initiatives, a change-tracking plan (Kanban or a list in the sbmad repo) and the release strategy (transcript available — Notes by Gemini).
- Held the recurring "Progress Check-In" as organizer with Samuel Couture, Justin Labrash and Ankit Mittal, 1:30–1:50 PM EST, overlapping the SBMAD Discussion (transcript available — Notes by Gemini).
- In #project-surf-build, flagged to Tasmia Shefa and Karan Kapoor that the Figma "Action requirement Bento" wasn't covered by the O-11 Bento and asked for access to the External Applicant Portal Figma file; Karan made it a new O-13 organism (merged in PR #4868), so Story 98.81 is now ready for Douglas.
- In #project-surf-build, asked Tasmia Shefa to keep QA fix requests within the current story's scope, since the tooltip was added on purpose for testing and a later story removes it.
- In #project-surf-build, told Timothy Meyer and Dipak Parmar he was working on the PM story-creation change, and asked Timothy to merge/rebase from `develop` and retest.
- In #team-devops, announced he had joined the DevOps group (agreed with Samuel Couture) so he can update super-bmad CI checks; infra changes will still be reviewed by Simone Giacomel or Dipak Parmar, and Dipak agreed.
- In a DM with Samuel Couture, reviewed CI performance (about 14 min average total across nine runs, about 10 min of test execution, 22 min at the 90th percentile, 3.4 min of waiting), said the tests need cleaning up, and suggested trying blacksmith.sh (about 20–50% cheaper and faster); also asked why a merge got past CODEOWNERS.
- In #project-surf-how-we-build, pointed Shreyansh Kumar to `/sbmad-pr-goal` (built on `/goal`) for watching PRs and auto-fixing CI, in reply to a proposed `/sbmad-watch-pr` skill.
- In #project-surf-precheck, supported multiple migration streams, with each cell applying the migrations for its own products.
- Told Dipak Parmar the session with Timothy Meyer will cover the Operator console UI shell (stories 57.2 and 57.10).
- Joined a Google Meet huddle with Amrita Patra and Colin John that resolved Amrita's issue (headroom was the cause).

## Decisions & Rationale

- **Douglas joined the DevOps group**: he needs to update super-bmad CI checks himself; infra changes still go to Simone Giacomel or Dipak Parmar for review.
- **The applicant-portal "Action Required" bento becomes a new O-13 organism, not part of O-11**: Karan Kapoor's call, because it is a new component that isn't in the design system yet. Specs merged in PR #4868.
- **Keep QA fixes within the current story's scope**: temporary testing aids like the tooltip will be removed by upcoming stories.
- **Use the existing `/sbmad-pr-goal` instead of a new `/sbmad-watch-pr` skill**: it already watches PRs against the default goals.
- **Migrations: multiple streams, one per cell**: each cell applies the migrations for the products it runs.

## Open Loops

- **Unmerged PRs**: Douglas mentioned "a couple of PRs that were never merged" to Dipak Parmar (carried from 2026-11-11).
- **Timothy Meyer to rebase and retest**: Timothy was asked to merge/rebase from `develop` and test again; he replied "I'll get to this eventually."
- **No data field for blocking fees in Story 98.81**: nothing in the data says which fees block a review; Karan Kapoor asked not to invent a field and to flag it if it blocks.
- **CODEOWNERS bypass**: Douglas and Samuel Couture need to find out why GitHub allowed a merge despite CODEOWNERS.
- **Blacksmith.sh evaluation**: Douglas asked Samuel Couture how they could test blacksmith.sh as a CI runner.
- **Unanswered invite**: Douglas has not responded to "Project Surf – End of Sprint Demo/Check-in" (4:00–4:30 PM EST).

## Blockers

No active blockers. The shared DEV tenant was replaced today (Dipak Parmar), so shared logins no longer work and each person must use their own account.

## Next Steps

- Pick up Story 98.81 (O-13 Action Required: fee emphasis only when blocking, plus the Summary variant).
- Finish story 25.21 and the PM story-creation change.
- Look into the CODEOWNERS bypass and plan a blacksmith.sh trial and test clean-up with Samuel Couture.
- Prepare the Operator console UI shell session with Timothy Meyer (stories 57.2 and 57.10).
- Check the Gemini notes for the SBMAD Discussion and stand-up for action items.
- Follow up on the outstanding unmerged PRs.

## Transcript Source (Cleaned)

I spent the morning in a DM with Samuel Couture on our CI pipeline. Across nine recent runs it averages about 14 minutes total and around 10 minutes of actual test execution, but the 90th percentile hits 22 minutes and the 3.4-minute wait is bad. We need to clean up the tests, and I suggested trying blacksmith.sh, which T3 code uses and which looks 20–50% cheaper and faster. Later we noticed GitHub allowed a merge despite CODEOWNERS, which we need to look into. After talking with Samuel, I added myself to the DevOps group so I can update super-bmad CI checks, and I posted in #team-devops that Simone and Dipak will still review anything infra-related. Dipak agreed.

In #project-surf-build I told Timothy and Dipak I was working on the PM story-creation change, since PMs are the ones creating stories, and asked Timothy to rebase from develop and retest. I asked Mia (Tasmia Shefa) to keep her QA fixes within the current story, because the tooltip was only there to help testing. I also flagged that the Action Required bento in the External Applicant Portal Figma wasn't covered by O-11 and asked Mia and Karan for access. Karan decided it should be a new organism, O-13, and paused me for a bit. By the afternoon the specs were merged in PR #4868 and Story 98.81 is ready for me. In #project-surf-precheck I supported running multiple migration streams, one per cell.

From 12:30 I was in the Project Surf stand-up. At 1:30 I had both my Progress Check-In with Samuel, Justin and Ankit and Ankit's SBMAD Discussion about current initiatives, change tracking in the sbmad repo and our release strategy. All three meetings have Gemini notes attached. Afterwards I let Dipak know the session with Timothy will cover the Operator console UI shell (stories 57.2 and 57.10). In #project-surf-how-we-build I pointed Shrey to `/sbmad-pr-goal` for watching PRs. I ended the day on a quick Meet with Amrita and Colin, where we found headroom was causing Amrita's issue and fixed it.
