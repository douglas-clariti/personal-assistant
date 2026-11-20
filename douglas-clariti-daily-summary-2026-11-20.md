---
date: "2026-11-20"
weekday: "Friday"
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
  - audit-history
  - citizen-portal
  - backoffice-roles
  - hiring
  - wiz
  - sprint-planning
---

# Daily Summary — Friday, 2026-11-20

## Summary
- Douglas attended Wiz onboarding with Dipak Parmar on Google Meet, after asking in a Slack DM to move it to 11:40 (transcript available).
- Douglas attended the Project Surf Stand-up hosted by Timothy Meyer with the wider Surf team (transcript available).
- Douglas attended Surf Build Sprint Planning hosted by Timothy Meyer, where the audit-history follow-up and Story 0.124 were due for prioritization (transcript available).
- Douglas agreed in #project-surf-build that Ankit Mittal's remaining audit-history follow-up and Story 0.124 (pre-deploy checks and scheduled alerts) should move to Ryan Huang or another available engineer, and asked Timothy Meyer and Thom Oguntoyinbo to help reassign them.
- Douglas took on Karan Kapoor's two fixes for story 113.25 in #project-surf-build: exclude drafts from the attention summary (`listOwnApplicationSummary`) and right-align the bell notice's View button.
- Douglas began investigating why the `assign-activity` role does not appear in Backoffice after Tasmia Shefa asked for it on her dev account.
- Douglas gave Marnix Faes feedback on a candidate: acceptable if the role must be filled now, but better to wait and evaluate others.
- Douglas asked Marnix Faes to move their Workflows conversation to Monday so he could focus on fixes today.
- Douglas referred a friend (recently granted Canadian PR) for an open role, sent his LinkedIn to Samuel Couture Brochu, then sent the details to Samiha Nusrat and completed the referral form.

## Decisions & Rationale
- **Reassign audit-history follow-up and Story 0.124 away from Ankit Mittal**: Ankit asked to focus on sbmad discovery, so Douglas suggested Ryan Huang or another available engineer.
- **Postpone Workflows discussion with Marnix Faes to Monday**: Douglas needed today for urgent fixes.
- **Candidate recommendation to Marnix Faes**: hire only if the role is urgent; otherwise keep evaluating candidates.

## Open Loops
- Audit-history follow-up and Story 0.124 still need a new owner and a priority. Thom Oguntoyinbo noted that 0.124 is not in sprint 12, and Timothy Meyer asked what these items block.
- The `assign-activity` role is missing from Backoffice. Tasmia Shefa is waiting on it to test the review flow.
- Story 113.25 fixes from Karan Kapoor: draft exclusion from attention counts and View button alignment.
- Referral of Douglas's friend is with Samiha Nusrat and Samuel Couture Brochu, awaiting next steps.
- Dipak Parmar is still compiling the dev audit recovery notes in PR #5277.

## Blockers
- Tasmia Shefa cannot test stories that need the review flow until the `assign-activity` permission is available on her dev account.

## Next Steps
- Ship the two 113.25 fixes (drafts counted as needing attention; View button alignment) and ask Karan Kapoor to recheck on dev.
- Find out why `assign-activity` is not mapped in Backoffice roles and grant it to Tasmia Shefa.
- Confirm the new owner and sprint placement for the audit-history follow-up and Story 0.124.
- Hold the Workflows conversation with Marnix Faes on Monday.

## Transcript Source (Cleaned)
I started the morning on hiring. Marnix and I discussed a candidate. I said he'd be okay if we really need to fill the role now, but it would be better to wait and evaluate others. I also asked Marnix to move our Workflows conversation to Monday because I had fixes to finish today. I referred a friend who just got his Canadian PR. I sent his LinkedIn to Sam, and after Sam pointed me to Samiha, I sent her the details and filled out the referral form.

In #project-surf-build, Ankit asked whether the remaining audit-history follow-up from the dev migration failure, plus Story 0.124 for pre-deploy checks and scheduled alerts, should go to someone else so he can focus on sbmad discovery. I agreed it should move to Ryan Huang or whoever is available, and I asked Timothy and Thom to help. Thom said we'd prioritize it at sprint planning, since 0.124 isn't in sprint 12. Karan checked 113.25 on dev and asked for two fixes: drafts should not count as needing attention, and the View button in the bell notice should be right-aligned. I said I was on it.

I asked Dipak to push our Wiz onboarding to 11:40, and we did it then. After that I attended the Project Surf stand-up and the Surf Build sprint planning. In the afternoon, Tasmia asked me for the `assign-activity` permission on her dev account. The role isn't showing in Backoffice, so I started checking whether it's mapped to the roles we want. She can't test the review flow until this is fixed.
