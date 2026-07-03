---
kind: prd
id: STD-prd
project: PRJ-003-STD
title: Standard 1.0 — Product Requirements
owner: johntanner
status: approved
---

## Overview

The path from v0.3.1 to 1.0: specify what live use has proven (the bridge),
what governance needs (risk lifecycle, operations), widen the conformance
net, and give the standard its own stability rules.

## Product Requirements

- **STD-PR-001** (traces: STD-BR-001): Risk item metadata (probability, impact, owner, response) and the disposition lifecycle shall be specified normatively, matching the engine's parsing rules.
- **STD-PR-002** (traces: STD-BR-001): The execution mapping shall be promoted from informative appendix to a normative section, citing the live bridge as its evidence base.
- **STD-PR-003** (traces: STD-BR-001): The operations document kind shall be specified, including the service catalog grammar, service-level objectives, and review-freshness semantics.
- **STD-PR-004** (traces: STD-BR-003): The conformance suite shall reach 80 cases or more, with at least one case per normative MUST added in this project.
- **STD-PR-005** (traces: STD-BR-004): The specification shall carry a versioning policy section defining major, minor, and errata changes and the deprecation process.
- **STD-PR-006** (traces: STD-BR-002): Specification completeness shall be enforced in both directions: engine continuous integration shall run the conformance suite on every change, failing on divergence from the specification, and gate-observable behavior changes shall land specification-first, so no such change merges without its specification text.

## Acceptance Criteria

- **STD-AC-001** (verifies: STD-PR-001): Given the specification's risk section, when the engine's risk-parsing tests are mapped to it, then every parsed field and disposition value is specified.
- **STD-AC-002** (verifies: STD-PR-002): Given the normative execution section, when its MUSTs are enumerated, then each is either conformance-tested or marked untestable with a rationale.
- **STD-AC-003** (verifies: STD-PR-003): Given the operations kind section, when a fixture operations document is authored from it alone, then the reference implementation validates it without corrections.
- **STD-AC-004** (verifies: STD-PR-004): Given the conformance suite at 1.0, when cases are counted, then there are at least 80 and the reference implementation passes all.
- **STD-AC-005** (verifies: STD-PR-005): Given the versioning policy, when a breaking change is proposed, then the policy unambiguously classifies it as major.
- **STD-AC-006** (verifies: STD-PR-006): Given an engine change that diverges from a specified behavior, when engine CI runs, then the conformance job fails; and given a gate-observable behavior change proposed without specification text, when reviewed, then the spec-first policy blocks it.

## Out of Scope

Governance of third-party implementations; translations; a formal standards-body
submission.
