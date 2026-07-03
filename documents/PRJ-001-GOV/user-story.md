---
kind: user-story
id: GOV-user-story
project: PRJ-001-GOV
title: Self-governance — User Stories
owner: johntanner
status: approved
---

## Overview

Delivery slices for the governance stack. The repository, dashboard,
advisory, and registry stories reflect work already delivered and will close
on scaffold; the bridge requirement splits into three slices because scaffold,
board, and close-out are separately shippable. Acceptance criteria live with
the PRD.

## User Stories

- **GOV-US-001** (traces: GOV-PR-001): As a portfolio sponsor, I want every scope change to enter through a gated pull request so that nothing changes without validation and my recorded sign-off.
- **GOV-US-002** (traces: GOV-PR-002): As a skeptical reader, I want a public dashboard derived from the documents so that I can verify the portfolio's claims without cloning anything.
- **GOV-US-003** (traces: GOV-PR-003): As a portfolio sponsor, I want the alignment advisory grading document changes on a cached budget so that semantic drift is flagged without runaway spend.
- **GOV-US-004** (traces: GOV-PR-004): As a portfolio sponsor, I want each project's approved stories scaffolded into that project's code repository so that delivery is tracked where the work happens.
- **GOV-US-005** (traces: GOV-PR-004): As a portfolio sponsor, I want a portfolio board mirroring Features and Stories with their document ids so that execution is visible in one place.
- **GOV-US-006** (traces: GOV-PR-004): As a portfolio sponsor, I want Features to close when their last story completes and rogue issues flagged within minutes so that the board stays governed by the documents.
- **GOV-US-007** (traces: GOV-PR-005): As a contributor, I want registry drift to fail the gate so that projects.yaml never misrepresents the portfolio.
- **GOV-US-008** (traces: GOV-PR-006): As a contributor, I want gate feedback in under 5 minutes median so that governance never becomes the slow part of a change.
