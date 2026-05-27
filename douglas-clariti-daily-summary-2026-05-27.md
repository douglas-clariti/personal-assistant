---
date: "2026-05-27"
weekday: "Wednesday"
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
  - kubernetes
  - aws
  - iam
  - rbac
  - infrastructure
  - ai-native
  - clariti
  - claude
---

# Daily Summary — Wednesday, May 27, 2026

## Summary

Spent the morning troubleshooting an AWS Kubernetes RBAC permission error that blocked cluster access, resolved it by identifying a missing Admin role in the IoC configuration with help from Dipak Parmar. Shared AI development resources in the team learning channel, attended the daily sync with Justin LaBrash, and ran the afternoon Progress Check-In (Justin attended; Samuel Couture and Aman Bhalla had a conflict). Later in the day, topped up budget to resolve an API limit hit and asked Justin to retrigger the process.

- Attended "Douglas / Justin Daily" with Justin LaBrash (organizer) via Google Meet, 9:30–9:45 AM EDT (transcript not available).
- Notified Justin LaBrash via DM of 10-minute delay to morning sync.
- Shared two AI development resources in #clariti-eng-ai-native-development-learning: a tweet link and a post from deepswe.datacurve.ai/blog.
- Reached out to Dipak Parmar via DM with AWS Kubernetes RBAC error: "IAM principal doesn't have access to Kubernetes objects on this cluster"; Dipak identified the missing Admin role in the Kubernetes IAM policy.
- Resolved Kubernetes cluster access issue by adding the missing Admin role to IoC configuration.
- Organized and ran "Progress Check-In" at 1:00–1:20 PM EDT with Justin LaBrash via Google Meet; Samuel Couture and Aman Bhalla could not attend (transcript not available).
- Added budget/credits to resolve an API limit issue and asked Justin LaBrash via DM to retrigger the process.

## Decisions & Rationale

- **Kubernetes IAM Admin role added to IoC**: Missing Admin role in the Kubernetes IAM policy was the root cause of cluster access denial; resolved by updating the IoC configuration to include the role rather than a manual one-off fix, keeping infrastructure-as-code consistent.

## Open Loops

- **Expensify access** (carried from 2026-04-17): Awaiting response from accounting@claritisoftware.com to submit train ticket expenses from Lévis offsite. (stale — consider closing or escalating)
- **API retrigger confirmation**: Asked Justin LaBrash to retrigger the process after topping up budget — result not yet confirmed.

## Blockers

- AWS IAM/Kubernetes RBAC access error blocked Kubernetes cluster work for part of the morning (resolved by ~12:03 PM EDT with Dipak Parmar's help).

## Next Steps

- Confirm the retriggered process with Justin LaBrash succeeded after the budget top-up.
- Follow up on or escalate Expensify access with accounting@claritisoftware.com (open since 2026-04-17).
- Continue IoC/infrastructure work now that Kubernetes cluster access is restored.

## Transcript Source (Cleaned)

The day started with the recurring "Douglas / Justin Daily" standup (9:30–9:45 AM EDT), organized by Justin LaBrash over Google Meet; Douglas notified Justin via DM that he would be 10 minutes late. No transcript was linked. Before the meeting, Douglas shared two resources in #clariti-eng-ai-native-development-learning: a tweet and the deepswe.datacurve.ai/blog post.

The bulk of the morning was spent troubleshooting an AWS Kubernetes RBAC issue. Douglas DM'd Dipak Parmar with the error "Your current IAM principal doesn't have access to Kubernetes objects on this cluster — This may be due to the current user or role not having Kubernetes RBAC permissions to describe cluster resources or not having an entry in the cluster's auth config map." Dipak advised that the Admin role needed to be added to the Kubernetes IAM policy. Douglas investigated, found he had forgotten to include the role in his IoC configuration, added it, and resolved the issue by approximately 12:03 PM. He noted frustration with AWS roles ("AWS roles are insane / I miss GCP").

In the afternoon, Douglas organized and ran the "Progress Check-In" (1:00–1:20 PM EDT) with Justin LaBrash via Google Meet. Samuel Couture declined the invite noting a conflict ("aman and i need to attend another meeting, dont wait for us!"); Aman Bhalla was listed as optional and accepted but also could not attend. No transcript was linked.

Later in the afternoon, Justin LaBrash asked Douglas via DM "Did we hit a limit?" — Douglas responded that he had added more money/credits and asked Justin to have Claude retrigger the process.
