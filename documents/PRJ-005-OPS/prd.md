---
kind: prd
id: OPS-prd
project: PRJ-005-OPS
title: Portfolio operations 2026-H2 — Product Requirements
owner: johntanner
status: draft
---

## Overview

The period's service commitments, expressed as requirements until the
operations document kind ships and this project migrates to it.

## Product Requirements

- **OPS-PR-001** (traces: OPS-BR-001): A dependency triage service shall cover all eight repositories, with each Dependabot pull request merged, or closed with a stated reason, within 14 days of opening.
- **OPS-PR-002** (traces: OPS-BR-002): A release service shall ship confirmed defect fixes to PyPI, the Homebrew tap, and the action tags within 7 days, following the release runbook.
- **OPS-PR-003** (traces: OPS-BR-003): A security service shall triage GitHub advisories within 48 hours and keep the CodeQL dashboard clean or dispositioned across the ecosystem.
- **OPS-PR-004** (traces: OPS-BR-001): A credential and domain lifecycle inventory shall list every expiring asset (domain, tokens, API keys, Pages certificates) with renewal dates and runbook steps.
- **OPS-PR-005** (traces: OPS-BR-004): A monthly operations status report shall record service-level attainment, keep-the-lights-on effort against the 20% cap, and period spend against budget.
- **OPS-PR-006** (traces: OPS-BR-002): Known transient CI failure patterns (PyPI propagation lag, Pages deployment flakes) shall have runbook entries with detection and response steps.

## Acceptance Criteria

- **OPS-AC-001** (verifies: OPS-PR-001): Given any Dependabot pull request in the period, when its age is measured, then it was merged or reason-closed within 14 days.
- **OPS-AC-002** (verifies: OPS-PR-002): Given a confirmed defect, when the fix ships, then PyPI, Homebrew, and action tags carry it within 7 days of confirmation.
- **OPS-AC-003** (verifies: OPS-PR-003): Given a security advisory affecting a dependency in use, when 48 hours have passed, then a triage decision is recorded.
- **OPS-AC-004** (verifies: OPS-PR-004): Given the lifecycle inventory, when each asset's renewal date is checked, then none expires without a scheduled renewal step.
- **OPS-AC-005** (verifies: OPS-PR-005): Given each month end, when the status report is read, then service levels, effort against cap, and spend are all stated.
- **OPS-AC-006** (verifies: OPS-PR-006): Given a recurrence of a known CI failure pattern, when the runbook is followed, then the pattern resolves without debugging.

## Out of Scope

New tooling for operations (an ENG concern if needed); on-call commitments;
support service levels for external adopters beyond issue triage.
