---
kind: charter
project: PRJ-001-GOV
id: GOV-charter
title: Self-governance — Project Charter
sponsor: John Tanner
budget:
  amount: 12000
  currency: USD
dates:
  created: 2026-07-03
  target: 2026-08-31
status: approved
---

## Objective

Make PMO as Code its own first-class user: every component of the ecosystem
(engine, spec, site, template, action, distribution) is governed by documents
in this repository, validated by the same gates adopters use, and reported on
a public derived dashboard.

## Success Criteria

- Portfolio dashboard live on GitHub Pages, regenerated within 10 minutes of every merge to main.
- Audit and consistency gates required on every pull request, with median CI time under 5 minutes.
- 100% of feature pull requests merged in scope repos reference a bridge story, once the bridge is wired.
- All 5 projects registered in projects.yaml with 0 registry-drift failures on main through 2026-08-31.

## Scope

In scope: this documents repository, its CI gates, the advisory alignment
layer, the derived dashboard, branch protection, and bridge wiring for each
project to its code repository. Out of scope: the engine features the bridge
wiring depends on (PRJ-002-ENG scope), the content of other projects'
documents, and any change to the Refuge for Humans repositories.

## Milestones

- Repository live with all five projects' draft documents: 2026-07-04.
- Charters and scope documents approved, projects active: 2026-07-15.
- Dashboard public: 2026-07-15.
- Bridge wired for all projects (gated on ENG delivering per-project mapping): 2026-08-31.

## Risks

- Recursion confusion between governing documents and product documents. Owner: John Tanner. Mitigation: this repository holds governance only; product truth stays in component repos.
- Single administrator for all repositories. Owner: John Tanner. Mitigation: documented runbooks; branch protection prevents silent drift.

## Approval

Approved by the sponsor, John Tanner, on 2026-07-03. Budget of USD 12,000
and the target date above are confirmed.
