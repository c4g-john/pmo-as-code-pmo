---
kind: risk-register
id: GOV-risk-register
project: PRJ-001-GOV
title: Self-governance — Risk Register
owner: johntanner
status: approved
---

## Overview

Risks specific to governing the toolchain with itself.

## Risks

- **GOV-RISK-001** (threatens: GOV-BR-001): Recursion confusion — contributors mistake governance documents for product documentation or vice versa. Probability: medium. Impact: medium. Owner: johntanner. Response: this repository holds governance only; each component repo keeps its own README and product docs; the portfolio README states the split.
- **GOV-RISK-002** (threatens: GOV-BR-003): Bridge wiring depends on engine features that may slip. Probability: medium. Impact: medium. Owner: johntanner. Status: closed. Response: documents-only phase delivers the dashboard first; bridge milestone is explicitly gated on PRJ-002-ENG scope. Evidence: the dependency shipped: bridge --project routing and repo mapping released in 0.14.0 and wired across all four delivery repositories on 2026-07-03.
- **GOV-RISK-003** (threatens: GOV-BR-002): Single administrator — one person holds all tokens and settings. Probability: low. Impact: high. Owner: johntanner. Response: settings documented as runbooks; branch protection and required checks prevent silent drift.
- **GOV-RISK-004** (threatens: GOV-BR-002): Pages deployment failures go unnoticed — GitHub's deploy backend fails opaquely (observed on two repos on 2026-07-03, one unnoticed for 16 hours) and nothing alerts on a stale dashboard. Probability: medium. Impact: medium. Owner: johntanner. Response: retry runbook proven (settle-and-retry, discriminating rerun); automatic surfacing of deploy failures is a candidate story for the bridge era.
