# User Stories and Acceptance Criteria

> Stories specify desired behavior, not completed features.

## US-ACA-001 · Plan a course

As a student, I want to add a course to a semester so that I can organize my academic schedule.

- **Given** a semester exists, **when** a valid course is saved, **then** it belongs to that semester and is available after restart.
- **Given** invalid credits, **when** Save is pressed, **then** the error is explained and no course is inserted.

Requirements: FR-ACA-001, FR-DAT-001.

## US-ACA-002 · See deadlines together

As a student, I want courses, tasks and exams in one calendar so that I can identify upcoming commitments.

- **Given** entries on different dates, **when** I select a date, **then** only the matching entries are displayed with their type and time.
- **Given** an edited deadline, **when** the calendar refreshes, **then** the entry moves to the new date without a duplicate.

Requirement: FR-ACA-002.

## US-ACA-003 · Understand GPA

As a student, I want a credit-weighted GPA so that I can track academic performance.

- **Given** graded courses, **when** GPA is shown, **then** it matches the documented conversion table and weighted calculation.
- **Given** no eligible credits, **when** GPA is shown, **then** the UI displays an empty state rather than a misleading zero.

Requirement: FR-ACA-005.

## US-FIN-001 · Record an expense

As a student, I want to record a purchase so that I can understand my spending.

- **Given** a valid amount and date, **when** the expense is saved, **then** it appears in the list and selected-period totals.
- **Given** a storage failure, **when** Save is pressed, **then** success is not reported and my input remains available to retry.

Requirements: FR-FIN-001, FR-FIN-003, NFR-USE-002.

## US-FIN-002 · Track a budget

As a student, I want a category budget so that I can see my remaining allowance.

- **Given** a budget of 100.00 and matching expenses of 35.50, **when** its summary is shown, **then** the remaining amount is 64.50.
- **Given** an income transaction, **when** category expenses are summarized, **then** that income does not reduce the expense budget.

Requirement: FR-FIN-002.

## US-GAM-001 · Gain progress from completion

As a student, I want a completed study task to award progress so that the RPG reflects my effort.

- **Given** an incomplete eligible task, **when** completion commits, **then** one reward is recorded and HUD progress refreshes.
- **Given** the same completion request twice, **when** both are handled, **then** the total reward is unchanged after the first successful grant.
- **Given** a write failure, **when** completion fails, **then** neither task completion nor progress is partially committed.

Requirements: FR-ACA-003, FR-GAM-001, FR-GAM-002, NFR-REL-001.

## US-RPG-001 · Access useful tools

As a student, I want to approach a functional entrance and open its module so that exploration connects to useful actions.

- **Given** the character is outside interaction range, **when** I move closer, **then** a readable prompt appears in range.
- **Given** an active prompt, **when** I interact, **then** the intended module opens once.
- **Given** a wall or furniture obstacle, **when** movement is requested, **then** the character stays outside the obstacle.

Requirements: FR-RPG-001, FR-RPG-002, FR-RPG-003.

[Product index](README.md)
