---
date: "2026-11-19"
weekday: "Thursday"
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
  - orchestrator
  - bmad
  - qa-testing
  - hiring
  - ai-gateway
  - cdi
---

# Daily Summary — Thursday, 2026-11-19

## Summary
- Prepped with Marnix Faes on the Senior MLOps Engineer interview structure and AI gateway expectations, sharing my three behavioural/architecture questions in the Slack group DM with Samiha Nusrat (transcript available).
- Co-led the Technical Interview with Saeed Pouryazdian alongside Marnix, probing event-driven debugging and stuck-message recovery and covering data-residency constraints for the AWS migration (transcript available).
- Joined "Testing on CDI" with Timothy Meyer, Aseem Gupta and Dipak Parmar, explaining that the canonical-structure linter removed Aseem's 20 screen tests on Nov 13 and committing to wire the test design skill into the orchestrator (transcript available).
- Reported at Project Surf Stand-up that 113.25 is in QA and an architecture cleanup document is in progress; team agreed on quarterly code-health cleanup epics (transcript available).
- Ran Progress Check-In with Ankit Mittal, Samuel Couture and Justin LaBrash: updated the orchestrator architecture with async QA/test design steps, landed the biox orchestrator change, and introduced two new debug skills (session-level and BMAD system-level) (transcript available).
- Deleted non-BMAD test files committed directly to the repo and restricted process changes to Ankit and myself.
- Held 1:1 with William Veldhuis (transcript available — Gemini produced no summary).
- Pinged Ryan Huang in #project-surf-build and set up a catch-up call to onboard him on the current work process.
- Attending "Discuss Module/Foundations Activation" with Eric McClelland and team (transcript not available).

## Decisions & Rationale
- **Add test design / QA steps to the orchestrator before story creation**: agreed in both Testing on CDI and Progress Check-In, since async epics lacked structured test design.
- **Ankit owns discovery, Douglas owns implementation**: lets Ankit engage Karan and Tim on design/QA pain points instead of rushing into code.
- **Process/repo changes restricted to Ankit and Douglas**: prevents structural drift after non-BMAD test files were added.
- **Split debugging into two skills (session vs. BMAD system)**: clearer separation between harness/CLI/model issues and code-level problems.
- **E2E automation prioritized, environment-agnostic, run on all PRs**: critical paths for permitting/planning need early break detection.
- **Ignore last-minute interview questions; use prepared structure**: questions arrived ~2 minutes before the interview.

## Open Loops
- Intermediate QA environment between dev and staging — deferred to the technical team.
- Approved method for managing multiple test user accounts for E2E permission tests — undecided.
- Interview scorecard for Saeed Pouryazdian to submit in Greenhouse.
- Aseem to restore the 20 deleted screen tests into a linter-ignored folder and rerun them on refreshed dev.
- Timothy Meyer to create tickets for the permitting E2E automation job and to share the permitting script for review.

## Blockers
- None reported today.

## Next Steps
- Update the orchestrator to run the test design skill during epic creation.
- Push the two new debug skills and have Ankit run them to generate logs/case artifacts.
- Release a new version with the new skills to the channel tomorrow; install and run a story on Project Surf, targeting release Monday/Tuesday (Ankit to shadow).
- Review Samuel's PR on testing environments and module configuration.
- Share the architecture cleanup document with team leads to distribute cleanup tasks.
- Move completed QA stories to done and recheck status.
- Catch up with Ryan Huang on current work process.

## Transcript Source (Cleaned)
I started the day prepping with Marnix for the Senior MLOps Engineer interview. We agreed on a 30–40 minute technical block, I'd ask the candidate to walk through an end-to-end system they're proud of, and Marnix would probe versioned ML pipelines and the AI gateway we're planning for Surf (unified routing to Anthropic/Google/OpenAI, spend tracking per user and city, PII filters, fallbacks). I posted my three questions in the group DM with Samiha and Marnix. We then interviewed Saeed Pouryazdian; I asked how he debugs stuck messages in event-driven systems and suggested customer-facing manual retries from saved message state, and I explained our Canada/US data-residency constraints.

In Testing on CDI with Tim, Aseem and Dipak, I explained the Nov 13 deletion of Aseem's tests was caused by the linter enforcing the canonical structure, so tests need a designated or ignored folder. We aligned on prioritizing environment-agnostic E2E automation on PRs and on me updating the orchestrator so the test design skill runs at epic creation, with Aseem trying it manually at story level during QA.

At the Project Surf stand-up I reported 113.25 in QA and that I'm drafting an architecture cleanup doc; the team agreed to recurring quarterly code-health epics. In my Progress Check-In with Ankit, Samuel and Justin, I walked through the orchestrator changes adding async test design/QA steps, got the biox change merged, deleted non-BMAD test files from the repo, and introduced two debugging skills. Ankit will run discovery with Karan and Tim while I handle implementation, and Ankit will shadow me when I run a Surf story ahead of next week's release.

In the afternoon I had my 1:1 with William, set up a catch-up with Ryan Huang (just back from leave), and joined the Module/Foundations Activation discussion with Eric.
