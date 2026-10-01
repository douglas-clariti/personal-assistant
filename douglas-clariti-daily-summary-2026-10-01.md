---
date: "2026-10-01"
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
  - t3-code
  - superbmad
  - ai-models
  - workflow-library
  - aws-infra
  - devops
---

# Daily Summary — 2026-10-01 (Thursday)

## Summary
- Douglas organized and ran the "T3 Code - All in ONE" session (13:00–13:30) for the Project Surf devs, sharing the Meet link in #project-surf-build and DMs (transcript available).
- The recurring Project Surf Stand-up (12:30–13:30, organized by Timothy Meyer) was on the calendar (transcript available).
- Douglas ran the Progress Check-In with Samuel Couture and Justin Labrash (13:30–13:50) (transcript not available).
- Douglas ran the 1:1 with Ryan Huang (14:00–14:30) (transcript available).
- In #project-surf-build, Douglas told Samuel, Amrita, Onildo and Craig that `--remote-control` doesn't work with T3 Code, and pointed them to T3 Code's connected-machine chat access instead.
- In #project-superbmad, Douglas advised Timothy Meyer and the team on model choice: Sol 6.1 (Medium/XHigh) over Opus 5.5 low as the main driver, and Luna for agent-driven tests to keep costs down.
- Douglas committed to adding the Luna/Sol testing instructions (Luna for Chrome calls and screenshot validation, Sol 6.1 for reviewing results against acceptance criteria) into the shared skill.
- Douglas took ownership of Justin Labrash's Workflow Library editor bug, where the step form snaps back to Activity Group Name (also reproduces on Develop, per Timothy).
- For Dipak Parmar's request about the CDI repo count for security-scanning costs, Douglas added Dipak and Colin John to the repo's DevOps team on GitHub.
- Douglas sent Thom Oguntoyinbo the Surf infra posture: staging backups 7d / prod planned 35d, Multi-AZ planned for prod, regions us-east-2 and ca-central-1, no TLS 1.3 (ELBSecurityPolicy-2016-08), and no EKS disk encryption.
- Douglas asked Timothy Meyer to beta-test and discuss the Workflow tooling.

## Decisions & Rationale
- **Use Luna for agent-driven tests, Sol 6.1/Opus as the main driver**: running tests on other models is too expensive, and Opus 5.5 low gives weak output.
- **Steer teammates to T3 Code's connected-machine chat instead of `--remote-control`**: remote-control isn't supported with T3 Code yet.
- **Grant Dipak Parmar and Colin John DevOps team access on the repo**: lets them get the repo count for security tooling costs themselves.

## Open Loops
- Workflow Library editor form snap-back bug (staging and Develop): Douglas said he'd take a look.
- Add the Luna/Sol testing instructions to the shared skill for the superbmad team.
- Prod second-region backup copy: the region hasn't been decided.
- Thom's team may raise stories for infra changes; Douglas offered to implement them.
- Timothy Meyer's beta-test session for Workflow: waiting on Timothy's availability.

## Blockers
- None reported.

## Next Steps
- Investigate and fix the Workflow Library step-edit form bug.
- Update the skill with the Luna (tests) / Sol 6.1 (review) instructions.
- Look into the model-behaviour thread in #project-superbmad (Douglas and Onildo are both on Opus 5.5).
- Follow up on infra gaps (TLS 1.3 policy, EKS volume encryption, second-region backups) once stories are created.

## Transcript Source (Cleaned)
Today I ran the T3 Code "All in ONE" session for the Project Surf devs and shared the Meet link in #project-surf-build. Afterwards I had to correct myself: `--remote-control` doesn't work with T3 Code yet, so I pointed people to the connected-machine chat access I'd demoed. I also had the Progress Check-In with Samuel and Justin and my 1:1 with Ryan. The Surf stand-up was on the calendar too.

In #project-superbmad I spent the morning on model choices with Timothy and the team. Sol 6.1 XHigh or Medium beats Opus 5.5 low as a main driver. For agent-driven testing everyone should use Luna, because tests on other models are expensive. I said I'd put those instructions into the skill: Luna for Chrome calls and screenshot validation, Sol 6.1 for reviewing results against acceptance criteria. I also asked Tim to beta-test the Workflow tooling with me.

On Surf, I picked up Justin's Workflow Library editor bug, where the step form snaps back to the Activity Group Name. I added Dipak and Colin to the repo's DevOps team for the security-scanning repo count. I also sent Thom a rundown of our infra posture: backups, Multi-AZ, regions, TLS policy and EKS encryption. I offered to implement any changes they put into stories.
