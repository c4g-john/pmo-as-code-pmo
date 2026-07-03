---
kind: brd
id: GOV-brd
project: PRJ-001-GOV
title: Self-governance — Business Requirements
owner: johntanner
status: draft
---

## Purpose

PMO as Code claims that documents can govern delivery. The strongest evidence
we can offer adopters is the toolchain governing its own portfolio in public,
with the same gates, dashboards, and traceability we recommend to them.

## Business Requirements

- **GOV-BR-001**: The business shall govern every ecosystem component through documents in this repository, with audit and consistency gates required on all changes.
- **GOV-BR-002**: The business shall publish a portfolio dashboard derived from these documents, refreshed within 10 minutes of every merge to main.
- **GOV-BR-003**: The business shall make delivery traceable end to end: once the bridge is wired, 100% of feature pull requests in scope repos reference a bridge story.
- **GOV-BR-004**: The business shall keep governance overhead proportional, with median gate time under 5 minutes per pull request.

## Out of Scope

The Refuge for Humans product and its repositories (separately governed);
engine feature work the bridge wiring depends on (PRJ-002-ENG); the public
launch narrative (PRJ-004-ADO).
