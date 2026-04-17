---
week: "2026-W16"
date_range: "2026-04-13 to 2026-04-19"
author: "douglas-clariti"
days_covered: 2
days_expected: 5
days_missing:
  - 2026-04-13
  - 2026-04-14
  - 2026-04-15
tags:
  - offsite
  - sprint-planning
  - bmad
  - ai-experiment
  - clariti
  - architecture
  - retrospective
  - levis
  - project-surf
  - super-bmad
  - sprint-1
  - claude-design
  - figma
  - expensify
---

# Weekly Rollup — 2026-W16

**2026-04-13 to 2026-04-19** | **2/5 days covered**

> Note: Summaries for Mon Apr 13, Tue Apr 14, and Wed Apr 15 are missing — these were offsite days (Lévis, QC, Days 1–3) with no daily summaries generated. Data below reflects Thu Apr 16 and Fri Apr 17 only.

## Themes & Focus Areas

- **AI Experiment Pod Offsite Wrap-Up**: The week closed out the 4-day Lévis offsite (Apr 13–16). Day 4 (Thursday) covered open items review, Sprint 1 planning, architecture spike scoping, communication plan alignment, and a closing retrospective before the team travelled home.
- **Sprint 1 Kickoff**: Friday was the first working day back, with two focused meetings with Justin Labrash (Project structure discussion; Definitions of Done) to begin Sprint 1 execution in earnest.
- **SuperBMAD & Tooling Foundation**: The super-bmad repo baseline was built and tested locally, an install command was shared with the PM, and a formal Git-based skill contribution workflow (branch → SKILL.md → test → PR) was defined and communicated to the team.
- **Operational AI Prompt Infrastructure**: Proposed a private Clariti repo for EPD team operational AI prompts modeled after skills.sh; received positive alignment from Aman Bhalla and Justin Labrash in #project-surf-how-track.

## Key Accomplishments

- Completed the AI Experiment Pod offsite in Lévis, QC (Apr 13–16) — Sprint 1 scope, architecture spikes, and communication plan all finalized before returning home.
- Built and tested the super-bmad repo baseline locally; shared install command (`npx github:clariti/super-bmad install`) with Justin Labrash and confirmed the path to team-wide clone access.
- Shared Claude Design dashboard prototype with Justin Labrash, walked through the Figma-import workflow, and granted edit access — moving the prototype to a usable state.
- Defined and proposed the SuperBMAD skill contribution workflow to the team; workflow adopted.
- Proposed private Clariti repo for EPD operational AI prompts — team alignment achieved, advancing auditable AI knowledge infrastructure.
- Retrieved offsite summary doc link from Justin Labrash, resolving a next step carried from Apr 16.
- Submitted Expensify access request to accounting@claritisoftware.com for Lévis offsite train ticket expenses.

## Decisions Made

- **Sprint 1 scope finalized**: Team aligned on Sprint 1 work items at the offsite wrap session to establish clear ownership and momentum returning home.
- **Communication plan agreed**: Established post-offsite communication plan with Samuel Couture, Aman Bhalla, and Justin Labrash to keep stakeholders informed of AI Experiment Pod progress.
- **Architecture spikes scoped**: Specific spikes identified to de-risk BMAD implementation in the near term.
- **SuperBMAD skill contribution workflow defined**: Git-based branch → `module/skills/<skill-name>/SKILL.md` → test install → PR workflow established, ensuring all contributions are auditable and peer-reviewed.
- **Private operational prompt repo proposed**: Recommended adding a private Clariti repo for EPD day-to-day AI personas, workflows, and patterns; team responded positively.

## Open Loops (End of Week)

- **Expensify access** (opened Apr 17): Requested from accounting@claritisoftware.com — awaiting response before train ticket expenses from the Lévis offsite can be submitted.

## Carried Into Next Week

- Finalize super-bmad repo baseline and confirm team can clone.
- Begin week-of-Apr-20 Sprint 1 cadence: daily standups, Friday review, Friday sprint planning.
- Cloud provider selection: scrape RFDs to gather requirements (per Justin's Apr 20–25 plan).
- Align with "What stream" on artifacts for PRD and Design.
- Set up Kanban board (Justin and Douglas) and roadmap tracker for leadership and go/no-go.
- Follow through on communication plan agreed at Lévis offsite (Samuel Couture, Aman Bhalla, Justin Labrash).
- Begin architecture spikes scoped during Lévis offsite wrap.
- Review offsite summary doc once available.
- Resolve Expensify access request (accounting@claritisoftware.com).

## Meetings & Collaboration

- 3 meetings attended (from available data — Mon–Wed offsite sessions not captured)
  - Thu Apr 16: Day 4 offsite session (Sprint 1 planning, architecture spikes, comms plan, retrospective)
  - Fri Apr 17: "Project structure discussion" with Justin Labrash (10:35–11:35 AM EDT)
  - Fri Apr 17: "Definitions of Done" with Justin Labrash (2:00–2:30 PM EDT)
- Key collaborators: Justin Labrash (PM), Samuel Couture (CTO), Aman Bhalla (VP Product)

## Data Source Coverage

| Day | Calendar | Gmail | Slack | Drive | Notes |
|-----|----------|-------|-------|-------|-------|
| Mon 2026-04-13 | — | — | — | — | No summary (offsite Day 1) |
| Tue 2026-04-14 | — | — | — | — | No summary (offsite Day 2) |
| Wed 2026-04-15 | — | — | — | — | No summary (offsite Day 3) |
| Thu 2026-04-16 | ✓ | empty | empty | empty | Partial quality; offsite Day 4 |
| Fri 2026-04-17 | ✓ | ✓ | ✓ | empty | Complete quality |

> Systemic gap: Gmail, Slack, and Drive were all empty on Thu Apr 16 (offsite conditions). No systemic connector issue — single-day gap explained by travel/offsite context. Google Drive returned no data on either available day — worth monitoring next week.
