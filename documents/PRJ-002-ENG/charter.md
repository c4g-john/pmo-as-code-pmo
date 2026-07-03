---
kind: charter
project: PRJ-002-ENG
id: ENG-charter
title: Engine 1.0 — Project Charter
sponsor: John Tanner
budget:
  amount: 12000
  currency: USD
dates:
  created: 2026-07-03
  target: 2026-10-31   # proposed — confirm at review
status: draft
---

## Objective

Ship docassert 1.0: a stable engine whose remaining pre-1.0 scope is exactly
the set of needs discovered by running PMO as Code on real portfolios — the
per-project bridge, risk disposition, and operations governance — backed by a
published stability and deprecation policy.

## Success Criteria

- docassert 1.0 released on PyPI and Homebrew with a published semver and deprecation policy.
- Zero unversioned breaking changes from 1.0 onward.
- Test coverage at or above 85% with all supported platforms green (Python 3.10–3.13 and Windows).
- This portfolio's bridge runs entirely on released engine features, with no repo-local patches.

## Scope

In scope: the docassert package, docassert-action, the Homebrew tap, PyPI
releases, and the pre-1.0 feature set named in the PRD. Out of scope: spec
authorship (PRJ-003-STD), site documentation of features (PRJ-004-ADO), and
post-1.0 maintenance (transfers to PRJ-005-OPS at closure).

## Milestones

- Bridge per-project mapping released: 2026-07-31.
- Risk disposition released: 2026-08-15.
- Operations kind and profile released: 2026-09-15.
- 1.0 release with stability policy: 2026-10-31.

## Risks

- GitHub sub-issues API changes under the bridge. Owner: John Tanner. Mitigation: tolerant error handling already in place; conformance of bridge behavior pinned by tests.
- Scope creep delays 1.0. Owner: John Tanner. Mitigation: pre-1.0 scope frozen to the PRD; everything else queues for 1.x.

## Approval

Draft — pending sponsor review of target date and milestone sequence.
