# Architecture Decision Records

> Proposed design decisions for the new repository. These records do not certify implementation.

## ADR-001 · Use Flutter for the application

**Status:** Proposed baseline.

**Context:** The product combines forms, calendar views and an interactive mobile scene.

**Decision:** Use Flutter for application UI and module navigation. Confirm the scene engine after reviewing existing code.

**Alternatives:** Native applications offer platform-specific control but require separate implementations; a web-only app changes the intended mobile experience.

**Consequences:** One UI codebase can support the target experience. Platform setup, asset performance and scene rendering still require verification.

## ADR-002 · Deliver a local Alpha before cloud services

**Status:** Proposed baseline.

**Context:** A course demo must show a complete and reproducible business journey.

**Decision:** Alpha operates without a mandatory backend. Defer authentication and synchronization.

**Consequences:** Fewer runtime dependencies and easier offline demonstration. No cross-device synchronization or server-side backup is promised.

## ADR-003 · Isolate SQLite behind repositories

**Status:** Proposed baseline.

**Context:** Structured academic, finance and progression data need durable storage and atomic completion.

**Decision:** Use SQLite data implementations behind repository contracts, with explicit transactions and migrations.

**Alternatives:** Preferences are suitable for small settings but do not model these relational workflows; a remote database would add network and identity requirements.

**Consequences:** Local queries and atomic updates are available. Driver/platform compatibility, backup and migration behavior must be checked.

## ADR-004 · Organize work by feature with shared contracts

**Status:** Proposed baseline.

**Decision:** Academic, finance, RPG and progression own their feature logic. Shared domain contracts have one designated owner; changes require review from affected modules.

**Consequences:** Most changes stay within a module. Cross-feature contracts and reward transactions require deliberate coordination. Avoid adding abstract layers with no clear responsibility.

## ADR-005 · Make reward grants idempotent

**Status:** Proposed baseline.

**Decision:** Store a grant ledger with a unique task/reward identity; persist completion and progress atomically. UI animation is triggered after commit.

**Consequences:** Repeated input cannot duplicate a reward. Correction, deletion and future rule changes require explicit policies and tests.

## Decision change process

State the trigger, affected requirements, alternatives and consequences in a PR. Accepted decisions should name their approving issue/PR. Superseded records remain as history. Exact SDK, scene engine, state-management package, grading scale and reward values remain open.

[Architecture index](README.md)
