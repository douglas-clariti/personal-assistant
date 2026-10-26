---
date: "2026-10-26"
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
  - platform-ops
  - temporal
  - qa
  - design-system
  - onboarding
  - github
---

# Daily Summary — Monday, 2026-10-26

## Summary
- Posted a Platform update in #project-surf-build announcing the Temporal console (dev/staging), EKS Metrics Server, sharded ~5-min PR checks, a single deploy pipeline for develop/main, and Slack deploy-alert improvements.
- Shipped fixes for intermittent 502s on Project Surf and asked Timothy Meyer in #project-surf-build to confirm whether things improved.
- Handed story 78.50 to Timothy Meyer for QA; it failed QA because published Activity Groups added to a workflow raise missing-Rule errors (and a Loop with no Steps can be published).
- Attended Project Surf Stand-up organized by Timothy Meyer (transcript available).
- Ran the Progress Check-In with Sam, Justin Labrash, and Ankit Mittal (transcript not available) and had the Douglas <> Sam 1:1 (transcript available).
- Held the Douglas / Karan DS Sync after missing the start, building a plan with Karan Kapoor so the DS component reaches 100% page coverage for the sales demo, using the "Surf DS - Component Tracker" sheet (transcript available).
- Met Aseem Gupta on QA Strategy (transcript available).
- Commented on Ankit Mittal's migration thread in #project-surf-build about whether the CI pipeline safely handles migrations while the old API is still running.
- Pointed Marnix Faes to the AWS infrastructure reference architecture docs in project-surf, noting it is the initial version and will change a lot after GA.
- Sent clariti-labs GitHub org invites to sree.nimmagadda and sumanth.meela at Marnix Faes's request so they can work on the civcheck branch in Surf.
- Welcomed new hire William Veldhuis in a group DM with Fiona Runa and Sam Couture Brochu.
- Had a short end-of-day Google Meet with Sam Couture Brochu and agreed to follow up first thing tomorrow morning.

## Decisions & Rationale
- **Build a DS component coverage plan with Karan Kapoor**: Ensures every page used in the sales demo has the DS component implemented, tracked in the Surf DS - Component Tracker.
- **Infra reference architecture shared as an initial version**: Expected to change significantly after GA, so it is a starting point rather than a final spec.

## Open Loops
- Story 78.50 failed QA: published Activity Groups (with gate, loop, or conditional inclusion) produce missing-Rule errors in workflows, and empty Loops can be published — needs a fix and re-QA with Timothy Meyer.
- Waiting on Timothy Meyer to confirm whether the 502 fixes improved stability.
- Ankit Mittal's question on whether the pipeline safely handles migrations while the old API is still running.
- EKS Metrics Server issue flagged in the Platform update that still needs fixing.
- Follow-up with Sam Couture Brochu planned for tomorrow morning.

## Blockers
- Story 78.50 cannot pass QA until Activity Groups work inside workflows.

## Next Steps
- Fix 78.50 by testing the front-end authoring flow for Activity Groups with a gate, loop, or conditional inclusion added to a workflow, and block publishing of Loops with no Steps.
- Ping Sam Couture Brochu first thing tomorrow morning.
- Fix the EKS Metrics Server problem on the shared dev/staging cluster.
- Review Karan Kapoor's PR (project-surf #3561) and continue the DS coverage plan.
- Set up weekly check-ins with William Veldhuis and help line up his first assisted story this week.

## Transcript Source (Cleaned)
I started the day by pushing a couple of fixes for the 502 errors we were seeing on Project Surf and asked Timothy to let me know if things improved. Later in the morning I posted a Platform update in #project-surf-build: the Temporal console is live on dev and staging, the EKS Metrics Server is installed (though I noticed a problem with it that I need to fix), PR checks are now sharded to target about five minutes, a single deploy pipeline owns develop and main, and Slack deploy alerts now link to the source PR. I also commented on Ankit's thread about whether migrations could break account writes while the old API is still running.

I marked story 78.50 ready for QA, but Timothy found that published Activity Groups break workflows with missing-Rule errors, and that a Loop with no Steps can still be published. It was working when I deployed and I had tested e2e on dev, but Timothy explained that the e2e only passed because workflows were injected via API, so I need to test the front-end flow directly.

Meetings: Project Surf Stand-up, the Progress Check-In I run with Sam, Justin, and Ankit, my 1:1 with Sam, a DS Sync with Karan where we worked on getting the DS component onto every page for the sales demo using the component tracker, and a QA Strategy session with Aseem.

On Slack I pointed Marnix to the AWS infrastructure reference architecture docs, noting they'll change a lot after GA, and invited Sree and Sumanth to the clariti-labs GitHub org so they can work on the civcheck branch. I welcomed William Veldhuis to the team. At the end of the day I jumped on a quick call with Sam and we agreed to pick it up tomorrow morning.
