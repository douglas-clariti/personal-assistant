---
date: "2026-09-23"
weekday: "Wednesday"
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
  - super-bmad
  - opencode
  - aws
  - infra
  - hiring
  - bmad
---

# Daily Summary — Wednesday, September 23, 2026

## Summary

A Project Surf-heavy day: rolled out super-bmad 0.3.118 to the team, unblocked several teammates on tooling versions (Codex, OpenCode, super-bmad), worked through infra and secrets questions, and ran a full afternoon of meetings including an Applied AI candidate assessment with Justin LaBrash.

- Held "1:1 Ryan - Douglas" with Ryan Huang (organizer), 10:00–10:30 AM EDT (transcript available).
- Invited to "Project Surf Stand-up" organized by Timothy Meyer, 12:30–1:30 PM EDT (transcript available).
- Hosted "Progress Check-In" with Samuel Couture Brochu, Justin LaBrash and Ankit Mittal, 1:30–1:50 PM EDT (transcript not available).
- Attended "Project Surf Infra" with Dipak Parmar (organizer) and Craig Stickel, 2:15–2:30 PM EDT (transcript available).
- Attended "Douglas / Karan - DS Sync" with Karan Kapoor, 2:30–3:00 PM EDT (transcript available).
- Interviewed Manpreet Singh with Justin LaBrash for the Senior Software Developer, Applied AI role (assignment interview/assessment), 3:30–4:30 PM EDT (transcript available).
- Announced super-bmad `0.3.118` in #project-surf-how-we-build (new OpenAI models, code-review phase improvements) and asked developers to update and the wider team to run `/sbmad-setup`.
- Troubleshot tooling for teammates: told Timothy Meyer to update Codex in #project-surf-build, told a teammate in #project-surf-how-we-build to update OpenCode to 2.0.15, and had Onildo Aguiar check `sbmad --version` via DM.
- Created a temporary component in a #project-surf-build thread to help the team.
- Clarified to Ankit Mittal via DM that Grafana is not implemented yet and everything runs on AWS.
- Told Karan Kapoor via DM to have his agent merge `develop` into his worktree for 2454, while still investigating 2473.
- Advised Amrita Patra and Onildo Aguiar in a group DM to confirm whether a secret is needed in GitHub Actions and AWS Secrets Manager, and to have the agent write a script that generates the key and updates AWS.
- Discussed BMAD Loop and model choice with Samuel Couture Brochu via DM, noting missing effort-level control was a blocker and that the BMAD bump after GA will be painful because many skills were removed.
- Committed to taking a look at a new #project-surf-build thread and told Timothy Meyer via DM he could handle a request right away.

## Decisions & Rationale

- **super-bmad 0.3.118 rollout**: Asked the team to upgrade after current work to pick up new OpenAI models and code-review phase improvements.
- **Standardize on current agent tooling versions**: Directed teammates to upgrade Codex/OpenCode (2.0.15) since outdated versions were causing the same issue across multiple people.
- **Script-based secret provisioning**: Recommended Amrita Patra have the agent generate a script that creates the key and updates AWS rather than doing it manually.

## Open Loops

No open loops carried (no summary found within the 10-day lookback window).

- **Karan Kapoor — item 2473**: Still investigating; 2454 pending Karan merging `develop` into his worktree.
- **#project-surf-build thread**: Committed to "take a look" late afternoon — follow-up pending.
- **Secret for GitHub Actions / AWS Secrets Manager**: Waiting on Amrita Patra/agent to confirm where it's needed and produce the provisioning script.
- **Manpreet Singh interview scorecard**: Submit Greenhouse scorecard for the Applied AI assessment.

## Blockers

- Karan Kapoor reported no machine available (from the previous day) — under investigation.

## Next Steps

- Finish investigating 2473 for Karan Kapoor and confirm 2454 after the `develop` merge.
- Follow up on the #project-surf-build thread and the fix promised to Onildo Aguiar.
- Submit the Greenhouse scorecard for Manpreet Singh.
- Confirm the team has upgraded to super-bmad 0.3.118 and run `/sbmad-setup`.

## Transcript Source (Cleaned)

I started the day with my 1:1 with Ryan Huang, then pushed super-bmad 0.3.118 to the team in #project-surf-how-we-build — it brings the new OpenAI models and improvements to the code-review phase — asking developers to update once they finish their current work and everyone else to run the setup command. A good part of the morning went to unblocking people on tooling: Tim needed to update Codex (Onildo hit the same problem and we just had the agent update it), someone else needed OpenCode 2.0.15, and I had Onildo check his sbmad version. I also built a temporary component in #project-surf-build to help the team, and told Ankit that there's no Grafana yet — everything is on AWS.

Around midday I picked up Karan's issues: 2454 should be resolved by merging develop into his worktree, while I'm still digging into 2473 and a report that no machine was available. After the Surf stand-up I ran our Progress Check-In, joined Dipak and Craig for the Project Surf Infra meeting, and had my DS sync with Karan.

In the afternoon I chatted with Samuel about models and BMAD Loop — my tasks are currently more mechanical than prose-heavy, so I'll revisit Opus when I'm back on planning; missing effort-level control in BMAD Loop was a blocker for me, and bumping BMAD after GA will be painful since many skills were removed. I helped Amrita and Onildo with a secret that may be needed in GitHub Actions and AWS Secrets Manager, suggesting the agent write a script to generate the key and update AWS. From 3:30 to 4:30 I interviewed Manpreet Singh with Justin for the Senior Software Developer, Applied AI role, and wrapped up by committing to look at a new #project-surf-build thread and telling Tim I could handle his request right away.
