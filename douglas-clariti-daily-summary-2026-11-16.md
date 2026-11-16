---
date: "2026-11-16"
weekday: "Monday"
author: "douglas-clariti"
quality: "partial"
sources_used:
  - google_calendar
  - slack
  - google_drive (Gemini notes via connector)
sources_empty:
  - gmail (connector needs re-authentication)
  - google_drive local sync (local_path not configured)
open_loops_carried: 2
tags:
  - project-surf
  - workos
  - local-dev
  - architecture-docs
  - test-data-seeding
  - design-system
  - conditions-of-approval
  - telemetry
---

# Daily Summary — Monday, 2026-11-16

## Summary
- Attended the Project Surf Stand-up (12:30–13:30 ET, Timothy Meyer) and reported cutting the Surf architecture doc in half, cleaning up the Super BMAD architecture docs, and fixing a local-env password/account issue (transcript available).
- Explained at stand-up that stories must specify design-system component IDs (PR in progress) after Karan Kapoor/Shreyansh Kumar flagged agents building custom page headers, and promised an agent-debugging skill by tomorrow.
- Thom Oguntoyinbo asked Douglas or Dipak Parmar to document test-data seeding in Slack and add a repo skill. Thom also announced he is resigning, and Friday is his last day.
- Asked #team-devops whether to reuse the DEV WorkOS IDs or create a separate "local" WorkOS environment so localhost redirects work for local Project Surf testing. Went with the simplest option that works with dev for now and said he is not blocked if the decision waits for Keycloak.
- Ran the recurring Progress Check-In (13:30–13:50) as organizer with Samuel Couture, Justin LaBrash and Ankit Mittal (transcript not available).
- Interviewed a Senior Software Developer candidate (technical interview) with Craig Stickel from 14:00 to 15:00 (transcript available, Gemini notes).
- Attended the Conditions of Approval Deep-Dive (15:30–16:00, Thom Oguntoyinbo), where Karin Lloyd showed how customers set up conditions in Salesforce. Afterwards he told Onildo Aguiar in DM that "conditions are steps" (transcript not available).
- Offered Tasmia Shefa (Mia) a call in #project-surf-build and held the "Mia / Douglas" session at 16:00–16:15 (transcript not available).
- In #project-surf-how-we-build, said a teammate's issue was a missing-telemetry-files problem, asked them to have their agent push the telemetry files, and said he is working on removing those files from the repo.
- Told Dipak Parmar in DM that he can see the item Dipak shared and will test it today.

## Decisions & Rationale
- **Local WorkOS: simplest option that works with dev for now**: This unblocks local Project Surf testing, and the long-term setup can wait for the Keycloak direction.
- **Telemetry files still pushed to the repo for now**: Douglas is removing them from the repo, but until that lands agents must keep pushing them.
- **Pre-generate epic explains before sprints (team)**: This catches product gaps, like the open EPR questions, before the sprint starts.
- **Repo skill for on-demand test-data seeding via API (team)**: This replaces shared accounts and fills the QA data gaps on the applicant portal.
- **Every design element lives in the shared library, edge cases included (team)**: Then elements can be updated everywhere at once and agents stop building duplicate components.

## Open Loops
- Dipak Parmar to set up the super-bmad AWS account, per PR #4949 (carried from 2026-11-13).
- Karan Kapoor to send his PR for review (carried from 2026-11-13).
- #team-devops to decide the long-term local WorkOS environment (shared DEV IDs vs. a separate "local" env vs. waiting for Keycloak).
- Amrita Patra's tenant-provisioning story 572 is paused until Douglas, Samuel Couture and Dipak Parmar answer her questions.
- Document the test-data seeding steps in Slack and create the seeding skill in the repo (Douglas or Dipak, as Thom asked).

## Blockers
- No blockers today; Douglas said he is not blocked on the WorkOS decision. (Craig Stickel's pentest access issue from 11-13 looks resolved, since Simone Giacomel helped set up the pentest accounts on Friday.)

## Next Steps
- Ship the agent-debugging skill (promised for tomorrow).
- Finish the PR that requires component IDs in stories.
- Answer Amrita's story 572 tenant-provisioning questions.
- Test the item Dipak shared in DM.
- Finish removing the telemetry files from the repo.
- Plan how work is handed over before Thom leaves on Friday.

## Transcript Source (Cleaned)
I started the morning by telling Dipak I could see what he shared and that I'd test it today. Then I posted in #team-devops that I want to test Project Surf locally but need WorkOS to allow localhost redirects. I offered three options: reuse the DEV WorkOS IDs, create a separate "local" WorkOS environment, or something else. Later I said I'd gone with the simplest option that works with what we have in dev and wasn't blocked, and that waiting for Keycloak before deciding was fine too.

At the Project Surf Stand-up I said I'd cleaned up the Surf and Super BMAD architecture docs, cutting the Surf one in half, and was fixing a local environment issue with passwords and accounts. When agents were found building custom components instead of using the library, I explained that stories need to specify component IDs and that a PR to fix this is in progress. I also said I'll have a skill for debugging agent behaviour ready tomorrow. The team agreed to pre-generate epic explains before sprints, to build a repo skill for seeding test data through the API, and to keep every design element in the shared library. Thom asked me or Dipak to document the seeding instructions. Thom also announced he's leaving, with Friday as his last day.

After stand-up I ran our Progress Check-In with Sam, Justin and Ankit. Then Craig and I ran a technical interview for a Senior Software Developer candidate. In the afternoon I joined the Conditions of Approval Deep-Dive, where Karin showed how customers set up conditions in Salesforce. I told Onildo afterwards that conditions are basically steps. I offered Mia a call to walk through what she was doing and we met at 4pm. In #project-surf-how-we-build I said a teammate's issue was missing telemetry files and asked them to have their agent push them. I added that I'm working on taking those files out of the repo.
