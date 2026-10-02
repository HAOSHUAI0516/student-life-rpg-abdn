# Baseline Issue Drafts

These are prepared drafts, not issues already created on GitHub. Use the Engineering task template. Dates are 2026 CST. PR target dates allow review before the Oct 9 baseline acceptance. Assign accounts only after matching them to team members.

Create BASE-01, BASE-02 and BASE-03 first; coordinate independent specification tasks in parallel. Record actual GitHub issue numbers after creation. Do not infer numbers from these planning IDs.

## [Task]: BASE-01 Establish shared Flutter baseline

**Owner:** 陈思翰  
**PR / draft due:** Oct 7  
**Dependencies:** None

### Intended outcome and deliverables

Create a new Flutter application in the documentation repository without replacing its docs. Record SDK/tool decisions, Android/Windows targets, architecture and routing conventions.

### Acceptance criteria

A clean checkout starts on Android and Windows; unrelated documents remain intact; commit and environment evidence attached.

### Verification and documentation updates

Attach relevant checks and observed results, revision/environment details and affected documentation. Clearly label any checks not executed. Reviewer: project lead; the lead's own PR requires teammate review.

## [Task]: BASE-02 Agree domain models and module interfaces

**Owner:** 陈思翰; 李雨真 coordinates storage; all module owners contribute  
**PR / draft due:** Oct 7  
**Dependencies:** None; merge scaffolding after BASE-01

### Intended outcome and deliverables

Specify Semester/Course/Assignment/Exam/Task/Event, Finance and progression contracts, IDs, validation, time representation, grade scale, recurrence semantics and reward policy. Resolve proposal gaps before coding dependent modules.

### Acceptance criteria

Owners agree contracts; example inputs/outputs and invalid cases recorded; interfaces can be used by UI and algorithms; reward ownership confirmed.

### Verification and documentation updates

Attach relevant checks and observed results, revision/environment details and affected documentation. Clearly label any checks not executed. Reviewer: project lead; the lead's own PR requires teammate review.

## [Task]: BASE-03 Prove local persistence on both platforms

**Owner:** 李雨真  
**PR / draft due:** Oct 7  
**Dependencies:** BASE-01 and minimum BASE-02 contracts

### Intended outcome and deliverables

Choose a compatible local storage implementation; implement one repository round trip with synthetic data, serialization and startup reload.

### Acceptance criteria

Record survives app restart on Android and Windows; invalid data produces controlled failure; meaningful persistence test attached.

### Verification and documentation updates

Attach relevant checks and observed results, revision/environment details and affected documentation. Clearly label any checks not executed. Reviewer: project lead; the lead's own PR requires teammate review.

## [Task]: BASE-04 Inventory and integrate reusable images

**Owner:** 陈思翰; 廖梦溪 and 黎宇轩 contribute  
**PR / draft due:** Oct 7  
**Dependencies:** Inventory independent; integration needs BASE-01

### Intended outcome and deliverables

Inventory existing images, sources/permissions, dimensions and intended scenes. Agree scale and coordinate conventions; separate collision/interaction logic from image assets.

### Acceptance criteria

Assets load on both platforms; sources documented; missing sprites/states listed honestly; no existing movement or collision implementation claimed.

### Verification and documentation updates

Attach relevant checks and observed results, revision/environment details and affected documentation. Clearly label any checks not executed. Reviewer: project lead; the lead's own PR requires teammate review.

## [Task]: BASE-05 Specify academic and schedule contracts

**Owner:** 蒋子康; 钟顺成  
**PR / draft due:** Oct 7  
**Dependencies:** Coordinate with BASE-02

### Intended outcome and deliverables

Agree weekly occurrences, semester weeks, Assignment/Exam links, scheduled/unscheduled Task/Event representation and timeline input.

### Acceptance criteria

Examples cover teaching weeks, overlapping events and unscheduled tasks; no independent duplicate models; CRUD issue boundaries agreed.

### Verification and documentation updates

Attach relevant checks and observed results, revision/environment details and affected documentation. Clearly label any checks not executed. Reviewer: project lead; the lead's own PR requires teammate review.

## [Task]: BASE-06 Specify algorithm and GPA acceptance examples

**Owner:** 郝文聪  
**PR / draft due:** Oct 7  
**Dependencies:** Coordinate with BASE-02 and BASE-05

### Intended outcome and deliverables

Define conflict/free-slot/scheduling/GPA/simulation/feasibility inputs and outputs with hand-calculated examples. Specify scheduling constraints and impossible-target behavior.

### Acceptance criteria

Boundary and infeasible cases have expected outputs; grade scale is explicit; algorithms can be developed without UI dependencies.

### Verification and documentation updates

Attach relevant checks and observed results, revision/environment details and affected documentation. Clearly label any checks not executed. Reviewer: project lead; the lead's own PR requires teammate review.

## [Task]: BASE-07 Specify Finance and dashboard metrics

**Owner:** 吴昕玥; 龙梓瑄  
**PR / draft due:** Oct 7  
**Dependencies:** Coordinate with BASE-02

### Intended outcome and deliverables

Agree transaction signs/precision, categories, month boundaries, budget totals, dashboard summaries and empty-state behavior.

### Acceptance criteria

Hand-calculated finance examples agreed; metric sources and exclusions documented; dashboard reads module contracts rather than direct database tables.

### Verification and documentation updates

Attach relevant checks and observed results, revision/environment details and affected documentation. Clearly label any checks not executed. Reviewer: project lead; the lead's own PR requires teammate review.

## [Task]: BASE-08 Review baseline and prepare Update 1

**Owner:** Project lead reviews; all members supply evidence  
**PR / draft due:** Oct 11  
**Dependencies:** BASE-01 through BASE-07

### Intended outcome and deliverables

Review PRs by Oct 9, collect actual evidence and prepare the course update using the official form. Define report outline and remaining tasks.

### Acceptance criteria

Status reflects actual implementation; contributors and evidence links included; update ready Oct 11 and submitted by Oct 12 23:59 CST; submission receipt retained.

### Verification and documentation updates

Attach relevant checks and observed results, revision/environment details and affected documentation. Clearly label any checks not executed. Reviewer: project lead; the lead's own PR requires teammate review.

