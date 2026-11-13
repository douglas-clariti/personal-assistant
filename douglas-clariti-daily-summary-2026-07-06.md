---
date: "2026-07-06"
weekday: "Monday"
author: "douglas-clariti"
quality: "complete"
sources_used:
  - google_calendar
  - slack
sources_empty:
  - gmail
  - google_drive
open_loops_carried: 1
tags:
  - project-surf
  - super-bmad
  - sbmad-change
  - pr-review
  - bmad
  - claude-code
  - all-hands
  - q3-kickoff
  - telemetry
---

# Daily Summary — Monday, July 6, 2026

## Summary

A busy first day of the week marked by PR cleanup, process clarification in #project-surf-build, five meetings (including company and R&D all-hands), a confidential heads-up from Samuel about organizational changes, and a Claude Code tooling blocker escalated to Clariti admin.

- Attended "Douglas / Justin Daily" with Justin Labrash (organizer), 10:15–10:30 AM EDT; brief call connection issue noted at the start (transcript available).
- Opened PR #467 on project-surf removing legacy files from the super-bmad design that were missed during migration; requested review from Karan Kapoor, Onildo Aguiar, and Justin Labrash in #project-surf-build; Justin approved merge ("looks fine if it's not in the app let's merge it").
- Clarified the /sbmad-change workflow in #project-surf-build (for Timothy Meyer, Craig Stickel, Onildo Aguiar): run it for new behavior or additions; bug-fixes matching existing spec are exempt; when in doubt, run it anyway.
- Determined that Craig Stickel's "activation as first-class audited event" finding is new behavior, not a bug-fix — requires /sbmad-change to trigger correct-course updating PRD + Story 1.4 and to capture the 2.12 break-glass gap; Craig's quick dev on P-AUDIT was compliant and stands.
- Attended "Project Surf Stand-up" organized by Timothy Meyer, 11:30 AM–12:30 PM EDT, with Edwin Leong, Karan Kapoor, Eric McClelland, Thom Oguntoyinbo, Craig Stickel, Aman Bhalla, Justin Labrash, Samuel Couture (transcript available).
- Posted in #pod-superbmad about new BMAD v6.10 release; flagged it may affect the human orchestration plan and scheduled a review for after lunch.
- Reported a Claude Code artifact publishing blocker to Colin John (Clariti admin) via DM: "publish denied: Artifact publishing is disabled for your user by organization policy" despite the org Artifacts toggle being ON, failing since Jul 3; provided a ranked diagnostic of four potential causes (role permission top suspect); Colin to follow up tomorrow.
- Received a confidential heads-up from Samuel Couture Brochu (DM): company layoffs today (non-Surf), Clariti now profitable after exits; Q3 quarter kickoff tomorrow will announce the consolidated Surf roadmap (Midmarket + Enterprise + Civcheck).
- Hosted "Progress Check-In" with Justin Labrash, Samuel Couture Brochu, and Aman Bhalla (optional), 1:00–1:20 PM EDT; shared Onildo Aguiar's delivery stats (30 stories, 8 features); noted burn rate concern and flagged telemetry fix in progress (transcript available).
- Attended company-wide "All Hands Meeting" organized by CEO Cyrus, 1:15–1:30 PM EDT, addressing the day's organizational restructuring (transcript available).
- Attended "R&D All Hands" organized by Samuel Couture Brochu, 1:30–2:00 PM EDT, with Surf team (transcript not available).

## Decisions & Rationale

- **PR #467 merged — legacy super-bmad design file cleanup**: Removed files missed during migration; not present in the live app, so Justin approved the merge without requiring a full review cycle.
- **/sbmad-change workflow rule codified**: Established in #project-surf-build that new/changed behavior requires /sbmad-change; fixing code to match what the spec already says is exempt; "when in doubt, run it" as the tiebreaker.
- **"Activation as first-class audited event" routed through /sbmad-change**: Ruled this is a new audit taxonomy addition (not a fix), so it triggers correct-course to update PRD + Story 1.4 and absorbs the 2.12 break-glass gap as tracked work; Craig's existing quick dev stands as-is.

## Open Loops

