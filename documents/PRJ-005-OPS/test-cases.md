---
kind: test-cases
id: OPS-test-cases
project: PRJ-005-OPS
title: Portfolio operations 2026-H2 — Test Cases
owner: johntanner
status: approved
---

## Overview

Operations verification runs against the record: pull request history,
release timestamps, and the monthly reports.

## Test Cases

- **OPS-TC-001** (tests: OPS-AC-001): Steps: at month end, list the period's Dependabot pull requests with open-to-close ages. Expected: all within 14 days or closed with a stated reason.
- **OPS-TC-002** (tests: OPS-AC-002): Steps: for each confirmed defect in the period, compare confirmation date to release timestamps on PyPI, Homebrew, and action tags. Expected: all within 7 days.
- **OPS-TC-003** (tests: OPS-AC-003): Steps: for each advisory in the period, read the triage record's timestamp. Expected: within 48 hours of publication.
- **OPS-TC-004** (tests: OPS-AC-004): Steps: walk the lifecycle inventory, checking each renewal date against today. Expected: no asset past due or unscheduled.
- **OPS-TC-005** (tests: OPS-AC-005): Steps: open the latest monthly status report. Expected: service levels, effort percentage against the 20% cap, and spend against the 12,000 USD envelope are stated.
- **OPS-TC-006** (tests: OPS-AC-006): Steps: on the next PyPI propagation failure in CI, follow the runbook entry. Expected: resolved by re-dispatch without investigation.
- **OPS-TC-007** (tests: OPS-AC-007): Steps: observe a real workflow failure (or dispatch one against a scratch branch), wait one sweep interval, read the alert issue, resolve the failure, and wait one more sweep. Expected: the issue named the failure with a run link and closed itself after the fix.
