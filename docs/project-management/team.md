# Team Responsibilities

> Responsibility model proposed for the team. Names and GitHub handles are intentionally unassigned.

## Workstreams

| Workstream | Owns | Required coordination |
| --- | --- | --- |
| Product and integration | Scope, shared contracts, requirements and acceptance review | All modules |
| Academic | Courses, assignments, exams, calendar and GPA | Persistence and progression |
| Finance | Transactions, budgets and summaries | Persistence |
| RPG and UI | Scene, movement, collision, prompts, navigation and HUD | Progress contract and feature screens |
| Data and quality | Schema, migrations, repository checks, test evidence and CI | Every implementation owner |

Workstreams are responsibilities, not fixed headcounts or a change to existing departments. Map the team's nine members and three departments to them after confirming assignments. Keep one owner and one reviewer for each shared contract or migration.

## Assignment record

| Module/contract | Owner | Reviewer | GitHub handle |
| --- | --- | --- | --- |
| Shared academic models | | | |
| Finance models | | | |
| Task completion and rewards | | | |
| Database schema/migrations | | | |
| RPG scene and interaction | | | |
| UI navigation | | | |
| Test evidence and CI | | | |

## Collaboration rules

- Each person keeps at most one main development issue active.
- Shared-model changes receive affected-owner review before merge.
- Standups report completed evidence, current work and blockers.
- Use GitHub issues/PRs as the record of implementation and review; keep any supplementary team notes linked and consistent.
- Raise blocked dependencies early instead of changing a shared interface independently.

[Management index](README.md)