- **Expensify access** (carried from 2026-04-17): Requested from accounting@claritisoftware.com to submit Lévis offsite travel expenses — no response on record. (stale — consider closing or escalating)
- **Claude Code artifact publishing blocked**: Escalated to Colin John (Clariti admin) today; awaiting investigation of role permission and managed settings; failing since Jul 3.
- **BMAD v6.10 review pending**: Announced in #pod-superbmad; needs review for potential impact on human orchestration plan.
- **Telemetry fix in progress**: Fixing telemetry to clarify reported burn rate discrepancy flagged during the Progress Check-In.

## Blockers

- Claude Code artifact publishing disabled for Douglas's user by organization policy despite the org Artifacts toggle being ON (error: "publish denied: Artifact publishing is disabled for your user by organization policy"; failing since Jul 3); Colin John (Clariti admin) to investigate and follow up tomorrow.

## Next Steps

- Follow up with Colin John on Claude Code artifact publishing fix (expected tomorrow).
- Review BMAD v6.10 release for impact on the human orchestration plan.
- Attend Q3 quarter kickoff tomorrow — consolidated Surf roadmap (Midmarket + Enterprise + Civcheck) announcement organized by Samuel and Aman.
- Complete telemetry fix to get accurate burn rate data for the team.
- Craig Stickel to run /sbmad-change with the audit taxonomy finding; confirm Story 1.4 and 2.12 break-glass gap are tracked.
- Consider closing or escalating the Expensify access request (stale since April 2026).

## Transcript Source (Cleaned)

Douglas started Monday (his birthday) with the recurring "Douglas / Justin Daily" check-in at 10:15 AM EDT organized by Justin Labrash. The call had a brief connection issue — Douglas noted "you are frozen" — before they moved into a discussion about PR #467 on the project-surf repo. Douglas had been cleaning up legacy super-bmad design files and shared the PR link with Justin; Justin confirmed the files weren't in the app and approved the merge.

In #project-surf-build, a thread started by Timothy Meyer asked whether Craig Stickel's quick dev on audit behavior needed to go through the /sbmad-change process. Douglas weighed in, giving the team a clear rule of thumb: new or changed behavior → run /sbmad-change; fixing code to match what the spec already says → exempt; when in doubt, run it anyway. He confirmed Craig's quick dev on P-AUDIT was the second kind (the spec already required the audit record) and was fine. However, "activation as first-class audited event" is new taxonomy and requires /sbmad-change, which will fire correct-course to update the PRD and Story 1.4 and also capture the 2.12 break-glass gap. Douglas also told Karan Kapoor to post any design problems on the public channel so he can address super-bmad issues there.

The Project Surf Stand-up ran 11:30 AM–12:30 PM EDT, organized by Timothy Meyer. Later in #pod-superbmad, Douglas announced a new BMAD v6.10 release, noting it might affect the human orchestration plan and that he'd review it after lunch.

Around 12:30 PM, Samuel Couture Brochu sent Douglas a confidential DM disclosing company-wide layoffs (not Surf-related), confirming Clariti is now profitable after the exits, and previewing tomorrow's Q3 quarter kickoff where the consolidated Surf roadmap (Midmarket + Enterprise + Civcheck) would be announced company-wide. Douglas acknowledged the news.

Douglas also messaged Colin John (Clariti admin) with a detailed diagnostic about a Claude Code blocker: artifact publishing from Claude Code fails with "publish denied: Artifact publishing is disabled for your user by organization policy" despite the org Artifacts toggle being ON, failing since Jul 3. He outlined four ranked causes (role permission top suspect, then prerequisite capabilities, managed settings JSON, data policies) and provided his account and org UUIDs. Colin said he'd follow up the next day.

The afternoon included the "Progress Check-In" hosted by Douglas at 1:00 PM EDT with Justin, Samuel, and Aman. Douglas shared that Onildo Aguiar had already delivered 30 stories and 8 features; he flagged a potential burn rate concern and noted he was fixing telemetry to clarify the data. The day closed with two all-hands: the company-wide All Hands at 1:15 PM EDT called by CEO Cyrus to address the restructuring, and the R&D All Hands at 1:30 PM EDT organized by Samuel with the Surf team.
