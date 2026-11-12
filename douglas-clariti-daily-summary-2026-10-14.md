---
date: "2026-10-14"
weekday: "Wednesday"
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
  - workflow-engine
  - ci
  - turbo
  - oxlint
  - staging
  - super-bmad
  - t3-code
---

# Daily Summary — Wednesday, 2026-10-14

## Summary
- Held 1:1 with Ryan Huang via Google Meet (10:00–10:30) (transcript available).
- Met with Aman Bhalla in "Douglas <> Aman" (11:00–11:15) and shared the super-bmad repo link with Aman in a Slack DM (transcript available).
- Attended the company-wide Quarterly Kick-off hosted by HR (12:00–13:30) (transcript available).
- Ran the Progress Check-In with Samuel Couture, Justin LaBrash and Ankit Mittal (13:30–13:50) (transcript not available).
- Posted the CI/Turbo cleanup recap (Stories 0.48–0.50) in #project-surf-build: PR CI 9% faster, post-merge CI 38% faster, 14%/64% lower CI machine usage per PR/merge, custom lint scanners replaced with Oxlint, and custom CI tiers replaced with Turbo workspace tasks.
- Announced the cascading "Publish + update dependents" feature for Workflow Journeys in #project-surf-build (PR #3253), which drafts, repoints and publishes dependent Activity Groups and Workflows in order.
- Reorganized remaining tasks and posted the list to Timothy Meyer in #project-surf-build: Epic 109 (8 stories), Epic 107 (3) and Epic 78 (3).
- Showed Timothy Meyer workflow progress in a DM, including a test-only fee display component on the Record Page (not merged), and asked Timothy to present the workflow engine to developers on Friday.
- Shared the T3 Code 0.0.46 nightly highlights in #project-surf-how-we-build (visual replies, multi-agent delegation, automations, remote browser).
- Proposed in #project-surf-how-we-build that the recurring resource check go into the super-bmad CLI and orchestrator rather than agent.md, after fixing the root cause of the memory usage first, and encouraged Shrey to build the check.
- Offered to optimize the memory-heavy tasks Onildo Aguiar hit, possibly linked to the recent lint/CI changes, and merged a lint-related update for Onildo.
- Told Justin LaBrash to test a flow up to story dev to validate changes that don't touch /sbmad-change or the orchestrator.
- Raised a concern with Samuel Couture that leaning on December (with people moving days off there) puts January deadlines at risk; reported no bugs found so far in feature testing.
- Committed to refreshing staging with the latest changes and resetting the data (in #project-surf-build and to Dipak Parmar).
- Agreed to take on stories Craig Stickel asked for help with and asked Craig for the story numbers.

## Decisions & Rationale
- **Replace custom CI tiers and lint scanners with native Turbo tasks and Oxlint**: faster CI, less compute, and less custom tooling to maintain.
- **Add a cascading publish option for Workflow Journeys**: avoids testing stale versions when an Application Definition changes but its dependent Activity Groups and Workflows don't.
- **Fix the root cause of high resource usage before adding an agent check**: running the check on every task would add cost; if one is added later, it goes in the super-bmad CLI and orchestrator, not agent.md.
- **Timothy Meyer to lead the product side of Friday's workflow engine presentation**: Timothy covers the concepts and Douglas answers technical questions.

## Open Loops
- Waiting on Timothy Meyer to confirm they will present the workflow engine to developers on Friday.
- Waiting on Craig Stickel to send the numbers of the stories to help with.
- Story 51.3 is not developed yet; QA status on the tasks still needs fixing (some "mostly backend" stories missed QA status).
- Test-only fee component on the Record Page is unmerged; decide whether to remove it once the new Record Page lands.
- January deadline risk from work being pushed into December, raised with Samuel Couture.
- Shrey to investigate the resource-check idea; Onildo Aguiar to share which tasks used the most memory.

## Blockers
- None reported.

## Next Steps
- Refresh staging with the latest changes and reset the data.
- Fix QA status across the reorganized Epic 109/107/78 stories.
- Pick up Craig Stickel's stories once the numbers arrive.
- Prepare the workflow engine presentation for Friday with Timothy Meyer.
- Look into the memory/resource usage root cause with Onildo Aguiar and Shrey.

## Transcript Source (Cleaned)
I started the day with my 1:1 with Ryan, then met with Aman and sent him the super-bmad repo. I attended the Quarterly Kick-off and then ran our Progress Check-In with Sam, Justin and Ankit.

On the engineering side, I wrapped up the CI/Turbo cleanup for Stories 0.48 to 0.50 and shared the results with the dev team: PR CI is 9% faster, post-merge CI is 38% faster, and we use much less compute. We now run native Turbo workspace tasks and Oxlint instead of our custom tiers and roughly 20 lint scanners. I also announced the new cascading publish for Workflow Journeys (PR #3253), so changing an Application Definition can update and publish every dependent Activity Group and Workflow in order.

I reorganized my tasks across Epics 109, 107 and 78 and posted the list for Tim. In our DM I showed Tim the workflow progress and a test-only fee component, and I asked Tim to present the workflow engine to the developers on Friday while I handle the technical questions. In #project-surf-how-we-build I shared the T3 Code nightly highlights and argued that we should fix the resource-usage root cause before adding an agent check, which would belong in the super-bmad CLI and orchestrator. I offered to help Onildo with the memory issues and merged a lint update for him.

I told Sam I'm worried that we're relying too much on December and that it puts January deadlines at risk. I promised to refresh staging and reset the data, gave Justin testing guidance, and asked Craig for the numbers of the stories I'm helping with.
