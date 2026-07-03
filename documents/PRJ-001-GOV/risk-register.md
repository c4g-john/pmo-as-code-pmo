---
kind: risk-register
id: GOV-risk-register
project: PRJ-001-GOV
title: Self-governance — Risk Register
owner: johntanner
status: draft
---

## Overview

Risks specific to governing the toolchain with itself.

## Risks

- **GOV-RISK-001** (threatens: GOV-BR-001): Recursion confusion — contributors mistake governance documents for product documentation or vice versa. Probability: medium. Impact: medium. Owner: johntanner. Response: this repository holds governance only; each component repo keeps its own README and product docs; the portfolio README states the split.
- **GOV-RISK-002** (threatens: GOV-BR-003): Bridge wiring depends on engine features that may slip. Probability: medium. Impact: medium. Owner: johntanner. Response: documents-only phase delivers the dashboard first; bridge milestone is explicitly gated on PRJ-002-ENG scope.
- **GOV-RISK-003** (threatens: GOV-BR-002): Single administrator — one person holds all tokens and settings. Probability: low. Impact: high. Owner: johntanner. Response: settings documented as runbooks; branch protection and required checks prevent silent drift.
