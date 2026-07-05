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

Root cause on this fleet (diagnosed 2026-07-05): simultaneous pushes from
fleet-wide merges made sibling repositories create Pages deployments in the
same second, and deployment creation is not retried by the deploy action.
Roughly one deploy in five collided. Resolution is automated at three levels;
no manual re-dispatch is part of this procedure.

1. Confirm the build steps succeeded and only the deploy step failed.
2. In-run convergence: the workflow tolerates the first deploy attempt, sleeps a jittered 30 to 120 seconds to desynchronize the herd, and makes an authoritative second attempt. Check whether `deploy-again` succeeded.
3. Run-level convergence: the `deploy retry` workflow (workflow_run) reruns a failed run once after completion.
4. Level convergence: staggered schedules (pmo :11, refuge :31, pipeline :51, every two hours) rebuild the dashboard from HEAD regardless of push outcomes, so a failed deploy self-corrects within two hours with no action.
5. Only if the same repository stays red across two consecutive scheduled rebuilds: check https://www.githubstatus.com and open a support ticket with the deployment IDs. That situation has not yet been observed.

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

## Renewal Inventory

Every expiring asset, walked at each monthly operations report (OPS-SVC-004).
Dates are recorded facts; "unrecorded" means the owner must confirm and fill
the date, never guess it.

| Asset | Kind | Where it lives | Scope | Expires | Renewal action |
|---|---|---|---|---|---|
| DISPATCH_TOKEN | Fine-grained PAT | Secret on pmo-as-code-pmo, refuge-for-humans-pmo | Actions read/write on docassert, pmo-as-code-spec, pmo-as-code, refuge-for-humans-app | 2026-10-03 | Re-mint fine-grained PAT, same four repos, Actions RW; `gh secret set DISPATCH_TOKEN` on both senders |
| BUMP_TOKEN | Classic PAT (repo) | Secret on pmo-as-code-pmo, refuge-for-humans-pmo, pmo-as-code-pipeline, pmo-as-code-spec, homebrew-tap | repo scope, account-wide | unrecorded | Re-mint classic PAT repo scope; `gh secret set BUMP_TOKEN` on all five |
| PROJECTS_TOKEN | Classic PAT (project) | Secret on bridge-board repos | project scope | unrecorded | Re-mint classic PAT project scope; reset secret |
| ANTHROPIC_API_KEY | API key | Secret on repos running advisory checks | Anthropic API | does not expire | Rotate on suspicion; no scheduled renewal |
| pmoascode.com | Domain | Registrar | public site | unrecorded | Confirm auto-renew and card on file |
| docassert.com | Domain | Registrar | tool site | unrecorded | Confirm auto-renew and card on file |

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
