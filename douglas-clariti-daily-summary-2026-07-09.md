---
date: "2026-07-09"
weekday: "Wednesday"
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
  - super-bmad
  - llm-strategy
  - aws-bedrock
  - clariti
  - telemetry
  - ci-cd
  - architecture
---

# Daily Summary — Wednesday, July 9, 2026

## Summary

A dense afternoon of back-to-back meetings covering Project Surf architecture, super-bmad toolchain adoption, orchestrator efficiency strategy, and LLM provider scoping for Legal. Douglas also resolved a teammate's MFA blocker, ran a super-bmad beta test with Thom Oguntoyinbo, and posted team communications across Slack.

- Attended "Douglas / Justin Daily" with Justin LaBrash (organizer) via Google Meet, 9:30–9:45 AM EDT; shared shell alias configuration for super-bmad toolchain with Justin via DM immediately after (transcript available).
- Participated in "#project-surf-build" LLM provider thread (11:16 AM–12:18 PM EDT): proposed three-tier LLM strategy — Anthropic (production), Amazon Bedrock (enterprise/data residency), Fireworks + OpenRouter (future cost/fallback/testing) — and committed to documenting US/Canada hosting validation in the Architecture doc.
- Confirmed Phase 1 GA vendor list with Samuel Couture Brochu: Grafana remains in scope (self-hosted, infra monitoring); WorkOS is removed.
- Resolved Onildo Aguiar's MFA blocker via DM, unblocking PR #537 in project-surf.
- Attended "Project Surf Stand-up" with 12-person team organized by Timothy Meyer, 12:30–1:30 PM EDT; reported CI memory fixes completed and testable user roles implemented; recommended formalizing open architectural decisions as markdown files with trade-offs (transcript available).
- Ran "Progress Check-In" (organizer) with Justin LaBrash and Samuel Couture, 1:00–1:20 PM EDT; aligned team on 50/20/30 workload split (refinement/future planning/validation), committed to updating BMAD to 6.10, and surfaced need for Tim consultation on velocity themes (transcript available).
- Attended optional CEO Office Hours with Cyrus covering H2 strategy and recent Clariti events, 1:30–2:00 PM EDT (transcript available).
- Attended "Douglas <> Sam" 1:1 with Samuel Couture Brochu (organizer), 2:30–3:00 PM EDT; confirmed orchestrator using Fable 5 achieves 96% performance at 46% cost, agreed to add third pod developer, authorized ChatGPT for development overflow, and identified Amarita onboarding as velocity priority (transcript available).
- Ran "Labs: Test new Super-bmad" session (organizer) with Thom Oguntoyinbo, 3:00–3:15 PM EDT; granted Thom access via Enterprise PMs group, diagnosed CI check delays on non-code PR artifacts, recommended worktree flag for agent isolation, and confirmed telemetry integration for cloud sessions (transcript available).
- Posted @here feedback poll in #project-surf-build on super-bmad adoption; received positive responses from Onildo Aguiar, Craig Stickel, and Timothy Meyer.
- Shared /bmad-technical-research skill usage tip in #project-surf-how-we-build to guide team on evidence-based architectural decisions.
- Flagged sbmad-land-pr CI performance issue with Craig Stickel: runtime is 45–60 min, should be max 20 min; committed to investigating.

## Decisions & Rationale

- **LLM provider framework for Project Surf defined**: Anthropic for production; Amazon Bedrock for enterprise/data residency scenarios (AWS regional infra); Fireworks and OpenRouter as future cost/fallback/test-environment options — to enable cheaper experimentation without compromising production on Anthropic.
- **WorkOS removed from Phase 1 GA, Grafana confirmed**: WorkOS was PoC-only; Grafana self-hosted confirmed for infrastructure monitoring and alerting at GA.
- **Fable 5 as super-bmad orchestrator confirmed**: Achieves 96% performance at 46% cost compared to alternatives; validated with Sam as the efficient production choice.
- **Third pod developer to be added**: Team agreed to expand the pod to increase velocity alongside the ongoing Amarita onboarding.
- **ChatGPT authorized for development overflow**: Permitted to mitigate current tool limitations during high-demand sprints.
- **Workload split target aligned**: 50% refinement, 20% future planning, 30% validation — to rebalance away from mid-sprint correction toward upfront planning.
- **Architectural decisions to be formalized as markdown with trade-offs**: Proposed by Douglas in stand-up to replace open-forum discussion bottlenecks and accelerate resolution.

## Open Loops

- **Expensify access** (carried from 2026-04-17 — stale, consider closing or escalating): Requested from accounting@claritisoftware.com to submit train ticket expenses from the Lévis offsite; no evidence of resolution found in today's data.
- **Vendor US/Canada hosting validation**: Douglas committed in #project-surf-build to validate that all selected Project Surf vendors have US and Canada hosting capabilities and document this in the Architecture doc — awaiting completion.
- **sbmad-land-pr CI hang**: Craig Stickel flagged 45–60 min runtime in #project-surf-build; Douglas committed to investigate; root cause not yet identified.
- **Clarify role re: full project leadership gap**: Douglas to speak with S to determine if full project leadership responsibility is needed to fill a team gap (from Progress Check-In notes).

## Blockers

