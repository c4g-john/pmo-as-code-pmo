---
kind: runbook
id: OPS-runbook
project: PRJ-005-OPS
title: Portfolio operations 2026-H2 — Runbook
owner: johntanner
status: approved
---

## Overview

Response procedures for the recurring operational patterns of this
ecosystem, written to be executable by a stranger. Every pattern here has
occurred in production; self-healing automation handles the first response
for most of them, and these procedures are the fallback when it does not.

## Prerequisites

The GitHub CLI authenticated as a repository admin; Python 3.10+ with pip;
read access to PyPI. Repository list and pins live in each repo's
`.docassert-version`.

## Procedures

### PyPI index propagation failure (install cannot find a fresh release)

1. Confirm the failing job's log shows `Could not find a version` naming the pinned version, and that the version exists on https://pypi.org/project/docassert/.
2. Note that installs retry automatically four times, 75 seconds apart (the docassert-action install path and the install sub-action); only proceed if all four failed.
3. Wait five minutes, then re-run only the failed jobs: `gh run rerun <run-id> --failed`.
4. If a third cycle fails, stop assuming propagation: diff what the job installed against the release, and read the pin file it used.

### GitHub Pages deployment failure ("Deployment failed, try again later")

1. Confirm the build steps succeeded and only the deploy step failed.
2. Note that the deploy retries itself once via the retry-on-flake job; only proceed if attempt two also failed.
3. Re-dispatch the workflow: `gh workflow run status-pages.yml --repo <repo>`.
4. On a newly Pages-enabled repository, expect a settling window: deploys may fail opaquely for up to an hour; re-dispatch after it.
5. If failures persist beyond an hour on an established site, check https://www.githubstatus.com and open a support ticket with the deployment IDs.

### Merge refused with green checks (base branch policy)

1. Confirm every required check passed and the refusal says the base branch policy prohibits the merge.
2. Prefer enabling auto-merge at PR creation (`gh pr merge --auto --squash`), which resolves base updates itself.
3. For an already-open PR: `gh pr update-branch <n>`, wait for checks on the refreshed head, then merge; read check-runs on the head commit, not the stale summary.

### Suspected drift-guard vacuity (a comparison check that cannot fail)

1. Identify what the guard compares against — a pin file, a tag, or "latest" — and read what the failing or passing job actually installed.
2. If the comparison target is stale, the guard is vacuous: bump the target and re-run to expose real drift, then fix the drift it reveals.
3. The ci-health sentinel lists pins that trail the latest release; treat a repeated listing as this pattern.

### Duplicate bridge issues (racing scaffolds)

1. Note that scaffolds converge automatically since docassert 0.14.1, closing higher-numbered duplicates per marker, and that workflow concurrency guards serialize runs.
2. If duplicates persist, run one manual scaffold dispatch and read its convergence log lines.

## Monitoring

The ci-health sentinel sweeps every repository's latest workflow conclusions
each half hour and maintains one self-closing "CI health: failures detected"
issue on this repository, including pins trailing the latest engine release.
Dashboards regenerate on every merge; the operations review date on the
operations document ambers this project automatically when it lapses.

## Escalation

Owner and operator: johntanner. Escalate GitHub-platform incidents via
https://support.github.com with run and deployment IDs; escalate engine
defects as issues on c4g-john/docassert, which enter scope through the
portfolio documents like all work.
