# Delivery Roadmap

> Phases use acceptance gates, not invented dates or completion claims.

| Phase | Deliverables | Exit gate |
| --- | --- | --- |
| Foundation | Product baseline, architecture, collaboration guide, issue/PR templates and test specifications | Team reviews scope and identifies open decisions |
| Runnable baseline | Import existing app; record real structure, versions and setup | Clean checkout starts on agreed target |
| Connected Alpha | Complete P0 academic, finance, persistence and progression journeys | Core user journeys work after restart |
| Verified demo | Run planned checks, address blocking defects, add applicable CI, screenshots and demo | P0 evidence names revision and environment |
| Cloud evaluation | Assess identity, sync and backend scope | Approved decision before cloud implementation |

## Recommended work sequence

Agree shared models and grading/reward policies first. Establish persistence and contracts. Develop academic, finance and RPG modules against those contracts. Integrate atomic completion and HUD updates. Execute acceptance tests, then polish the demo.

Document changes and code changes advance independently: specification completion does not imply feature completion. Existing work in an earlier repository must be imported and verified before its status is carried into this repository.

## Release checklist

- P0 requirements verified; P1 omissions disclosed.
- Setup checked by a teammate from a clean checkout.
- Test evidence identifies the demo revision and target.
- Screenshots and demo represent that revision.
- Asset sources and permissions documented.
- Known limitations recorded without hiding failed behavior.

## Tracking

Use issues and milestones for delivery. Link requirements and PRs in each issue; keep a shared planning record consistent with GitHub. A milestone closes only after its exit gate is satisfied.

[Responsibilities](team.md) · [Risks](risks.md) · [Management index](README.md)
