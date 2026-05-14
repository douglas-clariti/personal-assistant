---
date: "2026-05-14"
weekday: "Thursday"
author: "douglas-clariti"
quality: "partial"
sources_used:
  - google_calendar
  - slack
sources_empty:
  - gmail
  - google_drive
open_loops_carried: 1
tags:
  - project-surf
  - rust
  - typescript
  - go
  - zapier
  - workflow-engine
  - claude-platform
  - bmad
  - progress-check-in
---

# Daily Summary — Thursday, May 14, 2026

## Summary

- Organized and ran weekly Progress Check-In with Samuel Couture, Justin LaBrash, and Aman Bhalla (optional) via Google Meet, 1:00–1:20 PM EDT (transcript not available).
- Engaged in an extended technical DM discussion with Herman Chan about a potential Rust rewrite of "surf"; shared language selection philosophy — TypeScript for exploratory phases (fast iteration), Rust or Go for well-defined, stable domains — and noted that Rust compile times become a significant bottleneck as a codebase grows under AI-assisted development cycles.
- Initiated a quick Google Meet sync with Justin LaBrash (DM at 11:18 AM EDT); Justin delivered a written analysis concluding Zapier is unsuitable as the workflow engine (cannot model blocked states, SLA clocks, FEEL guards, or cyclic flows) and should only be used as a notification/integration side-car (transcript not available).
- Responded to Colin John regarding the Claude platform spend limit increase request — agreed to defer the increase by one week, to be revisited around May 18.
- Declined the CCC 101 onboarding session (calendar decline) and notified Samiha Nusrat via DM that tight deadlines prevent joining the 3 PM Mental Health Awareness art session.
- Tentatively marked on #clariti-intros Donut (2:30 PM EDT, Irene Plokar organizer); attendance unconfirmed.

## Decisions & Rationale

- **Zapier ruled out as workflow engine**: Justin LaBrash's analysis confirmed Zapier cannot model the state machine primitives required (blocked reasons, actor scopes, SLA clocks with named expiry transitions, FEEL/DMN guards, per-state form configs, cyclic re-entry); it may serve as a notification/integration side-car via webhooks at production time, but never as the engine itself.
- **Claude platform spend limit deferred one week**: Agreed with Colin John (Finance/Ops) to wait one more week before increasing the Anthropic Claude platform spend limit, per his suggestion that the current trigger was non-urgent.
- **Language selection philosophy articulated for surf rewrite discussion**: TypeScript preferred during high-uncertainty/exploratory phases for fast iteration; Rust or Go appropriate once the domain is well-understood and unlikely to change — trade-off framed for Herman Chan as a future reference point.

## Open Loops

- **Expensify access** (carried from 2026-04-17): Requested from accounting@claritisoftware.com to submit Lévis offsite train ticket expenses — no evidence of resolution today; still awaiting response.
- **Rust rewrite evaluation for surf**: Herman Chan raised the idea seriously; Douglas intends to consult with Claude on strategies to mitigate Rust compilation time challenges before any decision is made — outcome pending.
- **Claude platform spend limit increase**: Deferred one week per agreement with Colin John — to be revisited week of May 18.

## Blockers

- Tight deadlines (scope not specified in available data) were cited as the reason for skipping the 3 PM Mental Health Awareness session and may be constraining bandwidth across other work today.

## Next Steps

- Revisit Claude platform spend limit increase with Colin John around week of May 18.
- Consult Claude on Rust compile time mitigation strategies as input to the surf rewrite evaluation with Herman Chan.
- Follow up with accounting@claritisoftware.com on Expensify access (open since 2026-04-17).
- Continue sprint execution work carried from April: super-bmad baseline finalization, architecture spikes, Kanban board setup, and cloud provider RFD review.

## Transcript Source (Cleaned)

The morning began with a DM thread between Douglas and Herman Chan about whether to rewrite "surf" in Rust. Herman proposed it seriously, citing compiler error-catching, good tooling, lower memory footprint, and security surface area as advantages. Douglas engaged with the idea, noting he has personal Rust project experience and had just been reading about Bun's migration from Zig toward Rust. He then articulated the primary trade-off: Rust compile times become increasingly painful as a codebase grows — each test failure under AI-assisted development requires a recompile, and large change sets may force a full dependency graph walk or cache clear. His language selection heuristic: TypeScript for exploratory/uncertain domains (fast feedback loop), Rust or Go for well-understood, stable domains. He flagged wanting to consult Claude on compile-time mitigation strategies. Herman acknowledged compile times as a concern and noted Go as also a strong option. The thread ended without a decision — Herman framed it as a "crazy idea" still worth thinking through.

At 11:18 AM EDT, Douglas pinged Justin LaBrash ("Just do you have a sec?") and they jumped onto a Google Meet. Following the call, Justin posted a detailed written analysis in their DM: Zapier cannot serve as the workflow engine for the project because it lacks the modeling primitives needed — specifically: states with blocked reasons and actor scopes, SLA clocks with named expiry transitions, FEEL expression guards, DMN rule evaluation, per-state form configs, and cyclic state machine flows (monthly compliance re-entry, resubmittal loops). Justin concluded Zapier belongs only as a side-car — triggering Slack notifications or Salesforce updates via the `sendNotification` and `callExternalSystem` stubs — never as the engine itself.

At 12:35 PM EDT, Colin John reached out to say he saw Douglas's Claude platform spend limit request come through the system and suggested waiting one more week before increasing the cap. Douglas agreed with no objection.

At 1:00 PM EDT, Douglas ran the recurring Progress Check-In with Samuel Couture, Justin LaBrash, and Aman Bhalla (optional, attended). No transcript was linked to the event.

In the early afternoon, Samiha Nusrat (CCC organizer) reached out via DM to personally invite Douglas to the 3 PM Wellness Break: Recharge & Create session — a Mental Health Awareness Month art activity. Douglas replied that he is dealing with tight deadlines and likely cannot participate. The calendar event remained marked tentative.
