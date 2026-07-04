---
kind: operations
id: OPS-operations
project: PRJ-005-OPS
title: Portfolio operations 2026-H2 — Service Catalog
owner: johntanner
status: approved
review_by: 2026-09-30
---

## Overview

The 2026-H2 service catalog, migrated onto the operations kind its own
charter predicted (the period was chartered before the kind existed; the
engine shipped it as ENG-PR-003). Levels restate the approved service
commitments of the OPS product requirements; the mid-period review on
2026-09-30 and the period close on 2026-12-31 carry over unchanged.

## Services

- **OPS-SVC-001**: Dependency triage across the ecosystem's repositories. Level: every Dependabot pull request merged or reason-closed within 14 days. Measure: monthly pull-request age report in the operations status report.
- **OPS-SVC-002**: Defect release service to PyPI, Homebrew, and the action tags. Level: confirmed defects patched within 7 days of confirmation. Measure: confirmation-to-release timestamps compared per defect.
- **OPS-SVC-003**: Security posture. Level: advisories triaged within 48 hours and CodeQL findings at zero or dispositioned. Measure: triage record timestamps and the CodeQL dashboard.
- **OPS-SVC-004**: Credential, domain, and certificate lifecycle. Level: zero lapses in the period. Measure: the renewal inventory walked at each monthly report.
- **OPS-SVC-005**: Monthly operations reporting. Level: a status report at each month end stating service levels, effort against the 20% cap, and spend against the 12,000 USD envelope. Measure: the report's presence and completeness per month.
- **OPS-SVC-006**: CI health. Level: known transient failure classes self-retry once, and any workflow failure surfaces in the self-closing alert issue within 30 minutes. Measure: sentinel sweep logs and the alert issue's history.
