---
date: "2026-11-06"
weekday: "Friday"
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
  - workos
  - release-80.21
  - sla-alerts
  - deploy
  - ooo
---

# Daily Summary — Friday, 2026-11-06

## Summary
- Douglas confirmed in #project-surf-build that the citizen WorkOS credentials under `surf/dev/cell` belong to the separate Dev environment's `project-surf-portal-web` app, after checking the client ID against AWS.
- Douglas told Thom Oguntoyinbo in #project-surf-build that release 80.21, now in QA, would be available in dev soon.
- Douglas handed off 80.21 dev testing to Thom over DM, saying local tests passed and offering SLA test scripts that seed DB records against Thom's clock rules so Thom can test the alerts.
- Douglas asked Onildo Aguiar over DM to watch the project-surf `app-deploy.yml` GitHub Actions workflow and confirm the deploy, because Douglas was leaving to travel to the US.
- Douglas told Tasmia Shefa over DM that Douglas would handle Tasmia's open request on Monday.
- Douglas blocked 11:00–22:00 as "Busy - OOO" and declined Project Surf Stand-up (transcript available), Enterprise 2026.005 Release Demo (transcript available) and Surf Build - Sprint Planning (transcript not available).

## Decisions & Rationale
- **Thom Oguntoyinbo owns 80.21 dev validation**: Douglas is OOO, and Douglas's local tests plus SLA scripts give enough coverage for Thom to verify.
- **Onildo Aguiar monitors the 80.21 deploy**: Douglas left mid-deploy and needed someone to confirm the `app-deploy.yml` run.

## Open Loops
- Confirmation from Onildo that the project-surf `app-deploy.yml` run for 80.21 succeeded.
- Thom to create clock rules and send links so Douglas can seed SLA test records.
- Tasmia Shefa's request, which Douglas committed to handle on Monday.

## Blockers
- None reported.

## Next Steps
- Monday: handle Tasmia Shefa's request.
- When Thom sends the clock-rule links, seed DB records with elapsed time to trigger the SLA alerts.
- Check the Gemini notes from Surf Build - Sprint Planning and Project Surf Stand-up for anything assigned to Douglas during the OOO block.

## Transcript Source (Cleaned)
This morning I wrapped up Project Surf before going out of office for the rest of the day; I'm travelling to the US. In #project-surf-build I confirmed that the citizen WorkOS credentials under surf/dev/cell are for the separate Dev environment's project-surf-portal-web application, which I checked by matching the client ID against AWS. I also let Thom know that 80.21 is in QA and will reach dev soon.

Since I can't test 80.21 on dev myself, I messaged Thom directly. I told Thom I'd run plenty of tests locally, and that I'd prepared scripts for the SLAs: if Thom creates some clock rules and sends me the links, I can insert records with elapsed time so Thom can test the alerts. I asked Onildo to follow the project-surf app-deploy.yml workflow and make sure the deploy goes through. I told Tasmia I'll take care of Tasmia's item on Monday.

I blocked my calendar as OOO from 11:00 and declined the Project Surf Stand-up, the Enterprise 2026.005 Release Demo and Surf Build Sprint Planning. Gemini notes exist for the stand-up and the demo.
