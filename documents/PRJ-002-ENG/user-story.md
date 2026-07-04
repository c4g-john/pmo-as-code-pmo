---
kind: user-story
id: ENG-user-story
project: PRJ-002-ENG
title: Engine 1.0 — User Stories
owner: johntanner
status: approved
---

## Overview

Delivery slices for the 1.0 scope. The bridge mapping, risk disposition, and
operations kind each split into separately shippable slices; the stability
policy and coverage floor are single coherent deliverables. Acceptance
criteria live with the PRD.

## User Stories

- **ENG-US-001** (traces: ENG-PR-001): As a portfolio maintainer, I want bridge commands to accept a project filter so that one documents repository can drive scaffolds for a single project at a time.
- **ENG-US-002** (traces: ENG-PR-001): As a portfolio maintainer, I want each project's target repository declared in configuration so that scaffolds route to the right code repo without per-run flags.
- **ENG-US-003** (traces: ENG-PR-002): As a PMO lead, I want risks dispositioned open, mitigated, accepted, or closed, with only open risks driving the derived RAG, so that a governed register can earn green through recorded work.
- **ENG-US-004** (traces: ENG-PR-002): As a status-page reader, I want each risk's disposition visible in the risk table so that live threats are distinguishable from retired ones.
- **ENG-US-005** (traces: ENG-PR-003): As an operations owner, I want an operations document kind with a service catalog and a review-by date so that ongoing work is governed without invented end dates.
- **ENG-US-006** (traces: ENG-PR-003): As a sponsor, I want a stale operations review to turn the derived status amber automatically so that neglected operations become visible without anyone reporting them.
- **ENG-US-007** (traces: ENG-PR-003): As an adopter, I want an operations profile so that an operations-focused repository can enforce its own required document set.
- **ENG-US-008** (traces: ENG-PR-004): As an adopter, I want a published stability and deprecation policy with the full CLI surface documented so that I can pin, upgrade, and automate without fear of silent breakage.
- **ENG-US-009** (traces: ENG-PR-005): As a maintainer, I want continuous integration to fail below the 85% coverage floor so that the quality bar is enforced rather than aspirational.
- **ENG-US-010** (traces: ENG-PR-006): As a portfolio maintainer, I want racing scaffold runs to converge on one issue per marker so that a dispatch racing a push trigger cannot duplicate the board.
- **ENG-US-011** (traces: ENG-PR-006): As a portfolio maintainer, I want board field initialization to treat existing fields as success so that concurrent syncs to a shared board cannot fail each other.
- **ENG-US-012** (traces: ENG-PR-007): As a sponsor, I want the project page to open with a verdict and stat cluster composed from the real status causes so that the first screen answers whether I should worry.
- **ENG-US-013** (traces: ENG-PR-007): As a sponsor, I want milestone timelines and execution lanes drawn from dated charter milestones and real issue lifetimes so that schedule truth comes from records, not estimates.
- **ENG-US-014** (traces: ENG-PR-007): As a reader, I want the risk register as an interactive heat matrix and expandable table so that I can isolate what threatens what without leaving the page.
- **ENG-US-015** (traces: ENG-PR-007): As a reader, I want document, work, and activity views with filters so that one page carries the whole project story from scope to delivery.
- **ENG-US-016** (traces: ENG-PR-007): As a portfolio sponsor, I want the index redesigned as a health-distribution overview with filterable project rows so that portfolio triage starts at the worst news.
