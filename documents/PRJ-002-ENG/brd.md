---
kind: brd
id: ENG-brd
project: PRJ-002-ENG
title: Engine 1.0 — Business Requirements
owner: johntanner
status: draft
---

## Purpose

Adopters will not gate their delivery on a tool that changes under them. A
1.0 with a stability promise, and with the features real portfolio use has
demanded, is what makes PMO as Code adoptable beyond its author.

## Business Requirements

- **ENG-BR-001**: The business shall publish docassert 1.0 with a semver and deprecation policy, and shall make no unversioned breaking change thereafter.
- **ENG-BR-002**: The business shall hold the engine's quality floor at 85% test coverage or higher, green on Python 3.10 through 3.13 and Windows.
- **ENG-BR-003**: The business shall make the engine serve multi-repo portfolios, proven by this portfolio's bridge running entirely on released features.
- **ENG-BR-004**: The business shall make ongoing operations governable, shipping an operations document kind whose status derives from service health and review freshness.

## Out of Scope

Spec text and conformance cases (PRJ-003-STD); site and template documentation
(PRJ-004-ADO); operating the released engine (PRJ-005-OPS).
