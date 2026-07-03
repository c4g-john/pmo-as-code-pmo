---
kind: brd
id: OPS-brd
project: PRJ-005-OPS
title: Portfolio operations 2026-H2 — Business Requirements
owner: johntanner
status: draft
---

## Purpose

Every adopter-facing promise (a working action, an installable package, a
live dashboard, a renewed domain) depends on unglamorous recurring work. This
project makes that work visible, bounded, and owned instead of ambient and
unaccounted.

## Business Requirements

- **OPS-BR-001**: The business shall keep dependencies current, with Dependabot pull requests merged or dispositioned within 14 days across all ecosystem repositories.
- **OPS-BR-002**: The business shall service defects, shipping a patch release within 7 days of confirming one.
- **OPS-BR-003**: The business shall hold security posture, triaging advisories within 48 hours and keeping CodeQL findings at zero or dispositioned.
- **OPS-BR-004**: The business shall bound keep-the-lights-on effort at 20% of capacity, reported monthly, so operations never silently starves project delivery.

## Out of Scope

Feature development; adoption work; spec authorship. Each belongs to its
outcome project.
