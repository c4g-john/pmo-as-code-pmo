---
kind: user-story
id: OPS-user-story
project: PRJ-005-OPS
title: Portfolio operations 2026-H2 — User Stories
owner: johntanner
status: approved
---

## Overview

Delivery slices for the period's service commitments. Each service is a
single ongoing commitment, so stories map one to one; they close at period
end with the ops review. Acceptance criteria live with the PRD.

## User Stories

- **OPS-US-001** (traces: OPS-PR-001): As an operator, I want every Dependabot pull request merged or reason-closed within 14 days so that dependency debt never accumulates silently.
- **OPS-US-002** (traces: OPS-PR-002): As an adopter, I want confirmed defects patched within 7 days across PyPI, Homebrew, and the action so that staying current is always safe.
- **OPS-US-003** (traces: OPS-PR-003): As a sponsor, I want advisories triaged within 48 hours and CodeQL kept clean so that security posture is a record rather than a hope.
- **OPS-US-004** (traces: OPS-PR-004): As an operator, I want a renewal inventory covering every expiring asset so that no domain, token, or certificate lapses by surprise.
- **OPS-US-005** (traces: OPS-PR-005): As a sponsor, I want a monthly operations report stating service levels, effort against the 20% cap, and spend so that keep-the-lights-on stays bounded and visible.
- **OPS-US-006** (traces: OPS-PR-006): As an operator, I want runbook entries for known transient CI failure patterns so that a flake costs one dispatch instead of an investigation.
- **OPS-US-007** (traces: OPS-PR-007): As a sponsor, I want CI failures to surface themselves in one self-closing alert so that I am never the monitoring system for my own delivery infrastructure.
