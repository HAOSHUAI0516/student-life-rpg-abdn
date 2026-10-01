# Test Strategy

> Planned verification. Execution results remain blank in the test-case record.

## Scope and levels

| Level | Focus | Evidence |
| --- | --- | --- |
| Unit | GPA, money arithmetic, budgets, rewards and level thresholds | Deterministic rule tests with boundary cases |
| Repository | Queries, constraints, transactions and migrations | Isolated database fixtures and failure cases |
| Widget | Forms, empty states, validation and navigation | Rendered state and input assertions |
| Integration | Task-to-progress journey and persistence after restart | Executed end-to-end record |
| Manual scene | Collision, interaction range, camera and fixed HUD | Device/environment and annotated recording |

Pure rule and repository tests provide most feedback. Integration and manual tests cover the boundaries they cannot establish. Exact test libraries and CI commands are chosen after app import.

## Risk-led priorities

1. Duplicate rewards and partial persistence.
2. Incorrect GPA or finance arithmetic.
3. Loss of records on restart or migration.
4. Calendar date and recurrence errors.
5. Character clipping, stuck movement and wrong interaction targets.
6. Misleading success messages after failures.

Use synthetic records only. Separate each database test from prior runs. Fix the clock and locale when asserting date-dependent results. Exercise rapid repeated taps as well as normal input.

## Alpha acceptance gate

All P0 requirements have passing evidence on the selected revision and target. No unresolved defect blocks persistence, correct calculations, task rewards or basic navigation. P1 omissions are listed explicitly. The demo can be reproduced from the setup guide.

## Automation plan

After source import, configure formatting, analysis, applicable automated tests and a target build check. Required checks must use the app's actual directory and pinned SDK. Do not display a passing CI badge before a workflow has run successfully.

## Result-recording rules

Record requirement IDs, issue/PR, test ID, revision, environment, execution time, actual result and evidence. Planned and not-run cases are not passes. A failed case names a defect or investigation issue.

[Test cases](test-cases.md) · [Testing index](README.md)
