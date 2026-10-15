---
date: "2026-10-15"
weekday: "Thursday"
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
  - hiring
  - typecheck
  - playwright
  - infra
  - custom-fields
  - bmad
---

# Daily Summary — Thursday, 2026-10-15

## Summary
- Douglas ran a Technical Interview with Praveen S for the Senior Software Engineer role (Google Meet/Greenhouse) (transcript available).
- Douglas shared his interview assessment with Craig Stickel, Samuel Couture Brochu and the hiring group DM; it praised the candidate's habit of testing AI output and his structured way of working with agents.
- Douglas told Kiran Dhindsa that the technical interview steps match the current process but need a proper pipeline, and asked Sam whether there are other candidates.
- Douglas found that the TypeScript typecheck was freezing laptops at up to 12.4 GB, caused by long `.openapi()` chains and checking all projects at once, and posted the root cause and new harness safeguards in #project-surf-how-we-build.
- Douglas confirmed to Sam in #project-surf-how-we-build that tests run in headless mode and that the rendering flag gave little benefit, since the high memory came from 8 parallel workers.
- Douglas discussed Project Surf production infra with Samuel Couture Brochu (Slack DM): the PRD/Arch stop at staging, and after talking with Dipack, Clariti will control the infra, which makes release management and observability easier.
- Douglas told Timothy Meyer (Slack DM) that tenant custom fields use composite keys (`<domain>.<subdomain>.<field_name>`) that will likely need to change, and asked whether user-created fields need a cap.
- Douglas aligned with Ankit Mittal on updating the bmad-ux skill output to harden the design, and on having bmad-create-story map out the work.
- Douglas hosted the Progress Check-In with Samuel Couture Brochu, Justin LaBrash and Ankit Mittal (transcript available) and was invited to the Project Surf Stand-up (transcript available).
- Douglas told Tasmia Shefa and Shreyansh Kumar to use the dev environment instead of staging, because staging is being used for a POC and PMs review on develop.
- Douglas finished a requested item for Justin LaBrash and asked him to verify it (Slack DM).

## Decisions & Rationale
- **Harness safeguards added for typecheck**: These prevent the runaway memory use (12.4 GB) that froze developer laptops while agents ran checks.
- **Leave custom-field composite keys unchanged for now**: Douglas plans to change them eventually but needs to understand what "Parcel" means in the system first.
- **PMs and devs use the dev environment, not staging**: Staging is occupied by a POC and isn't working as intended.
- **Clariti will own production infra (per Dipack)**: This lets Project Surf work like a normal SaaS, with simpler release management and observability.

## Open Loops
- Whether there are more candidates for the Senior Software Engineer role (asked Samuel Couture Brochu, no answer yet).
- Whether user-created custom fields need a cap (asked Timothy Meyer).
- Justin LaBrash still has to check the item Douglas marked done.
- The Production section of the Project Surf PRD/Arch is outdated: the business model, customer cell creation UI, and how much rollout to automate are still open.

## Blockers
- None identified.

## Next Steps
- Submit the Praveen S scorecard in Greenhouse if not already done.
- Look into what "Parcel" means in the system before redesigning the custom-field keys.
- Update the bmad-ux skill output and run bmad-create-story with Ankit Mittal.
- Revisit the Project Surf production section of the PRD now that Clariti owns the infra.

## Transcript Source (Cleaned)
I started the day in Project Surf threads. I talked with Sam about production: we never got past staging in the PRD, and after talking to Dipack it looks like Clariti will control the infra, which makes release management and observability much easier. I also confirmed with Helen and Craig that we're trying to bring a strong hire onto the team.

Late in the morning I ran a technical interview with Praveen S for the Senior Software Engineer role. That afternoon I shared my assessment with Craig, Sam and the hiring group. He kept bringing up automated testing of AI output, gave solid answers about handling bad data, and has a clear process for working with agents. I asked Sam whether we have other candidates.

On the engineering side, I tracked down why laptops were freezing while agents ran checks. TypeScript typecheck was using up to 12.4 GB because of long `.openapi()` chains and checking every project at once, so I added harness safeguards. I also confirmed the tests run headless, and the high memory came from 8 parallel workers. With Tim I discussed the tenant custom-field schema and asked whether we need a cap on fields. With Ankit I talked about hardening the bmad-ux output and using bmad-create-story. I hosted our Progress Check-In, and at the end of the day I pointed Mia and Shrey to the dev environment, since staging is tied up with a POC.
