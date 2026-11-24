---
date: "2026-11-24"
weekday: "Tuesday"
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
  - sales-int
  - sentry
  - error-handling
  - observability
  - esri
  - code-review
---

# Daily Summary — Tuesday, 2026-11-24

## Summary
- Douglas held the 1:1 with William Veldhuis on Google Meet at 11:00 (transcript available).
- Douglas attended the Project Surf Stand-up hosted by Timothy Meyer at 12:30 (transcript available).
- Douglas ran the Progress Check-In with Samuel Couture, Justin Labrash and Ankit Mittal at 13:30 (transcript not available).
- In #project-surf-build, Douglas asked Timothy for the record ID, workflow, endpoint and user action behind the recurring 503/500 errors on sales-int, and said he would check the staging logs.
- Douglas told the #project-surf-build thread that he had already corrected some 500 errors that used the wrong status code, and that he has a task to rewrite the error-response schema.
- Douglas backed Dipak Parmar's plan to set up Sentry (US region, dev cluster first), and Dipak opened PR #5492 for his review.
- Douglas approved Dipak's manual-run evidence PR #5509 in #project-surf-build.
- Douglas asked Timothy which story would fix the sales-int portal-submit 500 (fees saved without a currency because finance settings were missing), then struck the question out; Timothy later opened PR #5538.
- In a DM, Douglas told Dipak to keep the `trace_parent` column because the choice is easy to reverse.
- In a DM, Douglas told Onildo Aguiar that a UI walkthrough had been requested before Onildo implements the feature, and mentioned that Simone Giacomel is looking at an issue.
- Douglas shared webmcp.sh in #tech-learn-and-share after asking Dipak which channel to use for tech articles.

## Decisions & Rationale
- **Keep the `trace_parent` column**: it is easy to reverse, and more trace fields can be added or moved later if needed.
- **Set up Sentry now (US region, dev cluster only)**: dev bugs on Project Surf need visibility right away. CA data residency (self-hosting or an EU region) and the staging/prod rollout are deferred.
- **Approved PR #5509** (Dipak's manual-run evidence).

## Open Loops
- Review Dipak's Sentry PR #5492 (clariti-labs/project-surf).
- Find the root cause of the recurring 503/500 errors on sales-int and staging; waiting on Timothy for the request details (record ID, workflow, endpoint, user action).
- Timothy's PR #5538 for the sales-int finance-settings/currency fix is waiting for review from Dipak (and later Edwin Leong).
- Rewrite the API error-response schema and audit the remaining wrong 5xx status codes.

## Blockers
- None reported today. Application intake on sales-int was blocked, but Dipak unblocked it with the Esri `geometryServiceUrl` hand-fix and by activating finance settings.

## Next Steps
- Review and approve Sentry PR #5492.
- Check the staging logs for the 503 errors.
- Continue the error-response schema rewrite and the 5xx status-code cleanup.
- Follow up with Onildo on the UI walkthrough before implementation.

## Transcript Source (Cleaned)
I started the day with my 1:1 with William, then joined the Project Surf stand-up with Timothy and the wider team, and afterwards ran our Progress Check-In with Samuel, Justin and Ankit. Gemini notes were attached to the 1:1 and the stand-up.

Most of my Slack time went to the #project-surf-build thread about the recurring 503/500 errors on sales-int. I asked Timothy for the concrete details I need to debug them: the record ID, the workflow, the endpoint and what the user was trying to do. I explained that I had already corrected some 500s that used the wrong status code, that the error-response schema needs a rewrite (I have a task for it), and that I'll dig into the staging logs. Dipak proposed setting up Sentry right away for the dev cluster in the US region, and I strongly agreed. He then opened PR #5492 for my review. I also approved his manual-run evidence PR #5509. On the separate portal-submit 500, which came from missing finance settings and fees saved without a currency, I asked which story would cover the fix, and Timothy has since opened PR #5538.

In DMs, I told Dipak to keep the `trace_parent` column because it's an easy choice to reverse. I told Onildo that a UI walkthrough had been requested before he implements, and mentioned that Simone was looking at an issue. I helped Marnix Faes with an OpenAI link that works when you log in with your Clariti account. I also shared webmcp.sh in #tech-learn-and-share.
