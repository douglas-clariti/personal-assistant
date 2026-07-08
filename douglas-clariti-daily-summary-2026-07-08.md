---
date: "2026-07-08"
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
  - compliance
  - sprint-planning
  - github-actions
  - cost-optimization
  - onboarding
  - ai-workflow
---

# Daily Summary — Wednesday, July 8, 2026

## Summary

Busy mid-week day spanning a morning car appointment, four back-to-back Clariti meetings in the early-to-mid afternoon, and active async work in Slack and GitHub. Key themes: team onboarding of Amrita, legal compliance requirements for Project Surf vendor data, cost-management improvements to the SBMAD orchestrator, and a GitHub Actions incident unblocked by merging Timothy Meyer's PR #517.

- Declined "Douglas / Justin Daily" (9:30–9:45 AM EDT) due to car repair appointment; proactively notified Samuel Couture Brochu and Justin LaBrash in #pod-superbmad (transcript not available).
- Attended **Douglas / Samiha - Onboarding Check-in** with Samiha Nusrat (organizer) via Google Meet, 12:00–12:30 PM EDT (transcript available).
- Attended **Project Surf Stand-up** via Google Meet, 12:30–1:30 PM EDT, with full EPD team (Aman Bhalla, Edwin Leong, Karan Kapoor, Eric McClelland, Thom Oguntoyinbo, Justin LaBrash, Amrita Patra, Craig Stickel, Onildo Aguiar, Samuel Couture Brochu, Timothy Meyer); Gemini transcript available but only 9 seconds captured (transcript available — content minimal).
- Organized and led **Progress Check-In** with Aman Bhalla, Samuel Couture Brochu, and Justin LaBrash, 1:00–1:20 PM EDT; covered legal compliance, epic restructuring, CI status, cost management, and team onboarding (transcript available).
- Attended **Douglas / Amrita** session with Amrita Patra (organizer), 2:00–3:00 PM EDT; deep dive on AI development workflows, compliance framework verification, testing strategy with tia module, and architecture documentation standards (transcript available).
- Confirmed Onildo Aguiar's orchestrator was using individual API keys instead of Anthropic seats, causing ~$1,000/day cost spikes; implemented a fix and is now monitoring usage.
- Introduced **SB orchestrate** skill to the orchestrator, automating model selection using a 1–9 task difficulty grid to optimize parallel task processing and token consumption.
- Flagged stale `docs/epics*.md` reference in Justin LaBrash's SBMAD PR #644 in #pod-superbmad; also identified a redundant epic escalation rule already covered in `_super-bmad/.skill-chain-catalog.yaml.upgrade-template`; Justin opened PR #646 to remove all stale references.
- In DM with Justin LaBrash: clarified that the existing `/bmad-board sprint` command supports sprint/epic board creation; confirmed milestones schema is the only gap; pointed out sprint planning skill already handles assigning epics and stories to developers.
- Met with Craig Stickel at 3 PM (unscheduled call via DM); discussed view audit logs page behavioral filter changes for performance and UX; shared AWS Cell-Based Architecture docs as reference material.
- In #project-surf-build: identified a stuck, uncancellable GitHub Actions run; obtained and merged Timothy Meyer's PR #517; advised Timothy that squash-and-merge is acceptable for non-critical check failures.
- Created a temporary login workflow to enable developers to perform end-to-end role and permission testing (pending Tim Meyer approval to document and publish).

## Decisions & Rationale

- **Cost optimization via SB orchestrate skill**: Deployed a new SBMAD orchestrator skill that auto-selects model tier based on task difficulty (1–9 grid); Fable is reserved for complex high-dependency tasks, Opus for ad-hoc work — avoids Tim-style unintentional Fable usage and eliminates manual model selection overhead.
- **Headroom usage mandated**: Team aligned on requiring headroom usage across development processes to control token costs and cloud billing spikes.
- **EPR folder stays in main PRD repository**: Confirmed EPR (surf permitting extension) will not have a standalone repository; it remains integrated into the existing single PRD repository per Justin's recommendation.
- **SBMAD PR #646 approved**: Removal of all stale `docs/epics*.md` references from skill.md and of the redundant epic escalation block; these are already covered in the skill-chain-catalog — no duplication needed.
- **GitHub Actions PR #517 merged**: Unblocked a stuck CI run for Timothy Meyer by merging his PR under the decision that only required checks matter; non-critical bleeding failures can be ignored.

