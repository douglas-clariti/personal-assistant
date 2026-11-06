---
week: "2026-W45"
date_range: "2026-11-02 to 2026-11-08"
author: "douglas-clariti"
days_covered: 5
days_expected: 5
days_missing: []
tags:
  - project-surf
  - wiz
  - cnapp
  - soc2
  - branching-strategy
  - staging
  - hiring
  - coderabbit
  - surf-compliance
  - pen-test
  - pen-testing
  - cdi
  - ci
  - super-bmad
  - telemetry
  - staging-release
  - ci-cd
  - aws
  - conditions
  - flags
  - dashboard
  - qa
  - rpass
  - design-system
  - core-beta
  - api-docs
  - workos
  - release-80.21
  - sla-alerts
  - deploy
  - ooo
---

# Weekly Rollup — 2026-W45

**2026-11-02 to 2026-11-08** | **5/5 days covered**

## Themes & Focus Areas
- **Staging release pipeline**: The first full pass through the release workflow fixed Git auth (PR #4385). It then stalled on missing AWS IAM/OIDC config (`SURF_RELEASE_ROLE_ARN` and others), and the AWS-account side was handed to Dipak. Staging cadence was set to Wednesday and Friday at end of day.
- **SOC 2 compliance vs. delivery speed**: Douglas pushed back on GitHub's mandatory "branch up to date" rule, which serializes merges, and floated splitting the repo. He flagged two audit-log gaps (the Super BMAD ruleset change and the CodeRabbit suspension), and CodeRabbit is suspended for now.
- **Pen-test support**: Set up the "CDI Pen Test Users" secret, refreshed the test accounts and added "Pen Test Citizen Two" for multi-tenancy testing. Answered vendor questions in #surf-compliance. A second-org tenant has to wait for the staging + Lakewood cell work.
- **Product scope trimming (Project Surf)**: Paused the supervisor dashboard (14.3), set ~85% design match as the bar for UI stories, built the simplest beta of record flags (10.16), and pushed for a simplified V1 of Conditions.
- **Core-beta delivery & QA**: Pushed 80.21, 98.56 and 98.49 toward completion. 80.21 reached QA, and Thom took over its dev validation (with SLA test scripts) while Douglas was OOO on Friday.
- **CI/infra reliability**: Debugged a CI timeout where the aws-node DaemonSet never became ready. Asked Dipak to migrate the deprecated Pulumi S3 BucketV2 resources, and published internal API docs at api.dev.clariticdi.com/docs.
- **Hiring**: Gave a "yes" on Aaron Boismier (Senior Software Engineer) after the technical interview with Craig Stickel.

## Key Accomplishments
- Fixed the Project Surf release-build CSP bug (the external API URL was blocked by the portal) and worked through its staging deploy.
- Fixed the release workflow's Git authentication failure (PR #4385). Sent Dipak a written status and an HTML dependency graph for Story 9.27.
- Got agreement with Thom on scope cuts (14.3 paused, 85% UI match, simplest record-flags beta) to protect beta timelines.
- Set up pen-test infrastructure: credentials secret, a second test citizen, real-name fake accounts and clear usage guidance, so the vendor can test multi-tenancy.
- Published internal API documentation for the team (api.dev.clariticdi.com/docs).
- Moved release 80.21 into QA and arranged coverage for dev testing (Thom) and deploy monitoring (Onildo) before going OOO.
- Pointed the team to the shared staging-admin/implementer RPass accounts and widened manager access (Simone).
- Raised the delivery cost of the SOC 2 branching rule early (8 ready stories ≈ 8h of serialized merges) and proposed alternatives.

## Decisions Made
**Compliance & process**
- **Push back on the mandatory up-to-date-branch rule**: Serialized merges threaten GA/Beta; keep the rule only if SOC 2 strictly requires it.
- **CodeRabbit suspended for now**: Communicated to Samuel and flagged as missing from the audit log.

**Release & infra**
- **Staging deploys Wednesday and Friday at end of day**: Holds until the PMs say otherwise.
- **Hand AWS-account release testing to Dipak**: He is already provisioning the accounts.
- **Bundle Justin's fix with the loops fix before the staging deploy**: Validate both in dev first, then deploy together.
- **Super BMAD telemetry stays in the repo for now**: It will move to a dedicated server later.

**Product scope**
- **Pause the supervisor dashboard (14.3) and close its PR**: It may duplicate the user dashboards; Thom is checking with Tim and Ken.
- **Accept UI stories at ~85% design match**: AI agents can't match font weights and spacing exactly, so chasing 100% causes endless rounds.
- **Simplest beta for record flags (10.16)**: Testing every record-locking edge case costs too much in QA/CI.
- **Simplified Conditions V1 (block only the next phase/issuance)**: Covers ~80% of use cases. The final model waits for the sales Salesforce-flow review.
- **Tabs are not a design-system component**: The 14.3 tabs Douglas already merged need follow-up.

**Pen test**
- **Pen testers use Clariti-provided credentials**: The team can monitor the logs and act on findings.
- **Second pen-test org deferred**: Needs a second tenant, which depends on the staging + Lakewood cell work.

**Release 80.21 / OOO coverage**
- **Thom owns 80.21 dev validation; Onildo monitors the deploy**: Douglas was OOO Friday afternoon.

**Hiring**
- **"Yes" on Aaron Boismier**: Positive technical interview; written scorecard pending.

## Open Loops (End of Week)
- Confirmation from Onildo that the project-surf `app-deploy.yml` run for 80.21 succeeded.
- Thom to create clock rules and send links so Douglas can seed the SLA test records.
- Tasmia Shefa's request, which Douglas committed to handle on Monday.
- Staging release still blocked on Dipak/DevOps for `SURF_RELEASE_ROLE_ARN`, the push role, the store bucket, OIDC trust and the signing setup (carried since Wed).
- QA pending from Timothy/Thom on 80.22, 10.16 and 98.55 (carried since Thu).
- PR reviews pending: super-bmad #1251 (Samuel), project-surf #4048 (Onildo), #4340 (Timothy) (carried since Wed).
- Thom to confirm with Tim and Ken whether 14.3 is a duplicate, and to share sales Conditions examples and a demo (carried since Wed).
- Not mentioned again after Monday/Tuesday, so status unknown: Aaron Boismier's Greenhouse scorecard, the Wiz permission bump, Eric McClelland's dev test, the SOC 2 branching-rule outcome, the CI aws-node DaemonSet fix, sharing the API spec with the pen testers, and Aman Bhalla's pending item.
- No item has been open for more than 5 working days yet. The Monday items above reach that threshold early next week.

## Carried Into Next Week
- Handle Tasmia Shefa's request (Monday).
- Confirm the 80.21 deploy and seed the SLA test records once Thom's clock rules exist.
- Finish the staging release once Dipak provisions the AWS roles and accounts, then run the Lakewood/Southampton staging checks and the #surf-compliance item.
- Set up the second-org pen-test account once the Lakewood cell is live.
- Follow up on the 14.3 tabs vs. design-system mismatch, close the 14.3 PR, and schedule the dashboard follow-up.
- Audit and close the redundant 98-series stories in QA (~5 are actually needed).
- Submit Aaron Boismier's Greenhouse scorecard (verify).
- Review the Gemini notes from Friday's missed Sprint Planning, Stand-up and Release Demo, and from Tuesday's Steerco.
- Remove the unused native.demo account after confirming with Simone.

## Meetings & Collaboration
- About 13 meetings attended (Mon 5, Tue 1 accepted while sick, Wed 4, Thu 3, Fri 0 while OOO). Several more were declined on Tue and Fri.
- Key collaborators: Samuel Couture Brochu, Dipak Parmar, Thom Oguntoyinbo, Justin LaBrash, Craig Stickel, Onildo Aguiar, Timothy Meyer, Simone Giacomel, Ankit Mittal, Karan Kapoor, Eric McClelland, Aseem Gupta, Marnix Faes

## Data Source Coverage
| Day | Calendar | Gmail | Slack | Drive |
|-----|----------|-------|-------|-------|
| Mon | ✓ | empty | ✓ | empty |
| Tue | ✓ | empty | ✓ | empty |
| Wed | ✓ | empty | ✓ | empty |
| Thu | ✓ | empty | ✓ | ✓ |
| Fri | ✓ | empty | ✓ | empty |

**Systemic gaps:** Gmail returned no data all week, so check the connector. Google Drive returned data only on Thursday. All five dailies are marked `quality: partial`. The daily summaries were pushed to separate `claude/clever-mayer-*` branches and are not merged to `main`.
