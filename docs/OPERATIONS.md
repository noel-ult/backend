# backend: verification and operations

Reviewed against [default-branch commit 80beed4a8da4](https://github.com/noel-ult/backend/commit/80beed4a8da4cfa75017405da787c9c17e56ab05) on 2026-10-28. Start with the [developer guide](../README.md) for installation and architecture, and the [source reference](REFERENCE.md) for exact scripts, configuration readers, routes, and source locations.

## Employee API

Check /api/health, then create, read, update, and delete a disposable employee. Compare primary /api/employees envelopes with compatibility /api/employeelist responses.

These are acceptance scenarios for a maintainer to run in the documented environment. Their inclusion is not a claim that live integrations or production credentials were tested during this documentation update.

## Deployment and failure diagnosis

Use Casestudy2 as the working directory. The Angular assets are prebuilt; the source required to rebuild that UI is absent.

## Maintaining the contract

When behavior changes, update the guide and examples in the same PR. Check the entry point and working directory before copying commands. Use the linked source readers to distinguish build-time configuration from process environment. For failures, capture the first application error, runtime version, selected mode, and redacted configuration names before later proxy or port errors.

Keep changes tied to evidence: a declared command is not proof it passes, a process health response is not a successful end-to-end workflow, and a historical report describes its own revision. Record actual check results and any unavailable external services in the PR.
