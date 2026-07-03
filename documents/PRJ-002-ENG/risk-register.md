---
kind: risk-register
id: ENG-risk-register
project: PRJ-002-ENG
title: Engine 1.0 — Risk Register
owner: johntanner
status: approved
---

## Overview

Risks to shipping a stable 1.0.

## Risks

- **ENG-RISK-001** (threatens: ENG-BR-003): GitHub's sub-issues API is still maturing and may change shape under the bridge. Probability: medium. Impact: medium. Owner: johntanner. Response: tolerant error handling for link mutations; bridge behavior pinned by regression tests; failures degrade to plain issues rather than blocking.
- **ENG-RISK-002** (threatens: ENG-BR-001): Committing to 1.0 stability too early freezes a design flaw. Probability: medium. Impact: high. Owner: johntanner. Response: the pre-1.0 scope is exactly the features this portfolio exercises daily; nothing enters 1.0 unproven by dogfood use.
- **ENG-RISK-003** (threatens: ENG-BR-002): Single maintainer — review depth and bus factor. Probability: medium. Impact: high. Owner: johntanner. Response: CI gates carry the review load a second engineer would; conformance suite pins behavior independently of the implementation.
- **ENG-RISK-004** (threatens: ENG-BR-001): PyPI CDN propagation lag makes releases look broken in downstream CI. Probability: high. Impact: low. Owner: johntanner. Response: documented re-dispatch runbook; downstream workflows budget a propagation delay before installing fresh releases.
