---
kind: prd
id: GOV-prd
project: PRJ-001-GOV
title: Self-governance — Product Requirements
owner: johntanner
status: draft
---

## Overview

The governance stack for this portfolio: repository, gates, advisory layer,
dashboard, and bridge wiring. Each requirement is the same mechanism we ship
to adopters, applied to ourselves.

## Product Requirements

- **GOV-PR-001** (traces: GOV-BR-001): The documents repository shall hold one folder per project with the full lean-startup document set, and audit plus consistency shall be required status checks on every pull request.
- **GOV-PR-002** (traces: GOV-BR-002): The status dashboard shall deploy to GitHub Pages on every push to main, with a portfolio index and one page per project.
- **GOV-PR-003** (traces: GOV-BR-001): The advisory alignment layer shall run with the key passed only when documents change, with the grading cache persisted between runs.
- **GOV-PR-004** (traces: GOV-BR-003): Each project shall be bridged to its component code repository, scaffolding Features and Stories from approved user stories.
- **GOV-PR-005** (traces: GOV-BR-001): The project registry shall be regenerated and checked for drift as a blocking gate.
- **GOV-PR-006** (traces: GOV-BR-004): Gate workflows shall complete in under 5 minutes median, measured over the trailing month of pull requests.

## Acceptance Criteria

- **GOV-AC-001** (verifies: GOV-PR-001): Given a pull request with a failing audit, when checks complete, then the merge is blocked.
- **GOV-AC-002** (verifies: GOV-PR-002): Given a merge to main, when the pages workflow completes, then the public dashboard reflects the merged content within 10 minutes.
- **GOV-AC-003** (verifies: GOV-PR-003): Given a pull request that touches no documents, when the consistency job runs, then the advisory reports skipped and no API spend occurs.
- **GOV-AC-004** (verifies: GOV-PR-004): Given an approved user story in any project, when the bridge scaffold runs, then a Story sub-issue exists in that project's code repository under its Feature.
- **GOV-AC-005** (verifies: GOV-PR-005): Given a project anchor edited without regenerating the registry, when consistency runs, then the check fails.
- **GOV-AC-006** (verifies: GOV-PR-006): Given the trailing month of pull requests, when gate durations are read from the Actions history, then the median is under 5 minutes.

## Out of Scope

Bridge board mirroring to Projects v2 for this portfolio (optional, revisit
after wiring); execution panels on the dashboard until the bridge is live.
