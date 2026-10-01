# Test Cases and Requirements Traceability

> Test specifications are populated. Issue/PR links and execution results are intentionally blank.

## Designed cases

| ID | Requirement | Preconditions and action | Expected result |
| --- | --- | --- | --- |
| TC-ACA-001 | FR-ACA-001 | Existing semester; save a course with positive credits, then restart | Course exists once in the selected semester |
| TC-ACA-002 | FR-ACA-001 | Save zero or negative course credits | Validation message; no inserted course |
| TC-ACA-003 | FR-ACA-002 | Create and edit a dated entry; inspect both dates | Entry appears only on its updated date |
| TC-ACA-004 | FR-ACA-004 | Create an assignment/exam for an existing course; edit it | Valid association and updated saved values |
| TC-ACA-005 | FR-ACA-005 | Use grade points 4.0/3.0 and credits 3/2 under a confirmed scale | GPA equals 3.6 before display rounding |
| TC-ACA-006 | FR-ACA-005 | No eligible graded credits | No GPA displayed; no divide-by-zero |
| TC-FIN-001 | FR-FIN-001 | Save expense 12.34 in a currency with two minor digits | Exact saved value 1234 minor units; one record |
| TC-FIN-002 | FR-FIN-001 | Save an invalid amount or simulate write failure | Clear error; no success feedback or invalid write |
| TC-FIN-003 | FR-FIN-002 | Budget 100.00; matching expenses 35.50; unrelated income/category | Remaining 64.50; unrelated records excluded |
| TC-FIN-004 | FR-FIN-003 | Income 200.00; expenses 35.50 in selected period | Income 200.00, expenses 35.50, net 164.50 |
| TC-GAM-001 | FR-ACA-003, FR-GAM-001 | Complete an eligible task twice, including rapid repeated input | Exactly one grant and one progress increment |
| TC-GAM-002 | NFR-REL-001 | Inject write failure during completion transaction | Completion, grant and progress all roll back |
| TC-GAM-003 | FR-GAM-002 | Complete task, inspect HUD, restart and inspect progress | HUD and persisted progress agree |
| TC-RPG-001 | FR-RPG-001 | Move into each wall and furniture boundary; move diagonally along wall | No overlap; unblocked movement remains possible |
| TC-RPG-002 | FR-RPG-002 | Approach, activate and leave an entrance's interaction range | Prompt appears/disappears correctly; target opens once |
| TC-RPG-003 | FR-RPG-003 | Move character and camera | HUD remains in its screen position |
| TC-DAT-001 | FR-DAT-001 | Save academic/finance/progress records; restart | Saved records and values remain unchanged |
| TC-DAT-002 | NFR-DAT-001 | Upgrade an old supported schema fixture | Records preserved; version updated correctly |
| TC-USE-001 | NFR-USE-001 | Open core modules through regular navigation | Core actions accessible without scene movement |
| TC-MNT-001 | NFR-MNT-001 | Review presentation imports and persistence calls | Persistence accessed through approved contracts |
| TC-SEC-001 | NFR-SEC-001 | Review changes and test fixtures | No credentials or personal student records committed |

## Traceability links

| Requirement group | Test cases | Issue | Implementation PR |
| --- | --- | --- | --- |
| Courses, calendar and GPA | TC-ACA-001–006 | | |
| Finance | TC-FIN-001–004 | | |
| Completion and progress | TC-GAM-001–003 | | |
| RPG interaction | TC-RPG-001–003 | | |
| Persistence and migrations | TC-DAT-001–002 | | |
| Usability and maintainability | TC-USE-001, TC-MNT-001 | | |
| Repository hygiene | TC-SEC-001 | | |

## Execution results

| Test ID | Revision | Environment | Executed at | Actual result | Pass/Fail | Evidence/defect |
| --- | --- | --- | --- | --- | --- | --- |
| | | | | | | |

<!-- Results deliberately left blank. No test has been certified by this documentation commit. -->

[Testing index](README.md)