## Open Loops

- **Expensify access** (carried from 2026-04-17 — stale — consider closing or escalating): Requested from accounting@claritisoftware.com after the Lévis offsite; no resolution visible in today's data — 82+ calendar days with no follow-up captured.
- **Temporary login workflow approval**: Created workflow to enable dev end-to-end testing; needs Tim Meyer's sign-off before being published to the team channel.
- **Telemetry fix notification**: Need to post instructions in the team channel for colleagues to run the telemetry fix deployed today.
- **Justin LaBrash final change proposal**: Justin to complete epic/story restructuring and submit change proposal to Douglas for review (action item from Progress Check-In).

## Blockers

- **GitHub Actions instability**: Reported runs taking 20+ minutes and becoming uncancellable in #project-surf-build; partially resolved by merging PR #517, but underlying GitHub Actions consistency issue is unresolved.

## Next Steps

- Consult with Tim Meyer to approve and document the temporary login workflow; publish process to team channel.
- Post telemetry fix instructions to team channel (action from Progress Check-In).
- Contact compliance team to identify which specific frameworks (SOC 2, etc.) are required for Project Surf.
- Create **diagramming skill** to auto-generate database relationship and sequential diagrams (committed in Douglas/Amrita session).
- Present **tia module** and Playwright tasks to Amrita Patra and Craig Stickel in next week's session.
- Review Justin LaBrash's final epic/story restructuring change proposal once submitted.
- Monitor cost telemetry after Onildo Aguiar API key fix to confirm costs have normalized.

## Transcript Source (Cleaned)

The morning began with a car repair appointment (10:00–11:30 AM EDT). Douglas proactively notified Samuel Couture Brochu and Justin LaBrash in #pod-superbmad at 8:53 AM and declined the recurring Douglas/Justin Daily meeting.

At noon, Douglas attended an onboarding check-in with Samiha Nusrat (Gemini notes captured). The full Project Surf Stand-up followed at 12:30 PM with the entire EPD team, though the Gemini transcript captured only 9 seconds of content and produced no usable notes.

Douglas organized a Progress Check-In (1:00–1:20 PM) with Aman Bhalla, Samuel Couture Brochu, and Justin LaBrash. Topics included: Aman's conversation with lawyers requesting a vendor and integration point list for Surf data (Samuel narrowing scope to avoid resource waste); Justin's ongoing work restructuring epics and stories with Tim, including a gap in BMAD around dependency mapping and milestones; Douglas's temporary login workflow created to allow developers to test roles and permissions (login epic not yet built); Marita's first story nearly complete, with onboarding meeting recorded; Onildo Aguiar's orchestrator running on individual API keys causing ~$1,000/day cost spikes — Douglas implemented a fix; the decision to reserve Fable for complex tasks and use Opus for ad-hoc work; and Douglas's new SB orchestrate skill automating model selection on a 1–9 difficulty grid. CI environment is functional with non-critical failures in sprint status.yaml deferred.

From 2:00–3:00 PM, Amrita Patra organized a continuation session with Douglas. They covered: compliance framework verification with the security team (SOC 2 and others), using AI to generate sequential diagrams and database relationship visualizations before coding, the Cloud HUD plugin for real-time agent visibility, avoiding quick-dev shortcuts for functional requirement changes (use SB-MAD change commands instead), the ask-first-code-second approach with test design validation before implementation, and architecture decisions centralized in plan/texture/spine docs. A new diagramming skill and a next-week demo of the tia module were committed.

In the afternoon, Douglas spotted Justin LaBrash's SBMAD PR #644 adding epic and PRD update flows and flagged: (1) the agent was reading a stale `docs/epics*.md` path removed previously; (2) a redundant epic escalation block in the skill already present in the skill-chain-catalog. Justin investigated, found the stale path in skill.md references, and opened PR #646 removing them. Separately, an unscheduled DM call with Craig Stickel covered the view audit logs page — behavioral filter changes for performance and UX, and a re-sign/re-link question — Douglas shared AWS Cell-Based Architecture docs as reference. In #project-surf-build, a stuck GitHub Actions run led Douglas to get and merge Timothy Meyer's PR #517 and advise the team to focus only on required checks for non-critical failures.
