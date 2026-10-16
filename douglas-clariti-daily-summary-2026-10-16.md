---
date: "2026-10-16"
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
  - workflow-engine
  - configuration-as-code
  - primitives
  - architecture
  - slack
---

# Daily Summary — Friday, October 16, 2026

## Summary

A Friday spent on workflow-engine architecture. In a Slack DM, Douglas explained to Samuel Couture Brochu how the configuration-as-code workflow model works and listed its shared primitive building blocks. Two calendar events were scheduled: the Project Surf Stand-up and a DS Sync with Karan Kapoor, who declined because of being out of office.

- Project Surf Stand-up (organizer Timothy Meyer) was on the calendar via Google Meet, 12:30–1:30 PM EDT; RSVP was not recorded (transcript available — "Notes by Gemini").
- "Douglas / Karan - DS Sync" was scheduled 2:30–3:00 PM EDT, but Karan Kapoor declined (out of office), so it likely did not take place (transcript not available).
- Told Samuel Couture Brochu via Slack DM that the workflow engine already runs versioned, database-stored configuration, and that the UI does not expose it yet because Product asked for it that way.
- Confirmed to Samuel that the UI will generate the configuration file, and that primitives are defined in and pulled from the backend.
- Shared the primitive building-block catalog with Samuel via DM; it lives in the package shared by front-end and back-end and covers state types, flow structures, activity types, triggers, condition sources and form field types.
- Explained to Samuel that every workflow, form, phase, rule and stage-transition condition should be user-built configuration on top of these primitives, with no hard-coded rules.
- Asked Samuel for a concrete example of a requirement that configuration-over-code does not cover.
- Told Samuel he would think the primitives design through more carefully on Monday.

## Decisions & Rationale

- **Primitives-first, configuration-over-code model reaffirmed**: Keep a small set of low-level shared primitives, adding richer ones only when needed, so users can build workflows, forms, phases and rules as configuration instead of hard-coded logic. Users who create their own primitives (e.g. custom Activity types) build on the same blocks.

## Open Loops

No open loops carried (most recent prior summary is 2026-04-17, outside the lookback window).

- **Gaps in configuration-as-code requirements**: Asked Samuel Couture Brochu for an example of what the current model does not cover; waiting for his answer.
- **Karan Kapoor DS Sync**: Karan was out of office, so the session needs to be rescheduled or skipped.

## Blockers

No blockers identified.

## Next Steps

- Monday: think through the primitives design more carefully, as promised to Samuel Couture Brochu.
- Review the Gemini notes from today's Project Surf Stand-up for follow-ups.
- Reconnect with Karan Kapoor on the DS Sync once Karan is back.

## Transcript Source (Cleaned)

My calendar had the Project Surf Stand-up, organized by Timothy Meyer, from 12:30 to 1:30 PM EDT, split into 30 minutes of stand-up and 30 minutes of follow-ups. Gemini meeting notes were attached. My 2:30 PM DS Sync with Karan Kapoor was also on the calendar, but Karan declined because of being out of office.

Late in the morning I had a long Slack DM with Samuel Couture Brochu about the workflow engine. I explained that the workflow is already a configuration file. The engine executes versioned, database-stored configuration, and business workflows are configured from capabilities in the shared engine. The UI doesn't expose this yet because Product asked for it that way, but the UI will generate the configuration file, and the primitives are defined in and pulled from the backend. I asked Samuel for an example of what the model doesn't cover, in case I had missed a requirement.

I then laid out the primitive building blocks that live in the package shared by front-end and back-end:
- State types: Start, Standard, Branch, Fan-out, Terminal
- Flow structures: Step, Activity Group, Parallel Block, Gate, Conditional Inclusion, Loop, Inline Step
- Activity types: Review, Inspection, Task, Document Requirement, Condition Verification
- Triggers: Review, Inspection, Notification, Condition, Hold, Obligation
- Condition sources: Form Input, System, Activity Outcome, Linked Record, Library Value, Spatial
- Form field types, from Text through File Upload

The idea is to keep the primitives very basic, with richer ones only where needed. Everything else, including workflows, forms, phases, rules and stage transitions, is user configuration with no code. I said I would think it through more carefully on Monday.

No Gmail data was gathered because the Gmail connector needs re-authentication. No Google Drive data was gathered because no local sync path is configured.
