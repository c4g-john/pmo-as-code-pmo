---
kind: test-cases
id: STD-test-cases
project: PRJ-003-STD
title: Standard 1.0 — Test Cases
owner: johntanner
status: draft
---

## Overview

Acceptance verification for the standard; the conformance suite itself is the
deeper test bed and is not duplicated here.

## Test Cases

- **STD-TC-001** (tests: STD-AC-001): Steps: list every field and disposition value in the engine's risk tests, then locate each in the specification's risk section. Expected: no unspecified field or value.
- **STD-TC-002** (tests: STD-AC-002): Steps: enumerate the MUSTs of the execution section and map each to a conformance case id or an untestable rationale. Expected: full coverage of the enumeration.
- **STD-TC-003** (tests: STD-AC-003): Steps: author an operations document using only the specification text, then run the reference validator. Expected: passes without corrections.
- **STD-TC-004** (tests: STD-AC-004): Steps: count conformance cases and run the suite against the reference implementation. Expected: at least 80 cases, all passing.
- **STD-TC-005** (tests: STD-AC-005): Steps: take three historical changes (one breaking, one additive, one editorial) and classify each with the versioning policy. Expected: unambiguous classification matching their actual version bumps.
- **STD-TC-006** (tests: STD-AC-006): Steps: patch the engine to emit a divergent status derivation on a conformance fixture and run CI. Expected: the conformance job fails.
