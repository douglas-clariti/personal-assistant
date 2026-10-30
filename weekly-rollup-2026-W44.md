---
week: "2026-W44"
date_range: "2026-10-26 to 2026-11-01"
author: "douglas-clariti"
days_covered: 5
days_expected: 5
days_missing: []
tags:
  - project-surf
  - platform-ops
  - temporal
  - qa
  - design-system
  - onboarding
  - github
  - staging
  - pentest
  - compliance
  - bmad
  - aws-bedrock
  - workflows
  - workflow-engine
  - story-25-22
  - super-bmad
  - agent-identity
  - ci
  - kubernetes
  - orchestrator
  - figma
  - surf-compliance
  - debugging
  - dev-environment
  - release-promotion
  - devops
  - epr
---

# Weekly Rollup — 2026-W44

**2026-10-26 to 2026-11-01** | **5/5 days covered**

## Themes & Focus Areas
- **Workflow Engine Stability**: Douglas cancelled his Wednesday meetings to fix three engine problems found in end-to-end testing: worker stalls, version-publish breakage, and retry exhaustion. Bounded retries were part of the fix. Story 78.50 failed QA on Monday because Activity Groups raised missing-Rule errors, and the workflow save fix was confirmed on Dev on Wednesday.
- **Platform, CI & Staging Operations**: Monday's Platform update announced the Temporal console, the EKS Metrics Server, ~5-minute sharded PR checks and a single deploy pipeline. During the week Douglas fixed the intermittent 502s, redeployed staging twice for the Internal POC team, fixed CDI CI node-replacement permissions, traced a 500 crash to a migration and fixed it, and documented the self-serve staging deploy flow.
- **Onboarding New Team Members**: William Veldhuis (1:1, CDI/Super Bmad walkthrough, story 116.1, Windows/WSL setup) and Simone Giacomel (BMAD guidance, Project Surf walkthrough, architecture docs) were onboarded. Douglas also arranged GitHub org invites for Sree and Sumanth. William's Windows problems led Douglas to propose Mac/Linux as the standard dev OS.
- **Compliance & Security**: Douglas joined Craig Stickel's Secure Development Process discussion, sent Craig the full vendor list (AWS Bedrock is the AI vendor), took on creating the staging pentest accounts, and met Craig on procedures.
- **Agent Identity & super-bmad Tooling**: Douglas proposed that coding agents commit under their own Git/GitHub identity (clariti-surf-agent), with the commit logic in the orchestrator. He also flagged that project-surf is still on super-bmad 0.3.160 without Ankit's QA/finalization changes.
- **Story Scope & Product Questions**: Douglas found the story 25.22 scope mismatch, and Eric approved a narrowed Complete. He shared UX suggestions for 14.3 and posted open questions on EPR module toggling vs. subscription access (57.13 vs. EPR-FR204).
- **Design System**: Douglas and Karan built a plan to get DS component coverage on every sales-demo page using the Surf DS Component Tracker. He also discussed the 3-dots menu divider discrepancy and described his Figma-first component workflow to Shreyansh.

## Key Accomplishments
- Diagnosed three workflow engine failure modes (worker stalls, version-publish breakage, retry exhaustion) and fixed them with bounded retries, which protects the beta's end-to-end flows.
- Confirmed the workflow save fix on Dev after Timothy's walkthrough.
- Shipped the Platform improvements: Temporal console on dev/staging, EKS Metrics Server, sharded ~5-minute PR checks, a single develop/main deploy pipeline, and deploy alerts that link to the source PR.
- Fixed the intermittent Project Surf 502s and a migration-caused 500 crash, and restored CDI CI by fixing its K8S node-replacement permissions.
- Redeployed staging twice for Justin's Internal POC team and documented the self-serve develop → main staging deployment flow.
- Caught the story 25.22 gate/Complete scope bug and got Eric's approval for a shared-scope fix that also protects deferred documents (29.2). 25.22 reached QA by Friday.
- Moved five stories into QA by Friday: 25.22, 98.16, 98.39, 98.50, 98.67.
- Onboarded William Veldhuis and Simone Giacomel, including assigning William his first story (116.1).
- Sent Craig Stickel the Project Surf vendor inventory for compliance.

## Decisions Made
**Workflow Engine & Delivery**
- **Engine fixes over meetings (Wed)**: The stalls and version breakage put the beta at risk.
- **Narrow Complete in 25.22 to the current round, sharing one scope with the gate (Eric McClelland)**: Checking one list and closing another is a bug.
- **Amrita takes 80.21**: This unblocks her 12.26 while Douglas focuses on the engine.
- **Ankit's implementation approved as is**: Permissions, roles and the IdP will be revisited later.

**Compliance & Security**
- **Pentest accounts via generic `pentest+<role>` aliases stored in an RPass vault**: Covers every role and keeps credentials in one place.
- **AWS Bedrock is the AI vendor**: Recorded in the vendor inventory for compliance.

**Tooling & Process**
- **Agents commit under their own identity through the orchestrator (proposed)**: Attribution stays accurate, and humans stay accountable through review and approval.
- **The super-bmad update in project-surf needs no story**: It is a routine update.
- **No meeting needed for staging deployments**: Anyone can already start one through the develop → main PR flow.
- **`_bmad-output/` is the source of truth for new joiners**: `docs/` is out of date.

