---
date: "2026-10-19"
weekday: "Monday"
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
  - cdi
  - workflow-engine
  - status-update
  - lakewood
  - super-bmad
  - staging-access
---

# Daily Summary — Monday, 2026-10-19

## Summary
- Douglas drafted and refined a Project Surf / CDI status update with Samuel Couture Brochu over Slack DM, condensing it into Highlights (CDI mostly built, ~14 stories/dev/week, Lakewood setup with 118 processes and 62,000+ fee rules) and Challenges (workflow engine at risk for the demo, team capacity).
- Douglas explained to Samuel that the workflow engine is domain-agnostic (states, transitions, rules, building blocks) and can serve Permitting, Planning & Zoning, Code Enforcement and Licensing through configuration, with room to move to a DAG model later.
- Douglas flagged in #project-surf-build and to Samuel that the application-submit steps are still hardcoded outside the workflow, and reminded Timothy Meyer of the agreement to make the application step 1 of the workflow.
- Douglas told Timothy Meyer in #project-surf-build that story 109.3 can only be tested once 109.17 delivers its UI.
- Douglas shared environment access in #project-surf-build, added Shrey to dev with admin-equivalent roles, explained Google SSO vs. the staging-admin account, and asked Onildo Aguiar to grant staging user access.
- Douglas helped Aman Bhalla with a bmad-spec issue by having him reinstall super-bmad 0.3.164 via `npx github:clariti-labs/super-bmad#0.3.164 install`.
- Douglas asked Shrey and Eric M. in #project-surf-build whether a blocked item had been started, and offered to fix it himself.
- Douglas attended Project Surf Stand-up (organized by Timothy Meyer) (transcript available).
- Douglas ran the Progress Check-In with Samuel Couture, Justin Labrash and Ankit Mittal (transcript not available).
- Douglas met Karan Kapoor and Tasmia Shefa in the Douglas / Karan DS Sync (transcript available).
- Douglas hosted the Workflow Engine Walkthrough for the Surf team, including Timothy Meyer, Onildo Aguiar, Amrita Patra, Ryan Huang, Shrey Kumar and Aseem Gupta (transcript not available).

## Decisions & Rationale
- **Status update trimmed to two highlights and two challenges**: The detailed version was too technical for its audience, so Douglas cut it down to the outcomes and key risks.
- **Workflow engine named as the main demo risk**: 23 workflow stories are still open and there are no automated workflow regression tests, so every change has to be tested by hand from application to issuance.
- **Engineering efficiency figures kept in a separate eng-only section**: The cost and build-time numbers (build times halved, 40–60% lower AI costs, ~62% lower test-environment bill) still need revalidating.
- **109.3 testing waits on 109.17**: 109.17 builds the UI that 109.3 needs for testing.
- **Push PRD/product challenges to after GA**: Douglas told Samuel he is moving forward instead of losing time on debates, with a plan to revisit after GA.

## Open Loops
- Samuel Couture Brochu has not yet confirmed the condensed CDI status update ("better?").
- The application-submit flow is still hardcoded; it needs to move into the workflow as step 1 (raised with Timothy Meyer and product).
- Douglas committed to make sure the UI-composes-from-workflow-primitives direction is reflected in the architecture.
- Onildo Aguiar was asked to grant staging user access (Douglas lacks admin).
- Waiting on Shrey / Eric M. to say whether the blocked #project-surf-build item has been started.
- Waiting on Aman Bhalla to confirm whether the super-bmad 0.3.164 reinstall fixed bmad-spec.

## Blockers
- Douglas has no admin rights on staging, so he needs Onildo Aguiar to grant staging user access.
- No automated workflow regression tests exist yet, so the Lakewood end-to-end permit test can't run until the open workflow stories land.

## Next Steps
- Recheck the telemetry and AI/infra cost figures before the eng-only numbers are used.
- Update the architecture docs so the UI composes itself from workflow primitives.
- Follow up with Samuel on a sync about the workflow UI direction and the final status update text.
- Follow up on the Workflow Engine Walkthrough outcomes with the Surf team.
- Review the Gemini notes from Project Surf Stand-up and the DS Sync with Karan.

## Transcript Source (Cleaned)
Today was mostly Project Surf. In the morning I worked with Samuel over DM on the CDI status update. I started with a long, detailed draft covering what we've built, the Lakewood setup, our AI-assisted delivery gains and the challenges, then cut it down to two highlights and two challenges: the workflow engine is at risk for the demo because of the testing time left, and the team is stretched and relies on a few key people. I moved the engineering efficiency numbers into an eng-only section, though I need to recheck telemetry and costs before we use them.

I also explained to Samuel that the workflow engine is only a shell: it runs whatever is configured and knows nothing about permits, and the PRD calls for one engine covering all four domains through configuration. I admitted the application-submit flow is still hardcoded outside the workflow, which I've already raised with product. I made the same point to Tim in #project-surf-build, reminding him we agreed the application should be step 1 of the workflow. Later I told Tim that 109.3 depends on the UI from 109.17.

On access and support, I shared environment access in #project-surf-build, added Shrey to dev with admin roles, explained the Google SSO and staging-admin login options, and asked Onildo to grant staging user access because I don't have admin. I helped Aman fix a bmad-spec problem by reinstalling super-bmad 0.3.164, and asked Shrey and Eric whether a blocked item was already being worked on.

Meetings: I attended Project Surf Stand-up (Gemini notes linked), ran my Progress Check-In with Samuel, Justin and Ankit, had the DS Sync with Karan and Tasmia (Gemini notes linked), and finished the day hosting the Workflow Engine Walkthrough for the Surf team.
