---
kind: test-cases
id: ADO-test-cases
project: PRJ-004-ADO
title: Launch and adoption — Test Cases
owner: johntanner
status: draft
---

## Overview

Verification for launch readiness and the adoption loop.

## Test Cases

- **ADO-TC-001** (tests: ADO-AC-001): Steps: list features from the engine changelog since 0.10, search the site for each. Expected: every feature has a documenting section.
- **ADO-TC-002** (tests: ADO-AC-002): Steps: open the self-governance page and follow every link. Expected: dashboard, five project pages, and the documents repository load and show current content.
- **ADO-TC-003** (tests: ADO-AC-003): Steps: diff every feature claim in the final announcement texts against the 1.0 changelog. Expected: no claim without a shipped feature.
- **ADO-TC-004** (tests: ADO-AC-004): Steps: at month end, capture template forks and action dependents with dates and record the status report. Expected: both figures present with retrieval dates and method link.
- **ADO-TC-005** (tests: ADO-AC-005): Steps: create a repository from the template, follow only the README, open a test pull request with a broken link, then fix it. Expected: the gate blocks then passes, and the dashboard deploys.
