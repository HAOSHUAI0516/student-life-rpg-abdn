# Team Responsibilities

Planning baseline: 2 October 2026. Application development has not started. Existing frontend images may be reused after checking their source and suitability; they do not count as implemented features.

## Owners and delivery dates

All dates below are in 2026, China Standard Time (UTC+8). Dates are internal acceptance targets; submit PRs two days earlier.

| Member | Responsibilities | Internal acceptance targets |
| --- | --- | --- |
| 陈思翰 | Flutter setup, shared architecture, routing, bedroom game core, final integration | Oct 9 baseline; Oct 25 bedroom; Dec 3 integration |
| 廖梦溪 | Keyboard/joystick movement, collision, walkable areas, scene boundaries | Oct 25 movement; Nov 8 feature room; Nov 22 platform refinements |
| 黎宇轩 | Reusable interaction, entrances, navigation protection, HUD and EXP/Level UI | Oct 25 interaction; Nov 8 HUD; Nov 22 progression UI |
| 蒋子康 | Semester/Course, weekly timetable, week rules, Assignment/Exam and tests | Oct 25 CRUD; Nov 8 timetable integration |
| 钟顺成 | Task/Event, calendar, timeline, overlap layout, duration and recurrence | Oct 25 CRUD; Nov 8 calendar/timeline; Nov 22 recurrence/duration |
| 郝文聪 | Conflict/free-slot algorithms, splitting, scheduling, GPA and simulation | Oct 25 contracts/tests; Nov 8 conflict/free-slot/GPA; Nov 22 advanced algorithms |
| 吴昕玥 | Finance CRUD, categories, validation, month filters, budgets and tests | Oct 25 CRUD; Nov 8 budgets/summaries |
| 龙梓瑄 | Dashboard, academic/task/finance statistics, charts and tests | Oct 25 metrics/contracts; Nov 8 dashboard; Nov 22 charts |
| 李雨真 | Repositories, storage, serialization, import/export, backup/reset, CI and builds | Oct 9 storage proof; Oct 25 persistence; Nov 8 integration/CI; Nov 22 backup; Dec 3 builds |

GitHub handles are not yet recorded. Do not infer an account from a name. 学号 are omitted from this public planning document.

## Review and coordination

The project lead (the user coordinating this repository) reviews all other members' PRs and signs off milestone acceptance. Record the lead's GitHub account in the project settings. A teammate must review the lead's own PRs; its author cannot approve their own PR. The lead's development responsibilities remain those of their proposal assignment; no identity mapping is assumed here.

- Keep at most one main implementation issue active per person.
- Every PR includes its issue, acceptance evidence, checks run and limitations.
- Shared-model/storage changes require input from affected module owners before lead review.
- Report blockers within one working day and agree interface changes before implementation.
- Each member provides weekly report evidence: design decisions, screenshots, test results and issue/PR links.
- Public reports use synthetic demonstration data.

## Shared responsibilities requiring confirmation

Proposed reward ownership: 陈思翰 owns completion/reward business rules, 李雨真 owns atomic persistence and duplicate-grant prevention, and 黎宇轩 owns HUD/EXP/Level presentation. Confirm this assignment in the baseline issue before implementation; acceptance target Nov 22.

Grade scale, recurrence semantics, reward policy, SDK versions, scene engine and state-management choice must be recorded before dependent work begins. Keep proposal requirements traceable; scheduling, target-GPA feasibility, export/import and Android/Windows release delivery are explicit project commitments.

[Roadmap](roadmap.md) · [Baseline tasks](baseline-issues.md) · [Management index](README.md)
