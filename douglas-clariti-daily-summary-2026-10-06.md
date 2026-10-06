---
date: "2026-10-06"
weekday: "Tuesday"
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
  - ci
  - prototyping
  - o-04-table
  - backoffice
  - super-bmad
  - sprint-9
---

# Daily Summary — Tuesday, 2026-10-06

## Summary
- Attended the **Project Surf Stand-up** (organized by Timothy Meyer, ~15 attendees) on Google Meet (transcript available — Notes by Gemini).
- Ran the **Progress Check-In** as organizer with Samuel Couture Brochu and Justin LaBrash (transcript not available).
- Found that the prototype skill step was having PMs build prototypes directly inside the backoffice app code; separated it into a dedicated prototyping project and announced it in #project-surf-build to Timothy, Justin, Eric, Edwin and Thom.
- Confirmed with Timothy Meyer that Map Compositions and GIS Bindings are real features (Spatial Checks ≈ Layer Sets) before moving prototype files out of the app.
- Fixed the broken CI in #project-surf-build after alerting the dev team (Amrita, Onildo, Craig, Ryan, Shrey, Samuel) that it was being handled.
- Told Samuel Couture Brochu (DM) that CI speed is being improved by splitting tests further and scaling the machine pool, targeting ~5-minute runs.
- Explained to Samuel that the O-04 `DataTable` filter chips were removed in #2917 because they weren't in the design, but per a call with Karan Kapoor they should come back via an updated O-04 table variant (Story 4.11).
- Got Timothy Meyer's approval in #project-surf-build to promote stories 109.7 and 109.9 to Ready for Dev (sprint 9 items already have AC and UX requirements).
- Met with Timothy Meyer (DM + Meet) to discuss a screen being migrated to the new table; resolved merge conflicts on that work and pushed it through CI.
- Committed to Edwin Leong to create a script that populates dev data so the page he's testing is never empty, and asked him to retest.
- Told Samuel that Windows support for Super-bmad is still a feature request, and that bmad-dev-story tests focus on critical flows (login, workflow engine) plus component tests.
- Started fixing a broken image issue with Onildo Aguiar (DM) at end of day.

## Decisions & Rationale
- **Prototypes moved out of the backoffice app into a dedicated prototyping project**: untested, non-functional prototype code was being mixed into production application code, creating a serious risk.
- **O-04 table filter chips to be restored via an updated table variant**: design update received today from Karan Kapoor reversed the earlier removal in #2917.
- **Stories 109.7 and 109.9 promoted to Ready for Dev**: Timothy Meyer confirmed both have AC and UX requirements.
- **Scale CI (more test splitting, larger/more machines) instead of tolerating slow runs**: slow CI forces costly rebases, per Samuel's feedback.

## Open Loops
- Walk the team through the new prototyping project at tomorrow's daily; deploy it to AWS if they approve.
- Samuel to restore the O-04 FilterBar chip row and update Story 4.11 accordingly.
- Edwin to confirm the dev data fix worked or send the page link he needs.
- Broken image issue (with Onildo Aguiar) still in progress.

## Blockers
- None reported today (CI breakage was fixed same day).

## Next Steps
- Demo the prototyping project at the Project Surf daily and decide on AWS deployment.
- Write the dev-data population script for Edwin.
- Continue CI speed-up work toward ~5-minute runs.
- Finish the broken image fix.
- Pick up 109.7 / 109.9 now that they are Ready for Dev.

## Transcript Source (Cleaned)
Today I joined the Project Surf stand-up run by Tim and then hosted our Progress Check-In with Samuel and Justin. Most of my day was in #project-surf-build: I discovered that our prototype step had been telling PMs to build prototypes right inside the backoffice, so half-working prototype code was landing in the real app. After confirming with Tim which screens (Map Compositions, GIS Bindings, Spatial Checks) are real features, I split prototyping into its own dedicated project — it's already wired into the prototype step, and I'll demo it tomorrow and deploy it to AWS if people like it. Tim already confirmed it's working for him.

I also fixed the CI after letting the devs know I was on it, and told Samuel I'm splitting tests further and scaling the CI machines to get runs down to about five minutes. Samuel asked about the O-04 table chips I removed in #2917; I explained they weren't in the design, but Karan updated me today on a call, so they should come back via an updated table variant. I got Tim's go-ahead to promote 109.7 and 109.9 to Ready for Dev, discussed a table-migration screen with him and pushed it after resolving conflicts, and promised Edwin a script to keep dev data populated. I ended the day working with Onildo on a broken image.
