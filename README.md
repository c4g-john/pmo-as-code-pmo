# PMO as Code, governed by PMO as Code

This repository is the governing document set for the PMO as Code portfolio
itself: five projects covering the engine, the standard, adoption, operations,
and this governance layer. Every document here is validated by
[docassert](https://github.com/c4g-john/docassert), gated in CI, and derived
into a public status dashboard — the same mechanics we recommend to adopters,
applied to ourselves.

## The portfolio

| Project | Outcome |
|---|---|
| `PRJ-001-GOV` Self-governance | This repo, its gates, dashboard, and bridge wiring |
| `PRJ-002-ENG` Engine 1.0 | docassert to a stable 1.0 (package, action, tap) |
| `PRJ-003-STD` Standard 1.0 | The specification and conformance suite to 1.0 |
| `PRJ-004-ADO` Launch and adoption | Site parity, public launch, first external adopters |
| `PRJ-005-OPS` Portfolio operations 2026-H2 | Period-chartered keep-the-lights-on |

Governance lives here; product truth lives in each component repository. The
[Refuge for Humans](https://github.com/c4g-john/refuge-for-humans-pmo) case
study is governed separately in its own repository.

## How this repo works

Documents follow the [PMO as Code spec](https://github.com/c4g-john/pmo-as-code-spec).
Pull requests are gated by `docassert validate` (changed documents) and
`docassert consistency` (the cross-document graph), with AI alignment
advisories when documents change. The dashboard is derived by `docassert
pages` and published on merge. Scope changes happen here first, by pull
request, with the sponsor's merge as sign-off.
