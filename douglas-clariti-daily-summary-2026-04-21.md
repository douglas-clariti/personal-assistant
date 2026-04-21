---
date: "2026-04-21"
weekday: "Tuesday"
author: "douglas-clariti"
quality: "complete"
sources_used:
  - google_calendar
  - gmail
  - slack
sources_empty:
  - google_drive
open_loops_carried: 1
tags:
  - project-surf
  - super-bmad
  - soc2
  - expensify
  - onboarding
  - clariti-labs
  - cloud-vendor
  - github
---

# Daily Summary — Tuesday, April 21, 2026

## Summary

Active second week at Clariti: attended four meetings including a SOC2 controls kick-off and the Product, Design & Engineering All Hands, resolved the pending Expensify access issue via Fiona Runa, merged PR #12 in the super-bmad repo, announced a temporary Project Surf repo migration to the clariti-labs GitHub org, and contributed to the cloud vendor comparison doc review with Justin LaBrash.

- Attended "kick-off discussion on SOC2 controls" organized by Colin John with Justin LaBrash via Google Meet, 11:00–11:30 AM EDT (transcript not available).
- Organized and attended "Progress Check-In" with Samuel Couture, Justin LaBrash, and Aman Bhalla (optional) via Google Meet, 1:00–1:20 PM EDT (transcript not available).
- Attended "ONBOARDING: Self-guided Enterprise Sales Demo" (P&T Team Calendar, self-paced recording with linked Drive video), 2:00–3:00 PM EDT.
- Attended "Product, Design & Engineering All Hands" organized by Aman Bhalla, 4:00–5:00 PM EDT (transcript not available).
- Followed up with Fiona Runa (HR) via DM about pending Expensify access; Fiona escalated to Julie Hossain and Jari Kubica (payroll), who confirmed Douglas will be added to Expensify before end of week for next payroll — resolving the open loop from 2026-04-17.
- Reached out to Herman Chan via DM for an intro 1:1; Herman confirmed open calendar availability.
- Herman Chan provided a detailed Project Surf tech-stack recommendation via DM covering WorkOS (authz), Temporal.io (workflow), customizable server-driven UI, flexible data model, PostHog (o11y), GIS ingestion, cell-based architecture, GraphQL, and MCP/A2UI agent support; Douglas acknowledged and committed to reviewing the tools.
- Announced migration of all Project Surf repos to github.com/orgs/clariti-labs in #project-surf-how-track; confirmed using Clariti Gmail accounts only with Samuel Couture added as org member; decision is temporary pending alignment with Dipak before moving under claritisoftware org.
- Asked for and received Justin LaBrash's approval to merge PR #12 in super-bmad (clariti-labs/super-bmad/pull/12); Justin granted repo access and confirmed merge.
- Reviewed Justin LaBrash's cloud vendor comparison v2 doc via DM; suggested additions: AWS vs Azure tiebreaker, cost/TCO comparison, VPC/VNet isolation, and AI/ML managed services; expressed no strong opinion on retaining a Vercel hybrid frontend option.
- Sent two outbound emails (14:51 and 14:58 EDT) — one to Samuel Couture, one to Justin LaBrash, Samuel Couture, and Aman Bhalla; bodies not captured (signature-only content visible in both threads).

## Decisions & Rationale

- **Project Surf repos migrated to clariti-labs GitHub org (temporary)**: All repos moved to github.com/orgs/clariti-labs under Clariti Gmail accounts; agreed as temporary until alignment with Dipak on whether to migrate to claritisoftware org for CodeRabbit integration and unified management.
- **PR #12 merged in super-bmad**: Merge approved by Justin LaBrash after confirming repo access; closes the baseline PR for this sprint iteration.
- **Skill removed from super-bmad system**: Proposed and agreed with Justin to remove the human-override skill as low-value for now; agreed it can be added back later.
- **Cloud vendor doc additions requested**: Douglas requested AWS vs Azure tiebreaker, cost/TCO, VPC/VNet isolation, and AI/ML managed services sections to be added to Justin's v2 vendor comparison; Justin will update.

## Open Loops

