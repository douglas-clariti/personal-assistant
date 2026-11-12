---
date: "2026-10-30"
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
  - super-bmad
  - dev-environment
  - design-system
  - release-promotion
  - devops
  - epr
  - qa
---

# Daily Summary — Friday, 2026-10-30

## Summary
- Attended **Project Surf Stand-up** (Timothy Meyer, ~18 attendees), **Douglas / Karan – DS Sync** with Karan Kapoor and Tasmia Shefa, and **Engineering/IT Monthly** hosted by Samuel Couture (transcript available — Gemini notes linked on all three).
- Proposed to Samuel Couture via Slack DM that Clariti standardize on Mac/Linux for development (Mac for iOS builds), citing Windows compatibility overhead, and suggested Ansible for provisioning the upcoming Linux dev boxes.
- Advised William Veldhuis to use WSL for now and wait for the Linux machine option, and offered to walk him through finishing his stories (needs Figma access from Karan Kapoor).
- Flagged in #pod-superbmad that project-surf is still on super-bmad 0.3.160 and lacks Ankit Mittal's QA/story-finalization changes (PR #1233), and offered to pair with Ankit on the update.
- Posted QA status in #project-surf-build: stories 25.22, 98.16, 98.39, 98.50 and 98.67 are in QA.
- Shared UX suggestions for story 14.3 (supervisor read-only workload view) with Thom Oguntoyinbo and Karan Kapoor: split "SLA time used" into its own column, use plain "On Track" statuses, and add a sortable "Last Update" column.
- Reviewed Surf-DS Figma with Karan Kapoor over a 3-dots menu alignment/divider-line discrepancy and offered a hotfix plus a DESIGN.md update.
- Recommended to Onildo Aguiar (DM) using an existing stylable component (e.g. Radix UI) instead of building a complex custom one.
- Documented in #project-surf-build the self-serve staging deployment flow (develop → main PR, checks, one approval, merge) for Craig Stickel and Justin LaBrash, and raised semantic versioning as a future topic.
- Posted three open questions on Surf module toggling vs. subscription-based access (story 57.13 vs. PRD EPR-FR204) and proposed limiting scope to CORE + EPR and CORE + PERMIT + EPR for now.
- Asked Samuel Couture to install Renovate for project-surf PR #4020 and offered weekend availability (Sat 5am–1pm, Sun 5am–3pm).

## Decisions & Rationale
- **Recommend Mac/Linux as the standard dev OS**: fewer environments to support, simpler scripts, faster onboarding, closer parity with Linux CI/AWS.
- **William to stay on WSL until Linux machines land**: avoids churn while the Linux box option is still being tested.
- **Super-bmad update in project-surf doesn't need a story**: told Ankit Mittal it's a routine update — run the npx and have Codex open the PR.
- **Prefer an existing UI component over a custom build (Onildo)**: the custom approach is complex and creates heavy maintenance burden.
- **Scope EPR configurations to CORE + EPR and CORE + PERMIT + EPR**: the non-host-company ("Enterprise") scenario has no viable connection path yet.
- **No meeting needed for staging deployments**: the existing PR-based develop → main flow already lets anyone initiate a deploy.

## Open Loops
- Samuel Couture to confirm whether project-surf can take the latest super-bmad or only Ankit's changes.
- Samuel Couture to decide on installing Renovate (re: project-surf PR #4020).
- Clarification pending from Samuel / Craig Stickel on whether Douglas can still sign off DevOps changes from Monday while working across both the DevOps group and dev team.
- Answer pending on whether Colin John can set up Douglas's own 32GB Linux mini PC for dev use.
- Karan Kapoor to decide with/without the divider line on the 3-dots menu (and whether DESIGN.md needs updating).
- Thom Oguntoyinbo / Karan Kapoor to respond on story 14.3 column suggestions.
- Eric McClelland / team to resolve module toggle vs. subscription access conflict (story 57.13 vs. EPR-FR204).
- Timothy Meyer / Aseem Gupta to triage the 116 items to decide fix-now vs. later; some overlap with Karan's work.

## Blockers
- Story 10.16 is blocked on story 10.24 — asked Shreyansh Kumar to prioritize it.
- EPR module work cannot be finished until the module on/off mechanism in Surf is decided.

## Next Steps
- Pair with Ankit Mittal to update super-bmad in project-surf once Samuel confirms the version.
- Apply the 3-dots menu hotfix after Karan's decision; update DESIGN.md if needed.
- Continue story 14.3 incorporating stakeholder feedback.
- Walk William Veldhuis through completing his stories.
- Follow up with Shreyansh Kumar on 10.24 to unblock 10.16.

## Transcript Source (Cleaned)
I started the morning in a DM with Sam about William running into problems developing on Windows. I proposed we standardize on Mac or Linux — Mac for anyone building iOS — since it simplifies scripts, onboarding, and keeps us close to our Linux CI/AWS setup. Sam mentioned Linux machines are being tested, and I suggested an Ansible setup to provision them remotely; I also asked if Colin could set up my own 32GB Linux mini PC. I told William to use WSL for now and wait for the Linux option.

I checked super-bmad in project-surf and found it's still on 0.3.160, without Ankit's QA/story-finalization changes from PR #1233. I flagged it in #pod-superbmad, asked Sam which version to install, and offered to help Ankit do the update — no story needed. I also asked Sam about installing Renovate for PR #4020, offered weekend availability, and asked how sign-off on DevOps changes will work from Monday given I sit in both the DevOps group and the dev team.

In #project-surf-build I posted the stories in QA (25.22, 98.16, 98.39, 98.50, 98.67), suggested UX tweaks for story 14.3 to Thom and Karan, and asked Timothy to triage the 116 items with Aseem's input. With Karan I went back and forth on a Figma divider line on the 3-dots menu. I told Onildo to look for an existing stylable component (maybe Radix UI) rather than building one. I asked Shreyansh to prioritize 10.24 since it blocks my 10.16.

After the Project Surf stand-up (transcript available), I wrote up the self-serve staging deployment process for Craig and Justin, described the image-based deploy pipeline I've used before, and raised semantic versioning as a future topic. I posted three open questions on module toggling vs. subscription access for EPR and proposed sticking to CORE + EPR and CORE + PERMIT + EPR for now. In the afternoon I had my DS Sync with Karan (transcript available) and attended the Engineering/IT Monthly (transcript available).
