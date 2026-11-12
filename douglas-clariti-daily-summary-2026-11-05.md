---
date: "2026-11-05"
weekday: "Thursday"
author: "douglas-clariti"
quality: "partial"
sources_used:
  - google_calendar
  - slack
  - google_drive
sources_empty:
  - gmail
open_loops_carried: 0
tags:
  - project-surf
  - pen-testing
  - staging
  - rpass
  - design-system
  - qa
  - core-beta
  - api-docs
---

# Daily Summary — Thursday, 2026-11-05

## Summary
- Douglas attended the Project Surf Stand-up (Google Meet, organized by Timothy Meyer) (transcript available).
- Douglas hosted the recurring Progress Check-In with Samuel Couture, Justin Labrash and Ankit Mittal (transcript not available).
- Douglas met 1:1 with Marnix Faes in the "Douglas / Marnix" session after scheduling it over Slack for after 1:30pm (transcript available).
- Douglas requested QA from Timothy M. and Thom Oguntoyinbo in #project-surf-build on tickets 80.22, 10.16 and 98.55.
- Douglas told Samuel Couture Brochu that his core-beta items are 80.21, 98.56 and 98.49 (in review) and committed to finishing them all today.
- Douglas shared the new internal API documentation (api.dev.clariticdi.com/docs, behind login) with Samuel Couture Brochu.
- Douglas answered Craig Stickel's pen-test questions: test accounts with real-name fake people were updated, and a "Pen Test Citizen Two" account now exists for multi-tenancy testing.
- Douglas pointed the team in #project-surf-build to the shared staging-admin and staging-implementer RPass accounts for staff/admin testing.
- Douglas made Simone Giacomel a manager on his RPass entry and asked Onildo Aguiar to grant Simone manager access on the staging-admin/staging-implementer accounts.
- Douglas reviewed tabs on task 14.3 with Karan Kapoor, concluded the tabs component is not in the design system, and noted he had already merged with the tabs.
- Douglas reviewed and commented on Ankit M's PR in #pod-superbmad.
- Douglas asked Samuel Couture Brochu to work 5am–10am on Friday to travel for the weekend, offsetting with extra hours on Wednesday and today.

## Decisions & Rationale
- **Second pen-test org deferred**: orgs are split by infrastructure, so a second tenant account can only be set up once Dipak's work delivers staging + the Lakewood cell.
- **Tabs are not a design-system component**: confirmed with Karan Kapoor that the 14.3 prototype tabs aren't developed in the design system, so the merged tab implementation needs follow-up.
- **Remove the native.demo account**: Douglas suggested to Simone Giacomel removing it since it isn't used anywhere.

## Open Loops
- QA pending from Timothy M. / Thom Oguntoyinbo on 80.22, 10.16 and 98.55.
- Waiting on Onildo Aguiar to grant Simone Giacomel manager access to the staging-admin and staging-implementer RPass accounts.
- Waiting on Craig Stickel to verify the updated CDI Pen Test Users.
- Waiting on Samuel Couture Brochu to approve the 5am–10am schedule for Friday.
- Waiting on Thom Oguntoyinbo to confirm 14.3 is on develop.

## Blockers
- Second pen-test org/tenant can't be set up until Dipak Parmar's infrastructure work (staging + Lakewood cell) is complete.

## Next Steps
- Finish core-beta items 80.21, 98.56 and 98.49 (in review).
- Follow up on the 14.3 tabs mismatch with the design system (Karan asked to add it to Douglas's todos).
- Set up the second-org pen-test account once the Lakewood cell is available.
- Remove the native.demo account after confirming with Simone Giacomel.
- Work 5am–10am on Friday, if Samuel approves.

## Transcript Source (Cleaned)
I started the day early, catching up with Simone Giacomel on dates (Slack Oct 25–26, Renovate Oct 30). I thanked Sam for something he sent me to look at, then reviewed and commented on Ankit's PR in #pod-superbmad. In #project-surf-discovery I checked with Thom that 14.3 is on develop, and I posted a QA request to Timothy and Thom for 80.22, 10.16 and 98.55 in #project-surf-build.

After the Project Surf Stand-up, I let Sam know I'd added API documentation for the team at api.dev.clariticdi.com/docs. I asked to work 5am–10am tomorrow so I can travel for the weekend, offsetting with extra hours yesterday and today. I also gave him my core-beta list (80.21, 98.56, 98.49 in review) and said I'd finish them all today. Then I ran my Progress Check-In with Sam, Justin and Ankit.

I met 1:1 with Marnix at 2pm. Around then I went through the 14.3 prototype tabs with Karan. The tabs don't match the design system and aren't built there yet, and I realized I'd already merged with the tabs, so Karan put it on my todos. I pointed the team to the staging-admin and staging-implementer RPass accounts for staff and admin testing. I asked Onildo to make Simone a manager on those accounts, added Simone as a manager on the account I own, and suggested we remove the unused native.demo account.

Last, I answered Craig's pen-test questions. The fake-person test accounts are updated, and "Pen Test Citizen Two" exists for multi-tenancy testing. A second org has to wait for a second tenant, which comes once Dipak finishes the staging + Lakewood cell work. I asked Craig to check the CDI Pen Test Users I updated.
