---
kind: brd
id: STD-brd
project: PRJ-003-STD
title: Standard 1.0 — Business Requirements
owner: johntanner
status: approved
---

## Purpose

A standard is what separates a methodology from a tool's behavior. For PMO as
Code to outlive any one implementation, the specification must be complete,
testable, and stable enough for a second implementation to target.

## Business Requirements

- **STD-BR-001**: The business shall publish specification 1.0 such that an independent implementer can pass the conformance suite without reading the reference implementation's source.
- **STD-BR-002**: The business shall keep the specification complete with respect to the engine, with zero gate-observable behaviors undescribed at 1.0 and none introduced undescribed thereafter.
- **STD-BR-003**: The business shall grow the conformance suite to 80 cases or more, covering every normative section.
- **STD-BR-004**: The business shall version the standard itself, with breaking changes only in major versions.

## Out of Scope

Engine implementation and release mechanics (PRJ-002-ENG); marketing of the
standard (PRJ-004-ADO); certification of third-party implementations.