- ~~**Expensify access**~~ (carried from 2026-04-17) → **RESOLVED**: Fiona Runa escalated to Julie Hossain and Jari Kubica; confirmed Douglas will be added to Expensify before end of week so train ticket expenses from the Lévis offsite can be submitted for next payroll.
- **clariti-labs → claritisoftware org migration**: Awaiting alignment with Dipak (not yet aware of Project Surf) before migrating repos to the claritisoftware org; Samuel Couture flagged this as a blocker for the permanent move.
- **Cloud vendor comparison doc update**: Justin LaBrash to add AWS vs Azure tiebreaker, TCO, VPC isolation, and AI/ML services per today's discussion.
- **Intro 1:1 with Herman Chan**: Herman confirmed open calendar; meeting not yet booked.

## Blockers

No blockers identified today.

## Next Steps

- Book intro 1:1 with Herman Chan (calendar is open per DM).
- Review Project Surf tech-stack tools recommended by Herman Chan: WorkOS, Temporal.io, PostHog, server-driven UI (React/React Native), GraphQL, MCP/A2UI agent framework.
- Await Dipak alignment before migrating clariti-labs repos to claritisoftware org; coordinate with Samuel Couture and Herman Chan.
- Complete self-guided Enterprise Sales Demo onboarding recording (P&T assigned session).
- Review cloud vendor comparison doc v2 once Justin LaBrash updates with requested additions.
- Continue sprint week rhythm: daily standups, Friday review, and sprint planning (per April 17 plan).

## Transcript Source (Cleaned)

Tuesday April 21 was Douglas's second week at Clariti and a full sprint-week day. The morning opened with the SOC2 controls kick-off (11:00–11:30 AM) organized by Colin John, attended with Justin LaBrash — no transcript linked. Douglas then ran his own "Progress Check-In" at 1:00 PM with Samuel Couture, Justin LaBrash, and optionally Aman Bhalla — no transcript linked. The afternoon included the self-guided ONBOARDING: Enterprise Sales Demo session (2:00–3:00 PM), a self-paced recording linked from the calendar event (Drive link in description). The day closed with the Product, Design & Engineering All Hands (4:00–5:00 PM) organized by Aman Bhalla — no transcript linked.

On Slack, the morning started with Douglas following up via DM with Fiona Runa (HR/onboarding) about the still-pending Expensify access — he had emailed Accounting on Friday April 17 with no response. Fiona escalated directly to Julie Hossain and Jari Kubica (payroll) via Slack; they confirmed Douglas would be added before end of week so he can expense the Lévis offsite train tickets by next payroll. The open loop from April 17 is now resolved.

Also in the morning, Douglas reached out to Herman Chan (engineering) via DM to schedule an intro 1:1 after a week without meeting; Herman confirmed his calendar was open. Later, Herman shared a detailed technical architecture recommendation for Project Surf in the same DM thread, covering nine building blocks: WorkOS for authz, Temporal.io for workflow orchestration, a server-driven UI / CMS-style frontend (React + React Native), a flexible/customizable data model, PostHog for observability, a GIS ingestion layer, cell-based architecture, GraphQL for frontend APIs, and MCP/A2UI integration for agents. Douglas acknowledged and committed to reviewing the recommended tools.

In #project-surf-how-track at ~3 PM, Douglas announced the migration of all Project Surf repos to github.com/orgs/clariti-labs, confirming the org is under Clariti Gmail accounts with Samuel Couture added as org member (no personal users). Herman Chan suggested moving under the claritisoftware org instead for CodeRabbit access and unified management. Samuel Couture noted the migration is temporary — alignment with Dipak is needed first as he is not yet aware of Project Surf.

Via DM with Justin LaBrash throughout the afternoon, Douglas asked for and received approval to merge PR #12 in super-bmad (Justin merged it and granted repo access), and reviewed Justin's cloud vendor comparison v2 doc. Douglas suggested adding an AWS vs Azure tiebreaker, cost/TCO, VPC isolation, and AI/ML managed services comparison. On the Vercel hybrid option (frontend Vercel + other backend), Douglas had no strong opinion. Douglas also proposed removing a human-override skill from the system; Justin agreed it is low-value now and can be reinstated later.

Two outbound emails were sent in the afternoon (14:51 and 14:58 EDT) — one to Samuel Couture, one to Justin LaBrash, Samuel Couture, and Aman Bhalla — but both contained only signature-block content; no substantive bodies were captured.
