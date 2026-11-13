---
date: "2026-05-20"
weekday: "Wednesday"
author: "douglas-clariti"
quality: "complete"
sources_used:
  - google_calendar
  - slack
sources_empty:
  - gmail
  - google_drive
open_loops_carried: 0
tags:
  - project-surf
  - super-bmad
  - coderabbit
  - claude-code
  - code-review
  - onboarding
  - workflow-builder
  - github
---

# Daily Summary — Wednesday, May 20, 2026

## Summary

- Organized and led "Progress Check-In" with Justin LaBrash, Samuel Couture, and Aman Bhalla at 1:00 PM EDT to align on project-surf and super-bmad status (transcript not available).
- Completed self-guided ONBOARDING session reviewing the Clariti Launch Product Demo recording via P&T Team Calendar at 2:00 PM EDT (transcript not available).
- Posted a comprehensive status update in #project-surf-how-track covering 9 merged PRs today on project-surf: technical blueprint (#61), work item reorganization (#62), naming fixes (#63), planning close-out/green light (#64), phase breakdown and story assignment (#65), repo skeleton (#66), codebase foundation (#67), cloud infrastructure groundwork (#68), and first automated tests (#69); 2 PRs remain in review (database schema #70, cloud infrastructure #71).
- Shipped bun migration for super-bmad installer and DevOps stories (#320 DONE); two additional super-bmad PRs in review (#321 DevOps faster runtime, #322 installer generate-board).
- Resolved a PR issue for Justin LaBrash (super-bmad #319) — confirmed "all good now" at 11:15 AM; Justin merged.
- Shared last week's super-bmad slides (sbmad-skill-builder-primer.html, weekly-review-2026-05-15.html) with Samuel Couture Brochu via DM in response to his demo request.
- Successfully integrated CodeRabbit into the clariti-labs GitHub org for automated CI code review; confirmed it is active and auto-reviewing PRs on super-bmad.
- Tipped team in #project-surf-how-track about Claude Code Desktop groups feature for managing multiple agents across projects simultaneously.
- Sent birthday wishes to Hayley Wasylycia and Samantha Pickett in #clariti-shoutouts.

## Decisions & Rationale

- **Integrate CodeRabbit into clariti-labs org CI**: Decided to add CodeRabbit alongside existing agents (Blind Hunter, Edge Case Hunter, Acceptance Auditor) for automated PR review on CI; Herman Chan flagged availability and it is now active on super-bmad with project-surf integration in progress.
- **Replace useEffect with useMountEffect in developer agent**: Agreed with Herman Chan to add a rule targeting useEffect replacement with useMountEffect (or equivalent) to reduce complexity and bugs in the codebase.
- **Add CodeRabbit Code Security tool to internal agent suite**: Flagged intent to incorporate the CodeRabbit Code Security tool into internal agents after reviewing its capabilities.
- **project-surf planning phase officially closed**: Obtained "ready to build" green light (PR #64), formally transitioning project-surf from planning to build phase today.

## Open Loops

- PR #70 (project-surf: database schema) — in review, awaiting approval.
- PR #71 (project-surf: cloud infrastructure setup) — in review, awaiting approval.
- PR #321 (super-bmad: DevOps skills default to faster runtime) — in review, awaiting approval.
- PR #322 (super-bmad: installer generate-board merge) — in review, awaiting approval.
- CodeRabbit setup on project-surf repo — Herman Chan working on access/indexing; not yet confirmed.

## Blockers

- None reported today.

## Next Steps

- Finish Epic 1 of project-surf tomorrow (working prototype of Phase 1 per product requirements) — stated goal for today and tomorrow.
- Follow up on PRs #70, #71, #321, #322 still pending review.
- Complete CodeRabbit integration for project-surf repo (Herman Chan in progress).
- Explore adding CodeRabbit Code Security tool to the internal agent suite.
- Investigate whether BMAD agents support the `/simplify` skill (agreed to check with Herman Chan).
- Test CodeRabbit slop detection when public-repo support becomes available.

## Transcript Source (Cleaned)

**Google Calendar:**
- 1:00 PM–1:20 PM EDT — Progress Check-In (organizer: Douglas Mendes; attendees: Justin LaBrash, Samuel Couture, Aman Bhalla optional). Recurring meeting. No transcript linked. (transcript not available)
- 2:00 PM–3:00 PM EDT — ONBOARDING: Self-guided Launch Product Demo (P&T Team Calendar; organizer: fiona.runa@claritisoftware.com). Self-paced Zoom recording. No live session. (transcript not available)

**Slack — DM with Justin LaBrash (9:09 AM–11:15 AM EDT):**
Douglas opened the morning by tipping Justin about the Claude Code Desktop groups feature for multi-project agent management. He requested a quick sync around 9:58 AM, which Justin confirmed; a Google Meet was started. At 11:15 AM Douglas confirmed a PR issue was resolved ("all good now") and Justin merged it (super-bmad #319).

**Slack — #clariti-shoutouts (11:33 AM EDT):**
Douglas posted birthday wishes for Hayley Wasylycia and Samantha Pickett.

**Slack — DM with Samuel Couture Brochu (1:23 PM EDT):**
Samuel requested last week's slides for a demo; Douglas shared links to sbmad-skill-builder-primer.html and weekly-review-2026-05-15.html from the super-bmad repo (_bmad-output/primers). Samuel confirmed receipt. Brief follow-up discussion about getting other devs onto super-bmad.

**Slack — #project-surf-how-track (1:19 PM onwards EDT):**
Douglas posted a detailed team status update covering two big days across project-surf and super-bmad, listing all PRs by status. Herman Chan mentioned the Enterprise/MidMarket teams use CodeRabbit; Douglas asked to have it added to project-surf CI and proposed running it alongside existing review agents. Herman attempted to add CodeRabbit to clariti-labs org; Douglas confirmed Herman was already an org owner. CodeRabbit was successfully activated on super-bmad and is now auto-reviewing PRs. Discussion also covered: replacing useEffect with useMountEffect in developer agent, exploring CodeRabbit Code Security tool, ast-grep, path-instructions for monorepo, and BMAD knowledge-base sync.

**Slack — DM with Herman Chan (~1:58 PM EDT):**
Douglas shared a Claude Code tip (groups for multi-project agents) and troubleshot a strange error Herman encountered. Later Herman asked whether BMAD agents use `/simplify`; Douglas noted he doesn't think so but agreed to investigate, noting BMAD agents are model/platform agnostic (support opencode, codex, claude, and others).
