---
kind: risk-register
id: STD-risk-register
project: PRJ-003-STD
title: Standard 1.0 — Risk Register
owner: johntanner
status: approved
---

## Overview

Risks to publishing a standard that holds up.

## Risks

- **STD-RISK-001** (threatens: STD-BR-002): Spec-engine drift — the implementation evolves faster than the text. Probability: high. Impact: medium. Owner: johntanner. Status: mitigated. Response: conformance suite in engine CI makes drift a failing build; spec-first policy for behavior changes. Evidence: conformance runs in engine CI at pinned spec tags, the spec-first merge policy held across five releases this week, and the artifact-sync drift guard is now verified live (its stale 0.7.1 pin was found and fixed).
- **STD-RISK-002** (threatens: STD-BR-001): Author bias — the spec unknowingly describes the implementation rather than the design. Probability: medium. Impact: medium. Owner: johntanner. Response: acceptance requires authoring fixtures from the text alone; adoption project recruits external readers.
- **STD-RISK-003** (threatens: STD-BR-004): Premature 1.0 locks in a flawed grammar. Probability: low. Impact: high. Owner: johntanner. Response: every grammar in 1.0 has shipped in the reference implementation for months and is exercised by two live portfolios.