- **Telemetry configuration being disabled/incorrectly reset**: Identified in Labs session with Thom — environment variable setup is required but not always persisting; fix in progress per Douglas.
- **sbmad-land-pr CI performance**: 45–60 min average to land a PR (target: ≤20 min) due to flaky CI steps and large merge conflicts in project tracking files — investigation pending.
- **Thom cannot access super-bmad repository**: Resolved during Labs session by Douglas granting access via Enterprise PMs group configuration.

## Next Steps

- Validate US/Canada hosting for all Project Surf vendors (Temporal, OpenFGA, etc.) and document in Architecture doc.
- Update BMAD system to version 6.10 (current sprint priority per Progress Check-In).
- Review Justin LaBrash's architecture decision proposals for the Epics board.
- Investigate sbmad-land-pr CI hang (Craig's 45–60 min issue, target ≤20 min); evaluate using a smaller model (Opus or Sonnet) for CI handling steps.
- Optimize CI checks to skip code-related checks when only planning artifacts are uploaded.
- Fix telemetry configuration bug (FR115 recording gate issue) and document setup as explicit user-facing requirement.
- Update orchestrator interface visibility and clarity to prevent user confusion in auto mode.
- Simplify assistant output vocabulary — harden documentation specs and implement a vocabulary filter.
- Onboard Amarita to the workflow to increase team velocity.
- Consult Tim on velocity themes and project plans (Justin LaBrash action item, Douglas to follow up).
- Schedule team work session for next week to address SBMAD improvements and systemic blockers (Justin to coordinate, Douglas to confirm attendance).
- Build a weekly feature/capability summary skill (automated roundup of new features).
- Post SBMAT system update to the team channel after Thom confirms it works.
- Request token limit increase from Colin or MTC for business account.

## Transcript Source (Cleaned)

Douglas's day opened with a brief 9:30–9:45 AM EDT 1:1 with Justin LaBrash (organizer), with Gemini notes attached. Immediately after, Douglas shared shell alias configurations for the super-bmad toolchain with Justin over DM and sent telemetry event file path references.

In the mid-morning, Timothy Meyer opened a thread in #project-surf-build asking which LLM providers to list for Legal's contract documentation. Douglas replied at 11:16 AM proposing Claude (main) and OpenAI GPT (backup), then expanded at 12:04 PM to a four-tier framework: Anthropic for production, Amazon Bedrock for enterprise/data residency (leveraging AWS regional infra), and Fireworks + OpenRouter as future cost/fallback/testing options. Samuel Couture Brochu clarified that the current inference provider in the CC precheck is Gemini (to be replaced by Anthropic), and Douglas and Sam aligned the vendor list: Grafana stays in Phase 1 GA (self-hosted), WorkOS is removed. Douglas committed to adding US/Canada hosting validation to the Architecture doc. He also resolved Onildo Aguiar's MFA blocker via DM ("mfa enabled"), after which Onildo opened PR #537.

The Project Surf Stand-up ran 12:30–1:30 PM EDT with 12 attendees (Timothy Meyer organizer). Douglas reported completing CI memory fixes and implementing testable user roles. Craig Stickel raised an architectural decision on the report builder engine with significant downstream business ramifications. Douglas recommended formalizing open architectural decisions as markdown files outlining trade-offs — the team aligned. Timothy is building a functional requirements tracking matrix for Phase 1 release. Secure credential vaulting for staging environments was also discussed.

Overlapping at 1:00 PM, Douglas ran a Progress Check-In (organizer) with Justin LaBrash and Samuel Couture (Aman Bhalla declined). The team agreed on a workload target of 50% refinement / 20% future planning / 30% validation. BMAD 6.10 update was prioritized. Next steps included architecture proposal review (Justin's Epic board proposals), Tim consultation, scheduling a team work session for next week, and building a bug-tracking skill for velocity monitoring.

At 1:30 PM, the optional CEO Office Hours and Q&A with Cyrus ran for all staff; Gemini notes were produced covering H2 strategy and recent Clariti events.

The 2:30–3:00 PM "Douglas <> Sam" 1:1 (Samuel organizer) covered orchestrator efficiency (Fable 5 at 96%/46% cost), repository hardening to reduce token waste, team expansion (third pod developer), ChatGPT authorization for overflow, and Amarita onboarding priority. Sam suggested a private ENT clinic in Gatineau for Douglas's sinus issues and committed to sending the clinic link.

At 3:00 PM, Douglas ran a 15-minute "Labs: Test new Super-bmad" session with Thom Oguntoyinbo (Douglas organizer). Key findings: missing project markdown file prevents automatic context loading (Thom to raise with Justin); CI checks running on non-code planning artifact PRs cause delays (Douglas to fix); telemetry env var config not persisting (Douglas to fix); assistant uses overly complex vocabulary (Douglas to harden); worktree flag recommended for agent isolation. Douglas granted Thom Enterprise PMs group access mid-session to resolve repo access block. Post-session, Thom shared a Claude Code permission error and a telemetry bug prompt for follow-up.

Post-meetings, Douglas posted a @here feedback poll in #project-surf-build on super-bmad adoption — Onildo, Craig, and Timothy all responded positively. Douglas also shared a tip in #project-surf-how-we-build promoting the /bmad-technical-research skill for evidence-backed architectural decisions. Craig Stickel raised the sbmad-land-pr 45–60 min CI hang issue in a DM; Douglas committed to investigate.
