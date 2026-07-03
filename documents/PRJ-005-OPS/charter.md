---
kind: charter
project: PRJ-005-OPS
id: OPS-charter
title: Portfolio operations 2026-H2 — Project Charter
sponsor: John Tanner
budget:
  amount: 12000
  currency: USD
dates:
  created: 2026-07-03
  target: 2026-12-31   # period end — re-charter for 2027-H1
status: approved
---

## Objective

Operate the PMO as Code ecosystem for the 2026 second half within a bounded
envelope: dependencies current, releases serviced, security posture held,
credentials and domains alive, and known CI failure patterns handled by
runbook, with keep-the-lights-on effort capped so project work stays funded.

## Success Criteria

- Dependabot pull requests merged or dispositioned within 14 days, measured across all eight repositories.
- Confirmed defects receive a patch release within 7 days.
- Security advisories triaged within 48 hours; CodeQL findings at zero or dispositioned.
- Keep-the-lights-on effort at or below 20% of capacity, reported monthly.
- 0 credential, domain, or certificate lapses through 2026-12-31.

## Scope

In scope: dependency triage, patch releases to PyPI, Homebrew, and the action
tags, credential and domain lifecycle (pmoascode.com, tokens, API keys),
Pages and CI health, and the monthly operations status report. Out of scope:
feature work of any kind (the outcome projects), and Refuge product
operations beyond the shared bridge schedules.

## Milestones

- Monthly operations status reports: end of each month, July through December 2026.
- Mid-period review: 2026-09-30.
- Period close and 2027-H1 re-charter: 2026-12-31.

## Risks

- Keep-the-lights-on quietly consumes project capacity. Owner: John Tanner. Mitigation: 20% cap reported monthly; breaches surface in the status report RAG.
- Recurring credentials or domains lapse silently. Owner: John Tanner. Mitigation: lifecycle inventory with renewal dates in the runbook; renewals are service items with due dates.

## Approval

Approved by the sponsor, John Tanner, on 2026-07-03. Budget of USD 12,000
and the target date above are confirmed.
