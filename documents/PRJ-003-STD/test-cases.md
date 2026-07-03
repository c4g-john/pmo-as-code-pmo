---
kind: test-cases
id: STD-test-cases
project: PRJ-003-STD
title: Standard 1.0 — Test Cases
owner: johntanner
status: approved
---

## Overview

Acceptance verification for the standard; the conformance suite itself is the
deeper test bed and is not duplicated here.

## Test Cases

- **STD-TC-001** (tests: STD-AC-001): Steps: list every field and disposition value in the engine's risk tests, then locate each in the specification's risk section. Expected: no unspecified field or value.
- **STD-TC-002** (tests: STD-AC-002): Steps: build a traceability table in the conformance suite's README with one row per MUST of the execution section, each row naming a conformance case id or carrying an untestable rationale, then check every execution-section MUST appears. Expected: the table exists, covers every MUST, and every named case id runs in the suite.
- **STD-TC-003** (tests: STD-AC-003): Steps: author an operations document using only the specification text, then run the reference validator. Expected: passes without corrections.
- **STD-TC-004** (tests: STD-AC-004): Steps: count conformance cases and run the suite against the reference implementation. Expected: at least 80 cases, all passing.
- **STD-TC-005** (tests: STD-AC-005): Steps: take three historical changes (one breaking, one additive, one editorial) and classify each with the versioning policy. Expected: unambiguous classification matching their actual version bumps.
- **STD-TC-006** (tests: STD-AC-006): Steps: patch the engine to emit a divergent status derivation on a conformance fixture and run CI; separately, propose a behavior change pull request with no specification change and read the review outcome. Expected: the conformance job fails the first, and the spec-first policy is cited blocking the second.
