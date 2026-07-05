---
kind: benefits-realization
project: PRJ-002-ENG
id: ENG-benefits-realization
title: Engine 1.0 — Benefits Realization
owner: johntanner
status: approved
---

## Overview

Tracks the benefits promised by the Engine 1.0 charter now that delivery is
complete: a stable foundation others can build on, governance that runs on
released software, and an engine trustworthy enough to anchor the standard's
public launch. Each benefit is measured by an automated, public artifact
rather than by anyone's assessment.

## Benefits

- Stability adopters can rely on: 0 unversioned breaking changes from
  1.0.0 onward, permanently, enforced by the CLI-surface drift gate and
  SemVer review on every release.
- Governance on released software: 100% of governance repositories run on
  pinned, released engine versions with 0 repo-local engine patches,
  continuously, visible in each repo's workflows and pin file.
- Quality floor that cannot regress silently: test coverage at or above 85%
  on every merge, enforced as a failing CI check rather than a report.
- Launch enablement: the public launch shipped within 1 day of the 1.0.0
  release, 118 days ahead of the 2026-10-31 charter target, through the
  launch gate that 1.0 opened for PRJ-004-ADO.

## Measurement

The stability benefit is measured at every release by the drift gate and
recorded in the changelog's SemVer history; a violation fails the release.
The released-software benefit is measured continuously by the pin files and
bump automation, and the CI-health sentinel lists any repo trailing the
latest release. Coverage is measured on every pull request by the enforced
floor. Realization is reviewed at the monthly PRJ-005-OPS operations
report, which owns these measures from close-out onward.

## Realized Value

As of 2026-07-05: 1.0.0, 1.0.1, and 1.0.2 have shipped with zero breaking
changes; every governance repository pins 1.0.2 with zero engine patches;
coverage holds at or above the enforced 85% floor across Python 3.10–3.14
and Windows; the public launch shipped on the stable engine one day after
1.0.0. The downstream adoption benefit (ten or more adopters by 2026-12-31)
belongs to PRJ-004-ADO and is measured monthly in public, from zero,
at pmoascode.com/self-governance/.
