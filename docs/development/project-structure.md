# Project Structure and Ownership

> This record deliberately leaves actual code paths blank until the application is imported.

## Actual application directory

<!-- Intentionally blank: audited application directory tree. -->

## Module paths

| Area | Actual path | Responsibility |
| --- | --- | --- |
| App composition | | Routing, startup and dependency wiring |
| Academic | | Academic entities, views and rules |
| Finance | | Transactions, budgets and summaries |
| RPG World | | Movement, collision, scenes and interaction |
| Gamification | | Progress, reward rules and grants |
| Persistence | | Database connection, mappings and migrations |
| Automated tests | | Tests organized by behavior and boundary |
| Assets | | Approved images, sprites, fonts and attribution |

## Structure rules

Feature ownership should be clear; UI, application rules and data access must have explicit boundaries. Only genuinely cross-feature contracts belong in shared code. Assign an owner before changing common models or database migrations.

After import, record exact existing paths and entry points. A directory reorganization must preserve behavior and be justified separately from document creation.

[Development index](README.md)
