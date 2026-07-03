---
kind: test-cases
id: GOV-test-cases
project: PRJ-001-GOV
title: Self-governance — Test Cases
owner: johntanner
status: draft
---

## Overview

Verification for the governance stack; most cases execute against live CI
behavior rather than code.

## Test Cases

- **GOV-TC-001** (tests: GOV-AC-001): Steps: open a pull request introducing a document with a broken item reference. Expected: the consistency check fails and the merge button is blocked.
- **GOV-TC-002** (tests: GOV-AC-002): Steps: merge a visible document change and poll the public dashboard. Expected: the change appears within 10 minutes.
- **GOV-TC-003** (tests: GOV-AC-003): Steps: open a workflow-only pull request and read the consistency log. Expected: the alignment advisory reports skipped with no key.
- **GOV-TC-004** (tests: GOV-AC-004): Steps: approve a test story, dispatch the bridge scaffold, and inspect the target code repository. Expected: the Story exists as a sub-issue under its Feature with the bridge marker.
- **GOV-TC-005** (tests: GOV-AC-005): Steps: edit a project anchor's name without regenerating projects.yaml and push. Expected: the registry check fails.
- **GOV-TC-006** (tests: GOV-AC-006): Steps: export gate durations for the trailing month from the Actions API and compute the median. Expected: under 5 minutes.
