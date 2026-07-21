---
date: "2026-07-21"
weekday: "Tuesday"
author: "douglas-clariti"
quality: "complete"
sources_used:
  - google_calendar
  - slack
sources_empty:
  - gmail
  - google_drive
open_loops_carried: 1
tags:
  - project-surf
  - super-bmad
  - claude
  - anthropic
  - api-usage
  - telemetry
  - standup
  - deployment
---

# Daily Summary — Tuesday, July 21, 2026

## Summary

Busy day with four back-to-back meetings (Douglas / Justin Daily, Project Surf Stand-up, Progress Check-In, and Douglas <> Sam) covering sprint progress and API cost management. The dominant Slack theme was tracking per-developer Claude API usage spend for Project Surf: requested dev expense account access from Samuel CB in #pod-superbmad, engaged Colin John to pull daily Claude spend per developer, and coordinated with Justin Labrash on a telemetry-viewing skill in progress. Also announced a prior day's deployment to #project-surf-build.

- Attended **Douglas / Justin Daily** with Justin Labrash (organizer) via Google Meet, 9:30–9:45 AM EDT (transcript available).
- Attended **Project Surf Stand-up** (organizer: Timothy Meyer) via Google Meet, 12:30–1:30 PM EDT, with Edwin Leong, Karan Kapoor, Eric McClelland, Thom Oguntoyinbo, Amrita Patra, Craig Stickel, Onildo Aguiar, and optional attendees Aman Bhalla, Justin Labrash, and Samuel Couture (transcript available).
- Hosted **Progress Check-In** via Google Meet, 1:00–1:20 PM EDT, with Samuel Couture, Justin Labrash, and Aman Bhalla (optional) (transcript available).
- Attended **Douglas <> Sam** with Samuel Couture (organizer) via Google Meet, 2:00–2:30 PM EDT (transcript available).
- Requested dev expense account access for himself and Justin Labrash from Samuel CB in #pod-superbmad to cross-reference Project Surf Claude API usage values against Anthropic's records.
- Asked Colin John (DM) to pull per-developer daily Claude spend for Project Surf; later extended the request to include Amrita Patra and Craig Stickel.
- DM'd Justin Labrash asking about a telemetry-viewing skill Justin was building to inspect Claude API usage values; asked to be notified when complete.
- Notified Timothy Meyer and Onildo Aguiar in #project-surf-build that a deployment/improvement was live.
- Shared the openusage GitHub repo (robinebers/openusage) with a team member via DM as a reference for API usage tracking.

## Decisions & Rationale

- **Per-developer Claude API spend tracking initiated**: Coordinated across Samuel CB, Colin John, and Justin Labrash to establish visibility into how much each Project Surf developer spends on Claude per day — intent is to cross-reference internal values against Anthropic's billing to identify any discrepancies.

## Open Loops

- **Expensify access** (carried from 2026-04-17) (stale — consider closing or escalating): Requested from accounting@claritisoftware.com for train ticket expenses from the Lévis offsite — no resolution recorded since April 17.
- **Per-dev Claude usage data**: Requested from Colin John via DM; awaiting delivery for Project Surf developers including Amrita Patra and Craig Stickel.
- **Dev expense account access**: Requested from Samuel CB in #pod-superbmad for Douglas and Justin Labrash; awaiting approval.
- **Telemetry-viewing skill**: Justin Labrash building a skill to inspect Claude API telemetry values — Douglas asked to be notified when complete.

## Blockers

No blockers identified.

## Next Steps

- Review telemetry skill with Justin Labrash once it is complete.
- Validate per-dev Claude spend data from Colin John against Anthropic values.
- Follow up on dev expense account access (Samuel CB).
- Review Gemini meeting notes from today's four sessions.

## Transcript Source (Cleaned)

The day started with the recurring **Douglas / Justin Daily** (9:30–9:45 AM EDT, organized by Justin Labrash), followed by the broader **Project Surf Stand-up** (12:30–1:30 PM EDT, organized by Timothy Meyer) with the full engineering team including Edwin Leong, Karan Kapoor, Eric McClelland, Thom Oguntoyinbo, Amrita Patra, Craig Stickel, and Onildo Aguiar. Douglas also hosted a **Progress Check-In** (1:00–1:20 PM EDT) with Samuel Couture, Justin Labrash, and Aman Bhalla, and wrapped up with a 1:1 **Douglas <> Sam** (2:00–2:30 PM EDT, organized by Samuel Couture). All four sessions had Gemini Notes attached.

On Slack, the main thread was tracking Claude API spend per developer for Project Surf. Douglas notified Justin Labrash he'd be 10 minutes late to the 9:30 AM meeting. In #pod-superbmad, he asked Samuel CB whether he and Justin could get access to the dev expense account to cross-check internal token usage values against Anthropic's billing data. In parallel, Douglas DM'd Colin John requesting a breakdown of daily Claude spend per developer on Project Surf — later asking to add Amrita Patra and Craig Stickel to the report. He also DM'd Justin Labrash asking about a skill Justin was building to view telemetry data, saying he was eager to see it once ready. In #project-surf-build, Douglas informed Timothy Meyer and Onildo Aguiar that a deployment/improvement (from the previous day) was live and asked them to flag anything that came up. A GitHub link to the robinebers/openusage repo was shared with a team member via DM, likely as a reference for API usage tracking tooling.
