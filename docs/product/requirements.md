# Requirements Baseline

> Proposed Alpha requirements. All implementation status is pending verification.

## Functional requirements

| ID | Requirement | Acceptance criterion | Priority |
| --- | --- | --- | --- |
| FR-ACA-001 | Manage semesters and courses | Valid courses reference a semester; invalid credit values are rejected | P0 |
| FR-ACA-002 | View academic entries in a calendar | Courses, tasks and exams appear on the correct local date and time | P0 |
| FR-ACA-003 | Create and complete academic tasks | A saved task can be completed and remains complete after restart | P0 |
| FR-ACA-004 | Record assignments and exams | Records reference an existing course and can be edited or removed with confirmation | P1 |
| FR-ACA-005 | Calculate credit-weighted GPA | Use the selected grading scale and include only eligible graded courses; no eligible credits displays no GPA | P0 |
| FR-FIN-001 | Record income and expenses | Positive amounts and valid categories save correctly; invalid input leaves data unchanged | P0 |
| FR-FIN-002 | Manage monthly budgets | One active budget per category and month; remaining budget equals limit minus matching expenses | P1 |
| FR-FIN-003 | View financial summaries | Income, expenses and net balance match saved transactions for the selected period | P0 |
| FR-GAM-001 | Award task-completion rewards | First eligible completion awards EXP and coins exactly once | P0 |
| FR-GAM-002 | Display player progress | HUD and progress view agree with saved EXP, coins and level | P0 |
| FR-RPG-001 | Move the character within boundaries | Movement stops at walls and furniture and allows sliding along an unobstructed wall | P0 |
| FR-RPG-002 | Interact with functional areas | A prompt appears in range; activating it opens the intended module or scene | P0 |
| FR-RPG-003 | Keep HUD anchored to the screen | Camera and character movement do not move the HUD | P0 |
| FR-DAT-001 | Persist records locally | Saved records survive a normal restart without a backend connection | P0 |

P0 means required for the Alpha acceptance journey; P1 means supporting functionality delivered after P0 is stable. Priorities do not indicate completed work.

## Non-functional requirements

| ID | Requirement | Verification method |
| --- | --- | --- |
| NFR-REL-001 | Task completion, reward ledger and progress update commit atomically | Force a write failure and verify that no partial reward remains |
| NFR-USE-001 | Essential actions work without navigating the RPG world | Walk through equivalent regular navigation |
| NFR-USE-002 | Validation and save failures give actionable text feedback | Inspect invalid forms and simulated failures |
| NFR-MNT-001 | UI accesses persistence through repository interfaces | Review imports and repository tests |
| NFR-SEC-001 | No credentials or personal data are committed as fixtures | Inspect staged changes; use synthetic records |
| NFR-DAT-001 | Schema upgrades preserve supported existing records | Run migration fixtures when schema changes |
| NFR-PER-001 | Routine input, navigation and scene movement meet agreed responsiveness targets | Define numeric thresholds and reference devices before measurement |

Performance thresholds are not invented here; record them when the demo platform is selected. Local storage alone does not provide encryption or backup.

## Rules to settle before implementation

- GPA conversion table and eligibility of ungraded or failed courses.
- Calendar recurrence, overnight courses and timezone behavior.
- Assignment-to-task identity and behavior on cancellation or deletion.
- Reward values, level thresholds and correction policy.
- Supported currency and minor-unit precision.

The proposed default reward policy is: first completion grants one reward; a later status correction grants no second reward and does not automatically reverse the first one. Approve this policy in the implementing issue.

## Traceability

Use the [test-case traceability table](../testing/test-cases.md). Record actual issue and PR references only after they exist. A requirement is verified only when its evidence names the tested revision and result.

[Product index](README.md)
