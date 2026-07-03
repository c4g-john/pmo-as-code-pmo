---
kind: charter
project: PRJ-003-STD
id: STD-charter
title: Standard 1.0 — Project Charter
sponsor: John Tanner
budget:
  amount: 12000
  currency: USD
dates:
  created: 2026-07-03
  target: 2026-11-30   # proposed — confirm at review
status: draft
---

## Objective

Publish PMO as Code 1.0 as a standard independent of its reference
implementation: everything the engine enforces is specified, everything
specified is conformance-tested, and the document carries a versioning and
stability policy of its own.

## Success Criteria

- Specification 1.0 published with a versioning policy and RFC-2119 conformance language throughout.
- Conformance suite at 80 cases or more, with the reference implementation passing 100%.
- Zero engine behaviors observable in the gates that the specification does not describe.
- Execution mapping, risk lifecycle, and the operations kind specified normatively.

## Scope

In scope: SPEC.md, the conformance suite, the artifacts mirror, and the
specification's own governance (versioning, change history). Out of scope:
engine implementation (PRJ-002-ENG) and site presentation of the standard
(PRJ-004-ADO).

## Milestones

- Risk metadata and disposition semantics specified: 2026-08-31.
- Execution mapping promoted from informative appendix to normative section: 2026-09-30.
- Operations kind specified: 2026-10-15.
- 1.0 published with versioning policy: 2026-11-30.

## Risks

- Spec and engine drift apart as both change. Owner: John Tanner. Mitigation: conformance suite runs in engine CI; drift is a red build, not a discovery.
- No external reviewers yet. Owner: John Tanner. Mitigation: the AI advisory grades internal consistency; external review is an adoption-project outcome.

## Approval

Draft — pending sponsor review of target date and conformance-count target.
