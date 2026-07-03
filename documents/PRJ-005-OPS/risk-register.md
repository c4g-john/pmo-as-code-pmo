---
kind: risk-register
id: OPS-risk-register
project: PRJ-005-OPS
title: Portfolio operations 2026-H2 — Risk Register
owner: johntanner
status: draft
---

## Overview

Operating risks for the period.

## Risks

- **OPS-RISK-001** (threatens: OPS-BR-004): Keep-the-lights-on effort creeps past its cap and starves project delivery. Probability: medium. Impact: high. Owner: johntanner. Response: monthly effort reporting against the 20% cap; a breach is an amber signal demanding rebalancing, not silent absorption.
- **OPS-RISK-002** (threatens: OPS-BR-002): Key-person dependency — one operator holds every runbook. Probability: medium. Impact: high. Owner: johntanner. Response: runbooks written to be executable by a stranger; the operations kind will make them auditable documents.
- **OPS-RISK-003** (threatens: OPS-BR-003): A vulnerable transitive dependency ships in a release. Probability: low. Impact: high. Owner: johntanner. Response: Dependabot plus advisory triage within 48 hours; patch-release service level bounds exposure to days.
- **OPS-RISK-004** (threatens: OPS-BR-001): Advisory API spend drifts upward unnoticed. Probability: low. Impact: low. Owner: johntanner. Response: key gating means spend only on document changes; monthly report states spend against the envelope.