**Team & Environment**
- **Recommend Mac/Linux as the standard dev OS (proposed)**: Fewer environments to support, simpler scripts, and closer parity with Linux CI/AWS.
- **William stays on WSL until the Linux machines arrive**: Avoids churn.

**Product & Design**
- **Scope EPR to CORE + EPR and CORE + PERMIT + EPR (proposed)**: The Enterprise scenario has no viable connection path yet.
- **Use an existing stylable component (e.g. Radix UI) instead of a custom build**: Less maintenance.
- **Build a DS coverage plan for the sales demo pages**: Tracked in the Surf DS Component Tracker.
- **Infra reference architecture shared as an initial version**: It is expected to change after GA.

## Open Loops (End of Week)
From Friday's daily:
- Samuel to confirm which super-bmad version project-surf should take.
- Samuel to decide on installing Renovate (project-surf PR #4020).
- Samuel/Craig to clarify whether Douglas can sign off DevOps changes from Monday.
- Colin John to confirm he can set up Douglas's 32GB Linux mini PC.
- Karan to decide on the 3-dots menu divider line and whether DESIGN.md needs an update.
- Thom/Karan to respond to the story 14.3 column suggestions.
- Eric/team to resolve module toggling vs. subscription access (57.13 vs. EPR-FR204).
- Timothy/Aseem to triage the 116 items into fix-now and later.
- Blocker: story 10.16 waits on 10.24 (Shreyansh Kumar).

Earlier this week and not confirmed resolved:
- Staging pentest accounts and credentials for Craig (flagged urgent Tue).
- Workflow engine fixes landed and re-tested end to end. Whether the staging invalid form/intake bug (Justin) is fixed is unconfirmed.
- 78.50 re-QA, plus the follow-ups on the error state shown before save and the 109.23 Gate label.
- Merge of 98.18 (blocks Onildo's 98.52).
- Agent identity / commit attribution decision with Samuel.
- Fallback for devs while Project Surf journeys/epics aren't ready, plus the proposal to trim the test suite.
- William's Project Surf AWS access (Colin John) and Figma access (Karan).
- 30-minute BMAD session for Simone, not yet scheduled.
- EKS Metrics Server issue.

**Stale (>5 working days, carried from W43 and not mentioned this week):** Slack webhook for the #cdi-* alert channels, Pulumi typecheck in CI, release promotion plan in the Architecture doc, Samuel's approval of focus-area assignments, and Timothy's data-field shapes for document-generation mapping. Confirm whether these were closed.

## Carried Into Next Week
- Verify the workflow engine fixes end to end on staging and confirm Justin's new-application bug is fixed.
- Create the pentest accounts and RPass vault, then send the credentials to Craig.
- Get 78.50 through re-QA and merge 98.18.
- Pair with Ankit on the super-bmad update once Samuel confirms the version.
- Add agent commits to the orchestrator if attribution is approved.
- Support QA on 25.22, 98.16, 98.39, 98.50 and 98.67, and get the 116 items triaged.
- Unblock 10.16 through 10.24, and continue story 14.3.
- Apply the 3-dots menu hotfix after Karan's decision.
- Walk William through finishing his stories, and schedule Simone's BMAD session.
- Push for a decision on EPR module toggling scope.
- Plan the scheduled Claude job that keeps project documentation up to date.

## Meetings & Collaboration
- 22 meetings attended (6 Mon, 5 Tue, 2 Wed, 6 Thu, 3 Fri). On Wednesday Douglas declined the Progress Check-In and the End of Sprint Demo to work on the engine, and he moved his 1:1 with Ryan Huang to Thursday.
- Recurring: Project Surf Stand-up, Progress Check-In (Samuel, Justin, Ankit), and DS Sync with Karan. One-off: QA Strategy with Aseem, Secure Development/Compliance discussion, CDI/Super Bmad walkthrough, Debug with Justin, procedures meeting with Craig, and Engineering/IT Monthly.
- Key collaborators: Samuel Couture Brochu, Timothy Meyer, Justin LaBrash, Ankit Mittal, Craig Stickel, Karan Kapoor, William Veldhuis, Simone Giacomel, Eric McClelland, Edwin Leong, Onildo Aguiar, Aseem Gupta, Amrita Patra, Shreyansh Kumar, Thom Oguntoyinbo, Ryan Huang, Marnix Faes, Colin John, Tasmia Shefa.

## Data Source Coverage
| Day | Calendar | Gmail | Slack | Drive |
|-----|----------|-------|-------|-------|
| Mon | Used     | Empty | Used  | Empty |
| Tue | Used     | Empty | Used  | Empty |
| Wed | Used     | Empty | Used  | Empty |
| Thu | Used     | Empty | Used  | Empty |
| Fri | Used     | Empty | Used  | Empty |

- **Systemic gap: Gmail returned no data all week** (second week in a row). Check the Gmail connector.
- **Systemic gap: Google Drive returned no data all week** (second week in a row). `google_drive.local_path` is empty in config.yaml.
- **Systemic gap: daily summaries still don't land on `main`.** Each daily was pushed to its own `claude/clever-mayer-*` branch, so cross-day lookback is unreliable (`open_loops_carried` was 0 on Mon, Tue, Thu and Fri).
- All five dailies are rated `quality: partial`.
