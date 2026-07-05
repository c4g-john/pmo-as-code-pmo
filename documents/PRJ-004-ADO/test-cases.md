---
kind: test-cases
id: ADO-test-cases
project: PRJ-004-ADO
title: Launch and adoption — Test Cases
owner: johntanner
status: approved
---

## Overview

Verification for launch readiness and the adoption loop.

## Test Cases

- **ADO-TC-001** (tests: ADO-AC-001): Steps: list features from the engine changelog since 0.10, search the site for each. Expected: every feature has a documenting section.
- **ADO-TC-002** (tests: ADO-AC-002): Steps: open the self-governance page and follow every link. Expected: dashboard, five project pages, and the documents repository load and show current content.
- **ADO-TC-003** (tests: ADO-AC-003): Steps: diff every feature claim in the final announcement texts against the 1.0 changelog. Expected: no claim without a shipped feature.
- **ADO-TC-004** (tests: ADO-AC-004): Steps: at month end, capture template forks and action dependents with dates and record the status report. Expected: both figures present with retrieval dates and method link.
- **ADO-TC-005** (tests: ADO-AC-005): Steps: create a repository from the template, follow only the README, open a test pull request with a broken link, then fix it. Expected: the gate blocks then passes, and the dashboard deploys.
- **ADO-TC-006** (tests: ADO-AC-006): Steps: open /press/, diff every number and version against the live release, spec tag, and dashboards; request each former /handoff/ path. Expected: all claims match shipped artifacts; the handoff paths return 404.
- **ADO-TC-007** (tests: ADO-AC-007): Steps: open /press/ on desktop and a 375px viewport; view each asset preview; copy each boilerplate and announcement block; measure that no copy block requires horizontal scrolling. Expected: previews visible without downloading, copied text matches the rendered text, and no text block overflows its container.
- **ADO-TC-008** (tests: ADO-AC-008): Steps: build the site; grep built pages for script tags; cross-reference each against its PR justification. Expected: all pages static; every script justified.
- **ADO-TC-009** (tests: ADO-AC-009): Steps: crawl the pre-rewrite sitemap and press-kit URL list; request each; follow redirects; grep built HTML for href="#/". Expected: every URL lands on content via 200 or 301; zero fragment-routed links.
- **ADO-TC-010** (tests: ADO-AC-010): Steps: run the guidelines checklist per page (heading lint, landmark check, JS-disabled fetch diff, JSON-LD validator, date source audit); confirm llms.txt and sitemap.xml are build outputs. Expected: all checks pass on every page.
- **ADO-TC-011** (tests: ADO-AC-011): Steps: sample ten claims from the parity record across kept, corrected, and retired; verify each against artifacts; run the tells scan on all migrated prose. Expected: samples verify; scan reports zero violations.
