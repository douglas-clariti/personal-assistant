---
date: "2026-05-28"
weekday: "Thursday"
author: "douglas-clariti"
quality: "complete"
sources_used:
  - google_calendar
  - slack
  - google_drive
sources_empty:
  - gmail
open_loops_carried: 1
tags:
  - project-surf
  - telemetry
  - opentelemetry
  - kubernetes
  - docker
  - clariti
  - townhall
  - demo-env
  - collector
---

# Daily Summary — Thursday, May 28, 2026

## Summary

Heavy collaboration day with Justin LaBrash spanning telemetry troubleshooting, a team Progress Check-In, and the mandatory Clariti Quarterly Townhall. Key outcomes: OpenTelemetry collector setup unblocked, dedicated demo environment strategy decided, demo pre-recording format adopted, and collector memory concerns documented for future improvement. No emails sent today.

- Attended Douglas / Justin Daily 1-on-1 with Justin LaBrash (organizer), 9:30–9:45 AM EDT (transcript not available).
- Troubleshot OpenTelemetry collector setup with Justin LaBrash via DM — identified that `opentelemetry-collector-contrib` is not available via Homebrew and must be installed via the repo bash script (`_bmad/telemetry/launchctl/install-collector.sh`).
- Flagged via DM that `.envrc` must be committed to project-surf main branch for git worktrees to function; shared PR #144 with updated telemetry/direnv configuration.
- Moved team daily standup to 2:00 PM in #project-surf-how-track — confirmed first open slot available for all attendees.
- Attended mandatory Clariti Quarterly Townhall (12:00–1:30 PM EDT) — company-wide mid-quarter update (transcript not available).
- Organized and led Progress Check-In with Samuel Couture, Justin LaBrash, and Aman Bhalla, 2:00 PM EDT — covered DevOps/cell architecture progress, telemetry going live, design restructuring, and demo planning (transcript available).
- Confirmed in post-check-in sessions that telemetry instrumentation is live for token usage, cost, and shot clock metrics; flagged zero token count issue for investigation.
- Discussed staging/dev workflow: auto-deploy on merge to staging, local dev via `dev.local` requires Docker; agreed to fix public URL and restrict access to specific IPs.
- Identified collector script memory consumption (reaching 80% RAM on local machine) as a future technical improvement; agreed to document optimization suggestions for Justin to integrate.

## Decisions & Rationale

- **Dedicated demo environment selected**: Team will promote specific branches to a dedicated demo env to enable independent testing and verification without disrupting the current staging environment.
- **Pre-recorded demo format adopted**: Demo will be pre-recorded to allow async sharing and accommodate stakeholders who cannot attend the live session.
- **Collector refactoring deferred**: Team agreed to maintain the existing persistent collector process for now; Douglas to document performance concerns as a lower-priority future improvement for Justin to integrate.
- **Telemetry server operation maintained**: Transition to a one-shot script deferred; current telemetry server stays active while Justin develops the one-shot alternative.
- **Daily standup moved to 2:00 PM EDT**: Rescheduled by Douglas in #project-surf-how-track as 2:00 PM was the first open slot for all team members.

## Open Loops

- **Expensify access** (carried from 2026-04-17): Requested from accounting@claritisoftware.com — awaiting response before train ticket expenses from Lévis offsite can be submitted. *(stale — consider closing or escalating — open since 2026-04-17, no progress captured in any subsequent summaries)*
- **Zero token count in telemetry**: Token data returning zero through chat interface — cause unknown; Douglas to ask in the project channel why tokens are not being captured.
- **Public URL fix pending**: Douglas to correct the staging/demo web address and restrict environment visibility to specific IP addresses (action item from Progress Check-In).

## Blockers

- Zero token count in telemetry output — cause unconfirmed, needs investigation before telemetry data can be trusted.
- Collector persistent server consuming ~80% local RAM — currently deferred as a future improvement, not actively blocking but noted as a constraint.

## Next Steps

- Douglas: Fix public URL for staging/demo environment and restrict visibility to specific IP addresses.
- Douglas: Document collector script performance issues and optimization suggestions for Justin to integrate.
- Douglas: Deploy application changes to make the cluster publicly accessible and fully operational.
- Douglas: Investigate and ask in team channel why token data returns zero in telemetry.
- Justin: Install Docker and configure local development environment.
- Justin: Share telemetry GitHub repository link in Slack so Douglas can begin plugin setup.
- Justin: Build interfaces for sandbox-to-production promotion and authentication flows.
- Justin: Pre-record the product demo; review presentation slides with the team before recording.
- Justin: Share updated folder structure with Tim and team.
- Justin: Coordinate co-creation session with architecture and PRD teams for accurate time estimates.
- Justin: Develop one-shot telemetry collection script as a future improvement (lower-priority).

## Transcript Source (Cleaned)

The day began with Douglas / Justin Daily 1-on-1 at 9:30 AM EDT (organizer: Justin LaBrash), a 15-minute recurring sync. Immediately after, Douglas and Justin exchanged messages in their DM to work through the OpenTelemetry telemetry collector setup on project-surf. Douglas discovered that `brew install opentelemetry-collector-contrib` fails because no such Homebrew formula exists (only `opentelemetry-cpp`, which is a different project). He identified that Claude had previously installed the collector via a bash script from the project repo itself (`_bmad/telemetry/launchctl/install-collector.sh`). Douglas also flagged that the `.envrc` file required for `direnv allow` was missing from the project-surf main branch and would need to be committed for git worktrees to work. He shared the link to PR #144 with his updates and Justin confirmed the fix.

In #project-surf-how-track, Douglas posted that he had moved the team daily standup to 2:00 PM EDT, noting it was the first open slot for all participants.

At noon, Douglas attended the mandatory Clariti Quarterly Townhall (12:00–1:30 PM EDT), a company-wide mid-quarter update organized by hr@claritisoftware.com with the full employee distribution list.

At 2:00 PM EDT, Douglas organized and led a Progress Check-In with Samuel Couture Brochu, Justin LaBrash, and Aman Bhalla (optional). The meeting covered: (1) DevOps and cell architecture — Douglas reported completing the final epic using Poly for sales architecture, enabling cell-within-cell sandboxes triggered by Temporal workers, with deployment pipelines active in the Kubernetes cluster; (2) telemetry going live — Justin confirmed token usage, input/output metrics, cost, and shot clock tracking are instrumented, though initial install had some issues; (3) design work — Justin discussed restructuring the "what" track folder structure and exploring Figma for vendor-agnostic handoffs; (4) demo planning — team decided on a dedicated demo environment for branch promotion and a pre-recorded demo format. Gemini meeting notes were auto-generated for this session.

Two post-check-in sub-sessions continued in Google Meet. In the first (14:14 EDT), Douglas and Justin reviewed the OpenTelemetry configuration in detail, encountered a `packer.yaml` not-found error during script execution, confirmed zero token count output, and discussed why a persistent server is necessary (Claude does not retain per-call cost data). Douglas proposed a one-shot script alternative to reduce memory overhead; team agreed to defer that change. In the second session (14:33 EDT), they discussed development workflows — Justin needing visual verification via staging/local environments before signing off, Douglas explaining the staging auto-deploy and `dev.local` URL requiring Docker. They agreed to fix the public URL and restrict access to specific IPs. Douglas raised the collector's 80% RAM usage as a concern and proposed a one-shot architecture; Justin clarified the persistent requirement for intermediate data capture. They agreed Douglas will document the performance concerns and Justin will integrate them as a future improvement.
