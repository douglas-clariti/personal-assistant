---
date: "2026-11-02"
weekday: "Monday"
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
  - wiz
  - cnapp
  - soc2
  - branching-strategy
  - staging
  - hiring
  - coderabbit
---

# Daily Summary — Monday, 2026-11-02

## Summary
- Attended **CDI CNAPP & CSPM Tooling Alignment** with Dipak Parmar and Simone Giacomel to discuss security tooling (Wiz) (transcript available).
- Asked Dipak Parmar via Slack DM for elevated Wiz permissions and shared the Wiz container-security board with Simone Giacomel.
- Diagnosed a Project Surf release-build bug in #project-surf-build: the build called the external API URL, which the portal's Content Security Policy blocked; spent ~1h working on the staging fix and deploy.
- Debated with Samuel Couture Brochu (Slack DM) a newly enabled GitHub "branch must be up to date" rule for SOC 2, arguing it serializes merges (8 ready stories ≈ 8h to merge) and risks GA/Beta deadlines.
- Proposed disabling the rule unless compliance-required until journey branching works, and floated splitting the mono repo (possibly via git submodules) so `_bmad-output` changes don't force rebases on `app/`.
- Explained to Samuel that unexpected policy overwrites may come from agents falling back to `sbmad install` (upsert) instead of `sbmad update`.
- Followed up with Eric McClelland in #project-surf-build on whether a test ran on dev, suggesting a call after the daily stand-up.
- Attended **Project Surf Stand-up** (transcript available) and hosted the **Progress Check-In** with Samuel Couture, Justin Labrash and Ankit Mittal (transcript not available).
- Conducted a **Technical Interview** for Aaron Boismier (Senior Software Engineer) with Craig Stickel (transcript available); gave an overall "yes" to Craig Stickel and Samiha Nusrat, with written feedback pending in Greenhouse.
- Attended **CDI Environments** with Dipak Parmar (transcript not available).
- Told Samuel Couture Brochu that CodeRabbit is suspended for now.

## Decisions & Rationale
- **Push back on mandatory up-to-date-branch rule**: Serializing merges in the mono repo would slow the team significantly and threaten this year's GA/Beta; keep it only if strictly required for SOC 2.
- **Fix Project Surf CSP issue and deploy to staging**: Release build's external API calls were blocked by the portal's Content Security Policy.
- **Hiring: "yes" on Aaron Boismier**: Positive technical interview outcome, pending written scorecard.

## Open Loops
- Waiting on Samuel Couture Brochu / compliance on whether the GitHub up-to-date-branch requirement can be disabled until journey branching works.
- 8 ready stories blocked from merging until the branching rule is resolved.
- Wiz permission bump requested from Dipak Parmar — confirm it was granted.
- Confirm with Eric McClelland whether the failing test was run on dev.
- Confirm which position Aaron Boismier applied for and submit the Greenhouse scorecard.

## Blockers
- GitHub branch-up-to-date protection forces serialized rebases/merges, blocking 8 completed stories.

## Next Steps
- Verify the CSP fix on Project Surf staging.
- Submit interview scorecard for Aaron Boismier in Greenhouse.
- Follow up with Samuel on branching strategy (journey branching / possible repo split) and with the team to flag delivery impact of compliance changes early.
- Review Gemini notes from the CNAPP/CSPM alignment and Project Surf stand-up.

## Transcript Source (Cleaned)
I started the day in the CDI CNAPP & CSPM tooling alignment with Dipak and Simone talking about security tools, then asked Dipak to bump my Wiz rights and pointed Simone to the Wiz container-security board. On Project Surf, I found that the release build was calling the external API URL but the portal's Content Security Policy blocked those requests, and I worked on deploying the fix to staging.

I spent a good part of the morning discussing with Sam the new GitHub rule requiring branches to be up to date before merging. I have 8 stories ready and would need to serialize the merges — about 8 hours in the best case — which I think could hurt our GA and Beta this year. I asked whether it's really needed for SOC 2, suggested disabling it until journey branching works, and floated splitting the mono repo, maybe with submodules. I made clear I'm not against compliance, just worried about balancing it with delivery. I also explained that policy overwrites might come from agents using sbmad install instead of sbmad update.

After the Project Surf stand-up I ran my Progress Check-In, then did a technical interview for Aaron Boismier with Craig — overall a yes from me, feedback still to write. I finished with the CDI Environments meeting with Dipak and let Sam know CodeRabbit is suspended for now.
