---
date: "2026-10-08"
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
  - super-bmad
  - staging
  - openfga
  - architecture
  - ai-models
  - figma
  - hiring
---

# Daily Summary — Thursday, October 8, 2026

## Summary

A full day on Project Surf: Douglas walked Shrey Kumar through Surf and SuperBMAD, updated and re-seeded the staging environment for the Product Team, worked out the rule-definition UI in #project-surf-build, and discussed the OpenFGA and production-cell architecture with Samuel Couture Brochu. The afternoon included 1:1s with Ryan Huang and Samuel Couture Brochu and a technical interview for the Senior Software Developer, Applied AI role.

- Attended "Douglas <> Shrey - Surf + SuperBMAD walkthrough" with Shrey Kumar (organizer), 11:45 AM–12:30 PM EDT (transcript available).
- Invited to "Project Surf Stand-up" (organizer Timothy Meyer), 12:30–1:30 PM EDT (transcript available); RSVP was left unanswered.
- Ran "1:1 Ryan - Douglas" with Ryan Huang (Douglas organized it), 2:30–3:00 PM EDT (transcript available).
- Attended "Douglas <> Sam" with Samuel Couture Brochu (organizer), 3:00–3:30 PM EDT (transcript available).
- Ran a technical interview with WILLIAM VELDHUIS for the Senior Software Developer, Applied AI role, alongside Craig Stickel, 4:00–5:00 PM EDT (transcript not available).
- Attended the CCC "Wellness Session", 2:00–2:30 PM EDT (transcript not available).
- Updated staging in #project-surf-build, warned the Product Team of about 20 minutes of downtime for seeding, then asked Justin Labrash and Timothy Meyer to test it.
- Asked Karan Kapoor, Tasmia Shefa and Timothy Meyer in #project-surf-build whether the AND/OR component exists in Figma, and shared the rule-definition prototype (`/proto-rule-definition-flow.html`, story 78.42).
- Told Samuel Couture Brochu by DM that the agent orchestrator now uses Haiku 5.5 (max effort) instead of Opus (low effort), and that OpenAI and Anthropic costs are being tracked.
- Told Samuel Couture Brochu by DM that dev was stabilized yesterday (about 3 hours of work) so it could be promoted to staging.
- Discussed OpenFGA and the production-cell architecture with Samuel Couture Brochu by DM (see Decisions).
- Clarified to Samuel Couture Brochu that Grafana isn't connected yet and only the AWS dashboards exist.

## Decisions & Rationale

- **Keep a shared OpenFGA for now and split it later**: This was a known, recorded tradeoff. The team starts with one shared instance and gives each cell its own when needed.
- **The production cell gets its own setup and an architecture doc check**: Production differs a lot from dev and staging, so the Arch doc has to be rechecked and revalidated before it's built.
- **Choosing a WorkOS replacement comes before the OpenFGA work**: The replacement may already include authorization that could replace OpenFGA.
- **Orchestrator model changed to Haiku 5.5 (max effort)**: It replaces Opus (low effort) because it costs much less for similar results; it won't be used for reviews because tasks take longer.
- **Rules UI reuses the Activity Groups pattern**: Created rules will use the same expand/collapse behaviour and UI as Activity Groups, since the two are similar.

## Open Loops

No open loops carried in; the last summary is from 2026-04-17, outside the lookback window.

- **AND/OR component in Figma**: Waiting on Karan Kapoor, Tasmia Shefa and Timothy Meyer to say whether it's mapped, or whether Douglas can add it to the package as it is now.
- **Picklist layout example**: Asked the Product Team in #project-surf-build for a simple drawing of the "two picklists max per row" structure.
- **Staging validation**: Waiting on Justin Labrash and Timothy Meyer to test the updated staging before more data is created there.
- **Grafana observability**: Grafana isn't connected yet; only the AWS dashboards are available.
- **Interview scorecard**: The Greenhouse scorecard for WILLIAM VELDHUIS still needs to be submitted.

## Blockers

No blockers identified.

## Next Steps

- Review the #project-surf-discovery thread tomorrow while writing stories for Douglas and Ryan Huang.
- Check whether atoms A-27 and A-35 exist and add them if they're missing.
- Revalidate the Arch doc for the production cell, including whether OpenFGA is shared or per cell.
- Submit the Greenhouse scorecard for the WILLIAM VELDHUIS technical interview.
- Confirm with Shrey Kumar whether tomorrow's meeting is skipped (Douglas offered it).

## Transcript Source (Cleaned)

My day was mostly Project Surf. Late morning I gave Shrey Kumar a walkthrough of Surf and SuperBMAD; Gemini notes were captured. I was also invited to the Project Surf Stand-up run by Timothy Meyer, which has Gemini notes. Over DM I told Shrey he could skip our meeting tomorrow, since I'd thought today was Friday.

Around the stand-up I worked on the rule-definition flow in #project-surf-build. I asked Karan, Mia and Tim whether the AND/OR component is in Figma yet. I shared the prototype (`/proto-rule-definition-flow.html`, story 78.42) and said created rules will reuse the Activity Groups expand/collapse UI. I also noted that atoms A-27 and A-35 may not exist yet and asked for a simple example of the two-picklists-per-row layout. Then I updated staging, warned the Product Team of about 20 minutes of downtime while the seeding scripts ran, and asked Justin and Tim to test before I create anything else there.

With Samuel Couture Brochu I talked about AI models over DM. I switched the orchestrator to Haiku 5.5 at max effort instead of Opus at low effort because it's much cheaper, and I'm tracking OpenAI and Anthropic costs. I also said current models still struggle with UI and UX details even with refined stories. Later we went through the architecture. I had recorded the shared OpenFGA as a deliberate starting point, to be split later. The production cell needs its own setup and a revalidated Arch doc. Picking the WorkOS replacement comes first, because it might cover OpenFGA's job. At the end of the day I confirmed Grafana isn't connected yet and only the AWS dashboards exist.

In the afternoon I had my 1:1 with Ryan Huang and a 1:1 with Sam, both with Gemini notes. I also joined the Wellness Session. I finished the day with a technical interview of WILLIAM VELDHUIS for the Senior Software Developer, Applied AI role, together with Craig Stickel.
