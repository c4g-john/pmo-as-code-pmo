---
kind: test-cases
id: ENG-test-cases
project: PRJ-002-ENG
title: Engine 1.0 — Test Cases
owner: johntanner
status: draft
---

## Overview

Acceptance verification for the 1.0 scope; engine features also carry unit
tests in the docassert repository, which these cases do not duplicate.

## Test Cases

- **ENG-TC-001** (tests: ENG-AC-001): Steps: in a fixture repository with projects mapped to two target repositories, run the bridge scaffold and list issues in both targets. Expected: each target holds only its own project's Features and Stories.
- **ENG-TC-002** (tests: ENG-AC-002): Steps: disposition every risk in a fixture register as mitigated or accepted, then derive status. Expected: the open-risk signal is empty and the RAG is not amber on account of risks.
- **ENG-TC-003** (tests: ENG-AC-003): Steps: set an operations document's review-by date in the past and derive status. Expected: amber, with the stale review named in the signals.
- **ENG-TC-004** (tests: ENG-AC-004): Steps: for each subcommand in the CLI help output, search the released documentation. Expected: every command and flag is documented, and the stability policy section exists.
- **ENG-TC-005** (tests: ENG-AC-005): Steps: push a branch deleting a test module and read CI. Expected: the coverage gate fails the build.
