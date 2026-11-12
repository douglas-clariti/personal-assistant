---
date: "2026-10-28"
weekday: "Wednesday"
author: "douglas-clariti"
quality: "partial"
sources_used:
  - google_calendar
  - slack
sources_empty:
  - gmail
  - google_drive
open_loops_carried: 4
tags:
  - project-surf
  - workflow-engine
  - temporal
  - story-25-22
  - super-bmad
  - agent-identity
  - onboarding
  - staging
---

# Daily Summary — Wednesday, 2026-10-28

## Summary
- Douglas cancelled his meetings for the day (declined Progress Check-In and the End of Sprint Demo) and told #project-surf-build, flagging Timothy Meyer and Justin LaBrash, that he was focusing on workflow engine issues found in end-to-end testing.
- The three workflow engine issues Douglas named: the worker stops processing tasks and stalls application starts and staff assignments; publishing a new workflow version breaks applications on older versions; repeated retries use up worker capacity. He is fixing these and adding bounded retries.
- Douglas confirmed in #project-surf-build that the workflow save fix works on Dev after Timothy's walkthrough, and asked Timothy to check it too.
- Douglas met with Justin LaBrash in a 1:1 call from 9:30 to 11:00 (transcript available).
- Douglas ran "Project Surft Stories & Task Management" with William Veldhuis (transcript available), pointed him to `/sbmad-explain`, assigned him story 116.1, and asked him to get Project Surf AWS access from Colin John.
- Douglas flagged a scope mismatch in story 25.22 to Edwin Leong in #project-surf-build: the gate checks only the current correction round, but Complete closes every open document request. Eric McClelland approved adding the Complete fix to 25.22.
- Douglas agreed in #project-surf-build that Amrita Patra takes story 80.21 to unblock her story 12.26, since he is focused on other work.
- Douglas proposed to Samuel Couture over Slack DM that coding agents get their own Git and GitHub identity in super-bmad (for example `claude@claritisoftware.com`), with humans still accountable through code review and PR approval.
- Douglas pushed back his 1:1 with Ryan Huang.

## Decisions & Rationale
- **Workflow engine fixes take priority over today's meetings**: E2E testing found stalls, version-publish breakage and retry exhaustion that put the beta at risk.
- **Add the Complete fix to story 25.22 (Eric McClelland)**: checking one list and closing another is a bug. Complete will close only the current round's requests through one shared scope with the gate, which also protects deferred documents (29.2).
- **Amrita takes 80.21**: it unblocks her 12.26 while Douglas works on the workflow engine.
- **Proposed agent identity for super-bmad commits and PRs**: the agent writes the code and commits, so it should be the author. People stay accountable through review and approval.

## Open Loops
- Finish the workflow engine fixes and bounded retries (worker stalls, version-publish breakage, retry exhaustion).
- Story 25.22: build the narrowed Complete with a shared scope, update the existing "close everything" test, add the outside-round test and Edwin's three boundary cases, and record the amendment in the story file.
- Agent identity proposal for super-bmad is waiting on Samuel Couture's response.
- William Veldhuis needs Project Surf AWS access from Colin John before starting 116.1.
- Create the staging pentest accounts (one per role plus a fake citizen) and send the credentials to Craig Stickel (carried from 2026-10-27).
- Staging bug where new applications fail with invalid form/intake errors (Justin LaBrash); this may be one of today's workflow engine issues (carried from 2026-10-27).
- 78.50 follow-ups with Timothy Meyer: the error state shown before save, and the Gate label requirement from 109.23 (carried from 2026-10-27).
- 30-minute BMAD and dev-cycle session for Simone Giacomel, not yet scheduled (carried from 2026-10-27).

## Blockers
- Workflow engine instability (worker stalls, version-publish breakage, retry exhaustion) blocks reliable end-to-end flows on Project Surf.
- William Veldhuis cannot fully start 116.1 until he has Project Surf AWS access.

## Next Steps
- Land the workflow engine fixes and bounded retries, then redeploy and re-test end to end.
- Implement the amended 25.22 and call out the behaviour change in the PR.
- Follow up with Samuel on the agent identity proposal.
- Check on William's progress with 116.1 and his environment setup on Windows/WSL.
- Set up the pentest accounts for Craig.

## Transcript Source (Cleaned)
I started the day confirming in #project-surf-build that the workflow save is fixed on Dev after Tim's walkthrough, and asked him to check it too. I then had a long call with Justin from 9:30 to 11. I pushed my 1:1 with Ryan and told William I'd need a bit more time because I was fixing a problem.

Before noon I told the team I was cancelling my meetings to focus on the workflow engine. End-to-end testing found three problems: the worker can stop processing tasks and stall application starts and staff assignments, publishing a new workflow version can break applications already on an older version, and repeated retries can use up worker capacity. I'm fixing these and adding bounded retries. I declined the Progress Check-In and the End of Sprint Demo.

At noon I met William to get him up and running. I pointed him to `/sbmad-explain`, gave him story 116.1, helped him with his Windows setup (WSL), and asked him to get Project Surf AWS access from Colin John.

While working on story 25.22 I found that the gate checks only the current correction round's documents, but Complete closes every open request on the application, and an existing test expects that. I asked Edwin if we could include the Complete fix. Eric approved it: one shared scope for checking and closing, update the old test, add a test that an outside-round request stays open, keep Edwin's three boundary cases, and record the amendment in the story file. Amrita offered to take 80.21 to unblock her 12.26, and I gladly agreed.

With Sam, I added one point to what he shared: agents should have their own Git and GitHub identity. The agent does the implementation and Git operations under its own account, while we review, test and approve it.
