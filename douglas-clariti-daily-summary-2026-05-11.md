---
date: "2026-05-11"
weekday: "Monday"
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
  - super-bmad
  - project-surf
  - bun
  - vercel-ai-sdk
  - llm-evals
  - clariti
  - onboarding
  - anthropic-api
---

# Daily Summary — Monday, May 11, 2026

## Summary

Back into sprint work on Monday. Shared a detailed Slack post in #project-surf-how-track outlining the new super-bmad skill-testing framework (Bun + Vercel AI SDK with LLM-judge scoring), then ran the weekly Progress Check-In with Justin Labrash, Samuel Couture Brochu, and Aman Bhalla. The afternoon included an unscheduled sync with Justin Labrash and the P&T onboarding session for new hire Meghan Pereira.

- Published a detailed technical post in #project-surf-how-track describing the super-bmad skill-testing framework — Bun + Vercel AI SDK with LLM-judge scoring, structure + quality gates, and a new `sbmad-skill-builder` skill in progress; asked Justin Labrash to hold off testing until harness tests are finalized today.
- Thanked Colin John (DM) for resolving an API access issue; Colin confirmed that API keys are scoped to specific workspaces for governance/security and that API usage (Claude Code, Workbench, API) is billed via separately purchased credits outside the Claude Enterprise plan.
- Ran recurring "Progress Check-In" (1:00–1:20 PM EDT) as organizer with Justin Labrash, Samuel Couture Brochu, and Aman Bhalla (transcript not available).
- Initiated a quick unscheduled Google Meet with Justin Labrash (~1:47 PM EDT, duration unknown).
- Welcomed Meghan Pereira (new Senior Manager, Customer Support) in #announcements.
- Attended "ONBOARDING SESSION: Intro To Marketing" (4:00–5:00 PM EDT) as attendee alongside Natasha Ulanowski, Emily Lanzillotta, Jacky Tam, Amandeep Kaur, and Meghan Pereira — organized by P&T Team Calendar (transcript not available).
- Congratulated Samuel Couture Brochu in #project-surf-how-track on the arrival of baby Hana (Sunday).

## Decisions & Rationale

- **Bun + Vercel AI SDK selected for super-bmad skill evals**: Chose this stack over pytest/subprocess, DeepEval, and Anthropic's `claude-skill-creator` because it is model-agnostic (Sonnet ↔ Opus ↔ Haiku is a one-line change), uses the `generateText`/`generateObject` APIs the JS/TS team already knows, supports typed LLM-judge verdicts via Zod structured output, has built-in tracing exports (Confident AI et al.), and avoids additional eval-framework dependencies.
- **Two-gate eval strategy adopted**: Deterministic `bun test` runs on every PR; live-LLM eval (`RUN_SKILL_EVALS=1 bun run test:eval`) runs manually — balances CI speed with deeper quality checks.
- **Hold on Justin Labrash testing super-bmad skills**: Asked Justin to wait for harness tests before trying the framework so he does not hit incomplete scaffolding.

## Open Loops

- **Expensify access** (carried from 2026-04-17): Awaiting response from accounting@claritisoftware.com before Lévis offsite train ticket expenses can be submitted.
- **`sbmad-skill-builder` skill**: Currently under active development — folder scaffolding, starter rubric/dataset generation, and `bun test` wiring not yet ready for team use; expected to mature this week.

## Blockers

No blockers identified today.

## Next Steps

- Complete remaining super-bmad harness tests today and signal Justin Labrash once ready.
- Continue `sbmad-skill-builder` skill development — add current skills to the new eval model this week.
- Follow up on Expensify access with accounting@claritisoftware.com (open since 2026-04-17).
- Continue weekly standup/review cadence; Friday sprint review and planning upcoming.

## Transcript Source (Cleaned)

Monday opened with Douglas posting a long-form technical writeup in #project-surf-how-track addressed to Justin Labrash and Samuel Couture Brochu, explaining the new approach to testing super-bmad skills. After evaluating pytest + subprocess (too many edge cases), DeepEval (extra deps and auth complexity), and Anthropic's `claude-skill-creator` (Python-only, no behavioural grading), Douglas landed on Bun + Vercel AI SDK. The framework uses three pieces per skill — a dataset, a task, and scorers — plus two test gates: a deterministic `bun test` for every PR and a live-LLM eval gated behind `RUN_SKILL_EVALS=1`. A new `sbmad-skill-builder` skill is also in progress to scaffold all of this automatically. Justin thanked Douglas and said he'd try it; Douglas asked him to hold off until today's harness tests are in place. Justin agreed and said he'd focus on security and accessibility requirements instead.

Separately, Douglas thanked Colin John in a DM (context not shown — likely related to API key access being unblocked). Colin followed up with a note that API keys are restricted to specific workspaces rather than the default org-wide context for governance and security reasons, and that API usage (Claude Code, Workbench, direct API) is billed via credits purchased separately from the Claude Enterprise plan.

At 1:00 PM EDT, Douglas ran the weekly Progress Check-In as organizer via Google Meet with Justin Labrash, Samuel Couture Brochu, and Aman Bhalla (Aman optional). No transcript was linked. At ~1:47 PM, Douglas pinged Justin Labrash asking if he had 3 minutes; Justin said yes and they started a Google Meet.

Douglas welcomed Meghan Pereira in #announcements at 11:02 AM — she joined as Senior Manager, Customer Support. From 4:00–5:00 PM EDT Douglas attended the P&T "Intro To Marketing" onboarding session alongside Natasha Ulanowski, Emily Lanzillotta, Jacky Tam, Amandeep Kaur, and Meghan Pereira; Justin Labrash was tentative. No transcript was linked.

At 3:18 PM, Samuel Couture Brochu announced in #project-surf-how-track that he's out for the week — baby Hana arrived Sunday. Douglas and Justin both congratulated him.
