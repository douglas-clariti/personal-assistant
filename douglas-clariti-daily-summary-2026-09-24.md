---
date: "2026-09-24"
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
  - onlyoffice
  - kubernetes
  - super-bmad
  - workflow-engine
  - ai-models
  - back-office
  - environments
---

# Daily Summary — Thursday, September 24, 2026

## Summary

Brought the OnlyOffice service online on dev after getting the license. Shipped a big Back Office navigation speedup. In Surf Orgs Creation, argued against creating new tenant orgs until the end-to-end workflow works, and the team agreed to hold the current environment structure for 3 weeks. Also set model-usage guidance (Sol vs. Luna vs. Opus) for the team and helped fix super-bmad/opencode issues.

- Asked Craig Stickel (DM) and then #project-surf-build (cc Craig Stickel, Timothy Meyer, Thom Oguntoyinbo) to share the OnlyOffice license via RPass, since the image and node were already deployed.
- Received the OnlyOffice license and confirmed to Craig Stickel in #project-surf-build that `onlyoffice.dev.clariti-surf.com` is up and passing its healthcheck, then validated it with Onildo Aguiar via DM.
- Announced in #project-surf-build that Back Office navigation dropped from ~6s to ~120ms (~50× faster) by reusing the active router's session instead of making repeated session calls, and reminded devs to flag performance regressions early.
- Told Amrita Patra in #project-surf-build that her requested item was done again, and asked a teammate to clear their cache to pick up the fix.
- Attended "Surf Orgs Creation" with Timothy Meyer (organizer), Craig Stickel, Justin LaBrash, Dipak Parmar, Edwin Leong, and Thom Oguntoyinbo, 11:30 AM–12:30 PM EDT, where he pushed back on new tenant orgs until the phase-one workflow is stable (transcript available).
- Attended "Project Surf Stand-up" with Timothy Meyer (organizer) and the Surf team, 12:30–1:30 PM EDT: reported the OnlyOffice license was received, Kubernetes pods were being tested, and stories 7820/7827 were pending code review, and announced travel to Canada on Tuesday (transcript available).
- Hosted "Progress Check-In" with Samuel Couture, Justin LaBrash, and Ankit Mittal, 1:30–1:50 PM EDT (transcript not available).
- Posted a model-selection rule of thumb in #project-surf-how-we-build ("Thinking = Sol, Doing = Luna"), recommended Sol as the default over Opus/Astra for cost reasons, and shared per-million-token pricing for GPT-6 Sol and Opus 5.5.
- Updated super-bmad and told Samuel Couture (DM) that Onildo Aguiar's issue was an opencode bug, not Luna.
- Advised in #project-surf-build that agent-generated stories should be checked for missing dependencies ("Show me the evidence…" prompt for Thom Oguntoyinbo).
- In #project-superbmad, said he will fix super-bmad for OpenAI models being more sensitive to commands, and told the worker it can open PRs manually without proof.

## Decisions & Rationale

- **Keep the current dev/staging environment structure for 3 weeks, with no new tenant orgs (Surf Orgs Creation)**: The end-to-end workflow isn't working yet, and each added environment multiplies debugging time, so workflows get stabilized before other teams come in.
- **Start the workflow engine when a record type is selected (Surf Orgs Creation)**: This lets pre-submission steps be managed. Timothy Meyer will draft the engine-trigger story.
- **Pause staging environment changes for internal PC training for 2–3 weeks (Stand-up)**: Keeps focus on the current build.
- **Group sprints 8–10 by journey, not only by epic (Stand-up)**: Makes QA and testing more effective.
- **Sol is the default model; Luna for clear implementation; Opus/Astra only for hard problems**: Opus 5.5 costs about 2× Sol per token, and BMAD's document-heavy context makes input cost significant.

## Open Loops

No previous summary within the 10-day lookback window, so no open loops were carried forward.

- **Stories 7820 and 7827**: Pending code review.
- **OnlyOffice on Kubernetes**: Service is up on dev; a couple of follow-up tests were still running.
- **Workflow issues discussion**: Timothy Meyer is to talk with Douglas about current workflow issues and possible misinterpretations.
- **Model cost benchmark**: Committed to benchmarking the same story across models to compare prices.
- **super-bmad OpenAI fixes**: Need to adapt prompts and commands for OpenAI model sensitivity.

## Blockers

- The OnlyOffice license blocker from this morning was resolved during the day. No other active blockers were identified.

## Next Steps

- Finish code review and merge for stories 7820 and 7827.
- Complete OnlyOffice tests on dev.
- Update super-bmad for OpenAI model command sensitivity.
- Run the same-story model cost benchmark (Sol vs. Opus 5.5).
- Meet with Timothy Meyer on workflow engine issues. Timothy Meyer and Thom Oguntoyinbo are setting up a workflow logic session next week.
- Travel to Canada on Tuesday; stay online for critical issues.

## Transcript Source (Cleaned)

I started the morning chasing the OnlyOffice license. I had deployed the image and node the night before and asked Craig Stickel over DM, then #project-surf-build, to share it through RPass. Once the license arrived, I confirmed to Craig that the service was up at the dev healthcheck endpoint and checked it together with Onildo Aguiar. In #project-surf-build I also announced that Back Office navigation went from about 6 seconds to about 120 ms by reusing the active router's session, and reminded the devs to watch performance. I confirmed to Amrita Patra that her item was done again.

In Surf Orgs Creation (Timothy Meyer's meeting, Gemini notes linked), I said we aren't ready to spin up tenant orgs for the Permit Center/PC team because the end-to-end workflow isn't working, and that more environments just add debugging hours. Craig Stickel and Dipak Parmar agreed. We kept the current dev/staging structure for 3 weeks and agreed the workflow engine should start at record type selection. At the Project Surf Stand-up (Gemini notes linked), I reported the OnlyOffice license and Kubernetes pod testing, said stories 7820 and 7827 were pending code review, and announced I'm travelling to Canada on Tuesday. The stand-up also agreed to pause staging changes for 2–3 weeks and organize sprints 8–10 by journey. Afterward I hosted the Progress Check-In with Samuel Couture, Justin LaBrash, and Ankit Mittal; no notes were linked.

On AI tooling, I posted a Sol/Luna rule of thumb and a Sol vs. Opus 5.5 pricing comparison in #project-surf-how-we-build, recommended Sol as the cost-effective default, and said I'd benchmark the same story across models. I updated super-bmad and found that Onildo's problem was an opencode bug rather than Luna. Late in the day in #project-superbmad I said I'd fix super-bmad for OpenAI models' command sensitivity.
