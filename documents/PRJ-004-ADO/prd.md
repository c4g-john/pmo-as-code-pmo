---
kind: prd
id: ADO-prd
project: PRJ-004-ADO
title: Launch and adoption — Product Requirements
owner: johntanner
status: approved
---

## Overview

Four deliverable groups: site feature parity, the self-governance showcase,
the launch itself, and honest adoption measurement.

## Product Requirements

- **ADO-PR-001** (traces: ADO-BR-002): The site shall document every released engine feature, including the advisory cache budget, per-relation rubrics, the risk table, and the operations kind when it ships.
- **ADO-PR-002** (traces: ADO-BR-004; after: ADO-PR-001): A self-governance page shall present the live portfolio dashboard, the five projects, and how a reader can verify each claim in the repositories.
- **ADO-PR-003** (traces: ADO-BR-001; after: ADO-PR-002): The launch announcements shall be published from the drafts on file, updated to the shipped feature set, only after Engine 1.0 is released.
- **ADO-PR-004** (traces: ADO-BR-003): The adopter count shall be produced monthly from template forks and action dependents, recorded in a status report, with the method documented on the site.
- **ADO-PR-007** (traces: ADO-BR-002): The site shall be rebuilt as a fully static multi-page site on Astro: prose pages authored as Markdown with schema-validated frontmatter, repeatable content (document kinds, profiles, proof links, fact-sheet entries) as typed data collections feeding page, JSON-LD, sitemap, and llms.txt from one record, and zero client-side JavaScript by default, with any interactive island justified in its pull request.
- **ADO-PR-008** (traces: ADO-BR-002; after: ADO-PR-007): Every page shall live at a real flat path with no fragment routing, every pre-rewrite URL shall keep resolving through permanent redirects, and every section heading shall carry a stable linkable anchor.
- **ADO-PR-009** (traces: ADO-BR-002; after: ADO-PR-007): Every page shall pass the delivery checklist of the committed content guidelines: one h1 with no skipped heading levels, semantic landmarks, primary content present in the built HTML, JSON-LD generated from the same records as the page and matching visible content, dateModified derived from git history, and llms.txt plus sitemap.xml emitted by the build.
- **ADO-PR-010** (traces: ADO-BR-002; after: ADO-PR-007): Every migrated page shall preserve or correct its factual claims, with a page-by-page parity record listing each claim kept, corrected, or retired, and all prose shall conform to the Human Authorship Standard.
- **ADO-PR-006** (traces: ADO-BR-001; after: ADO-PR-003): A public press and share kit page shall present a fact sheet, boilerplate descriptions, story angles, brand assets, contact details, and the announcement texts, with every factual claim verifiable against shipped artifacts; internal handoff drafts shall not be served on the public site.
- **ADO-PR-005** (traces: ADO-BR-003): The template's adopter experience shall be exercised end to end quarterly: a fresh copy reaches a green gate and a live dashboard using only the README.

## Acceptance Criteria

- **ADO-AC-001** (verifies: ADO-PR-001): Given the engine changelog at launch, when each released feature is searched on the site, then a documenting page exists for every one.
- **ADO-AC-002** (verifies: ADO-PR-002): Given the self-governance page, when a reader follows its links, then the live dashboard, the five project pages, and this repository are all reachable and current.
- **ADO-AC-003** (verifies: ADO-PR-003): Given Engine 1.0 on PyPI, when the announcements publish, then every feature claim in them matches the released engine.
- **ADO-AC-004** (verifies: ADO-PR-004): Given a month end, when the adopter count is recorded, then forks and dependents are separately stated with retrieval dates.
- **ADO-AC-005** (verifies: ADO-PR-005): Given a fresh template copy and only the README, when setup is followed, then audit and consistency gate a test pull request and the dashboard deploys.
- **ADO-AC-008** (verifies: ADO-PR-007): Given the built site, when its output is inspected, then every page is static HTML from Markdown or data-collection sources, and pages shipping JavaScript each cite a justification in the merged pull request.
- **ADO-AC-009** (verifies: ADO-PR-008): Given the pre-rewrite URL inventory, when each URL is requested, then it returns the page or a permanent redirect to it, and no link on the site uses fragment routing.
- **ADO-AC-010** (verifies: ADO-PR-009): Given any built page, when checked against the guidelines checklist, then heading structure, landmarks, server-rendered content, matching generated JSON-LD, derived dates, and build-emitted llms.txt and sitemap all pass.
- **ADO-AC-011** (verifies: ADO-PR-010): Given the parity record, when sampled against live pages, then every kept claim is verifiable, every corrected claim cites its correction, and a tells scan of migrated prose reports zero violations.
- **ADO-AC-006** (verifies: ADO-PR-006): Given the published press page, when each factual claim is checked, then it matches a shipped artifact (release, spec tag, or live dashboard), and no internal handoff draft resolves on the public site.
- **ADO-AC-007** (verifies: ADO-PR-006): Given the published press page, when a journalist uses it, then every visual asset is previewed on the page itself, prose copy renders wrapped with a one-click copy, and each announcement is presented in the form of its destination.

## Out of Scope

Site redesigns; localization; analytics beyond the documented adopter count.
