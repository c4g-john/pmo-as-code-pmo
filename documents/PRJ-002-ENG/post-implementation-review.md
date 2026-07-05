---
kind: post-implementation-review
project: PRJ-002-ENG
id: ENG-post-implementation-review
title: Engine 1.0 — Post-Implementation Review
owner: johntanner
status: approved
---

## Summary

docassert 1.0.0 shipped to PyPI on 2026-07-04, seventeen weeks ahead of the
charter's 2026-10-31 target, with the stability policy published and binding.
All 7 features and 18 stories closed on the delivery board with evidence, the
last several via the feature close-out automation the project itself built.
Thirteen releases carried the pre-1.0 scope from v0.14.0 (the first bridge
milestone) through v1.0.2. Verdict: delivered in full, early, with every
success criterion met and two exceeded.

## Outcomes vs Objectives

Charter objective: ship a stable engine whose remaining pre-1.0 scope is the
set of needs discovered by running PMO as Code on real portfolios, backed by
a published stability and deprecation policy. Outcome: delivered exactly so —
the per-project bridge (v0.14.0), risk disposition (v0.15.0), and operations
governance (v0.16.0) each came from a real portfolio need, and STABILITY.md
became binding at 1.0.0.

Success criteria, each against its actual:

- 1.0 on PyPI and Homebrew by 2026-10-31 with a published semver and
  deprecation policy: released 2026-07-04; the Homebrew tap converges
  automatically and serves 1.0.2 today. Met, 118 days early.
- Zero unversioned breaking changes from 1.0 onward: holds through 1.0.1 and
  1.0.2 (both patches); enforced ongoing by the CLI-surface drift gate.
  Met to date; measurement continues under PRJ-005-OPS.
- Coverage at or above 85% with all supported platforms green: CI enforces
  fail_under=85 and is green on Python 3.10 through 3.14 plus Windows — one
  more Python version than the charter named. Exceeded.
- The portfolio's bridge runs entirely on released engine features with zero
  repo-local patches: true since v0.14.0; every governance repo pins a
  released version and carries no engine patches. Met.

Milestones, target vs actual: bridge per-project mapping 2026-07-31 → shipped
2026-07-03; risk disposition 2026-08-15 → 2026-07-04; operations kind and
profile 2026-09-15 → 2026-07-04; 1.0 with stability policy 2026-10-31 →
2026-07-04.

Budget: no spend against the USD 12,000 authorization was separately
tracked; direct costs were limited to CI minutes and AI-advisory API usage.

## What Went Well

- Dogfood-driven scope held. The pre-1.0 backlog was frozen to needs
  discovered running real portfolios, and nothing else got in; the scope
  guard and the PRD freeze did their jobs.
- Spec-first lockstep worked: every normative change landed in the
  specification and its conformance suite before the engine PR that
  implemented it, so "implements spec vX" stayed a checkable claim.
- The delivery loop closed end to end: approved scope scaffolded the board
  in seconds, merged engine PRs closed stories, and features closed
  themselves — eight times without a hand touching the board.
- Release and pin automation reached zero-touch: version bumps, the tap,
  and the spec artifacts mirror all converge without manual steps.

## What Could Improve

- Two defects shipped inside the automation itself before being caught by
  live behavior rather than tests: the bridge's issue index assumed
  oldest-first API ordering (dashboards briefly over-reported completion),
  and a bump workflow referenced an undefined variable behind `|| true`,
  which silently disabled auto-merge arming for a day.
- A first-hour defect survived until after 1.0: the fresh project scaffold
  failed its own validation, found only when the adopter path was exercised
  end to end. The exercise existed as scoped work; running it earlier would
  have caught the bug pre-1.0.

## Lessons Learned

- Any consumer of a list API must state and test its ordering assumption;
  a wrong assumption can make derived status lie in the optimistic
  direction, which is the worst direction for this system.
- `|| true` after a mutating command is a vacuity hazard: pair every
  tolerated failure with a converging cleanup or an alert, never silence
  alone.
- Event-triggered automation under a concurrency guard must be
  level-triggered: GitHub keeps one queued run and cancels the rest, so any
  surviving run has to be able to reconcile everything.
- The adopter test earns its place as a release gate, not an afterthought:
  it is now a regression test that runs the README's exact command
  sequence.

## Follow-up Actions

- Post-1.0 maintenance, SLAs, and the stability commitment transfer to
  PRJ-005-OPS per the charter's scope clause. Owner: johntanner. Effective
  at this document's approval; already operating in practice.
- Conformance suite growth toward the 80-case threshold and spec 1.0
  remain with PRJ-003-STD; the engine tracks the spec pin as releases land.
  Owner: johntanner. Target: 2026-11-30 (the STD charter date).
- Quarterly adopter-path exercise continues under ADO-PR-005's cadence,
  next due 2026-10-05. Owner: johntanner.
