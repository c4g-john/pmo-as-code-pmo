---
kind: prd
id: ADO-prd
project: PRJ-004-ADO
title: Launch and adoption — Product Requirements
owner: johntanner
status: draft
---

## Overview

Four deliverable groups: site feature parity, the self-governance showcase,
the launch itself, and honest adoption measurement.

## Product Requirements

- **ADO-PR-001** (traces: ADO-BR-002): The site shall document every released engine feature, including the advisory cache budget, per-relation rubrics, the risk table, and the operations kind when it ships.
- **ADO-PR-002** (traces: ADO-BR-004): A self-governance page shall present the live portfolio dashboard, the five projects, and how a reader can verify each claim in the repositories.
- **ADO-PR-003** (traces: ADO-BR-001): The launch announcements shall be published from the drafts on file, updated to the shipped feature set, only after Engine 1.0 is released.
- **ADO-PR-004** (traces: ADO-BR-003): The adopter count shall be produced monthly from template forks and action dependents, recorded in a status report, with the method documented on the site.
- **ADO-PR-005** (traces: ADO-BR-003): The template's adopter experience shall be exercised end to end quarterly: a fresh copy reaches a green gate and a live dashboard using only the README.

## Acceptance Criteria

- **ADO-AC-001** (verifies: ADO-PR-001): Given the engine changelog at launch, when each released feature is searched on the site, then a documenting page exists for every one.
- **ADO-AC-002** (verifies: ADO-PR-002): Given the self-governance page, when a reader follows its links, then the live dashboard, the five project pages, and this repository are all reachable and current.
- **ADO-AC-003** (verifies: ADO-PR-003): Given Engine 1.0 on PyPI, when the announcements publish, then every feature claim in them matches the released engine.
- **ADO-AC-004** (verifies: ADO-PR-004): Given a month end, when the adopter count is recorded, then forks and dependents are separately stated with retrieval dates.
- **ADO-AC-005** (verifies: ADO-PR-005): Given a fresh template copy and only the README, when setup is followed, then audit and consistency gate a test pull request and the dashboard deploys.

## Out of Scope

Site redesigns; localization; analytics beyond the documented adopter count.
