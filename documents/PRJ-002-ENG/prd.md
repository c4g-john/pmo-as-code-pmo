---
kind: prd
id: ENG-prd
project: PRJ-002-ENG
title: Engine 1.0 — Product Requirements
owner: johntanner
status: approved
---

## Overview

The pre-1.0 feature set, every item of which was discovered by dogfooding:
the Refuge bridge exposed the single-repo limitation, the risk table exposed
the missing disposition lifecycle, and chartering this portfolio's BAU
exposed the missing operations kind.

## Product Requirements

- **ENG-PR-001** (traces: ENG-BR-003): Bridge commands shall accept a project filter and a per-project repository mapping, so one documents repository can scaffold each project into its own code repository.
- **ENG-PR-002** (traces: ENG-BR-005): Risk items shall carry a disposition (open, mitigated, accepted, closed); only open risks shall drive the derived RAG, and the status-page risk table shall show the disposition of every risk.
- **ENG-PR-003** (traces: ENG-BR-004): An operations document kind and profile shall exist, with a service catalog, service-level objectives, and a mandatory review-by date; a stale review shall turn the derived status amber.
- **ENG-PR-004** (traces: ENG-BR-001): The public CLI surface shall be documented, and a stability policy shall define what 1.x guarantees and how deprecations are announced.
- **ENG-PR-005** (traces: ENG-BR-002): Continuous integration shall enforce a coverage floor of 85% and keep the full platform matrix green.
- **ENG-PR-006** (traces: ENG-BR-003): Bridge mutations shall be safe under concurrent runs: scaffolding shall converge on exactly one issue per marker even when runs race, and board field initialization shall treat an already-existing field as success.
- **ENG-PR-007** (traces: ENG-BR-005): Status pages shall present the derived model as a decision-grade dashboard: a verdict composed deterministically from the actual status causes, milestone timelines from dated charter milestones and the operations review, execution work and lifetime lanes from real bridge issue dates and states, recent document activity from the repository history, and an interactive risk view — with every element derived from recorded data and nothing invented.

## Acceptance Criteria

- **ENG-AC-001** (verifies: ENG-PR-001): Given a documents repository with two projects mapped to different code repositories, when the bridge scaffolds, then each project's Features and Stories are created only in its own repository.
- **ENG-AC-002** (verifies: ENG-PR-002): Given a register whose every risk is dispositioned mitigated, accepted, or closed, when status derives, then open risks no longer hold the RAG at amber.
- **ENG-AC-003** (verifies: ENG-PR-003): Given an operations document whose review-by date has passed, when status derives, then the project shows amber with the stale review named as the cause.
- **ENG-AC-004** (verifies: ENG-PR-004): Given the 1.0 release, when its documentation is read, then every public command and flag is described and the deprecation policy is stated.
- **ENG-AC-005** (verifies: ENG-PR-005): Given a change that drops coverage below 85%, when CI runs, then the build fails.
- **ENG-AC-006** (verifies: ENG-PR-006): Given two scaffold runs racing over the same repository, when both complete, then exactly one open issue exists per bridge marker; and given field initialization against a board whose fields already exist, when it runs, then it succeeds without error.
- **ENG-AC-007** (verifies: ENG-PR-007): Given a project page, when its verdict, stats, timeline, gantt lanes, and activity are compared to the model, then each traces to a recorded source (documents, bridge issues, or repository history) with no unsourced value.
- **ENG-AC-008** (verifies: ENG-PR-007): Given a charter milestone bullet ending in an ISO date, when status derives, then the milestone appears on the timeline with its temporal state (elapsed, today, or upcoming with a day count), and a past date is never presented as completion.
- **ENG-AC-009** (verifies: ENG-PR-007): Given bridge execution data with issue states and dates, when the page renders, then work rows and lanes show real titles, real states, and real created-to-closed spans, and the presentation never feeds back into the derived RAG.

## Out of Scope

New document kinds beyond operations; plugin or extension APIs; performance
work beyond keeping gates under the portfolio's 5-minute budget.
