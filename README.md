<div align="center">

# 🎓 Student Life RPG

### Make everyday progress part of your adventure.

**学业规划 · 个人财务 · 角色成长**

A gamified university-life application that brings academic planning,
personal finance and RPG progression into one interactive experience.

![Stage](https://img.shields.io/badge/Stage-Repository_Setup-7C3AED?style=flat-square)
![Approach](https://img.shields.io/badge/Alpha-Local_First-0F766E?style=flat-square)
![UI](https://img.shields.io/badge/Planned_UI-Flutter-02569B?style=flat-square)
![Storage](https://img.shields.io/badge/Planned_Storage-SQLite-003B57?style=flat-square)

[Explore the docs](docs/README.md) · [Product](docs/product/README.md) · [Architecture](docs/architecture/README.md) · [Development](docs/development/README.md)

</div>

---

## The idea

University life is spread across timetables, deadlines, grades and spending records. **Student Life RPG** is designed to bring these together in a mobile application, with a pixel-art RPG world that connects everyday actions to visible character growth.

**Plan your day. Complete meaningful tasks. Watch your character grow.**

> **Current stage — repository foundation.** This repository currently contains the documentation structure. The modules and architecture below describe the proposed Alpha; application source code, a runnable build and executed test evidence have not yet been added here.

## One world, four connected modules

| Module | Student experience | Planned Alpha scope |
| :--- | :--- | :--- |
| **RPG World** | Explore a personal space and access everyday tools | Character movement, collision, interaction prompts, scene navigation and a fixed HUD |
| **Academic** | Keep courses, deadlines and academic progress together | Courses, assignments, exams, calendar and credit-weighted GPA |
| **Finance** | Understand where money goes | Income, expenses, budgets and basic summaries |
| **Gamification** | Turn completed tasks into visible progress | Task completion, EXP, coins, levels and persisted player progress |

The proposed visual direction is a **portrait, 2.5D pixel-art experience**. Real application screenshots and a demo will be added after the existing implementation is imported and verified.

## A complete Alpha journey

1. Create an academic task with a deadline.
2. See it in the academic view and calendar.
3. Mark the task as complete.
4. Apply its reward once and update player progress.
5. See the new EXP or level in the RPG HUD.
6. Restart the app and retain the completed task and progress.

**Acceptance focus:** saved data survives restart, repeated completion cannot duplicate rewards, and the displayed state agrees with the stored state. These are delivery targets, not recorded test results.

## Architecture at a glance

The proposed Alpha uses a local Flutter application. Feature screens and RPG interactions access business logic through controllers; repository interfaces isolate persistence from the UI.


```mermaid
flowchart TD
  World["RPG world"] --> State["Controllers and business rules"]
  Academic["Academic screens"] --> State
  Finance["Finance screens"] --> State
  State --> Records["Academic and finance repositories"]
  State --> Progress["Player progress repository"]
  Records --> DB[("Local SQLite")]
  Progress --> DB
```

| Boundary | Responsibility |
| :--- | :--- |
| Presentation | Screens, forms, RPG rendering and user input |
| Controllers and rules | Validation, GPA calculations, task completion and rewards |
| Repository interfaces | Stable contracts for reading and updating feature data |
| Local persistence | SQLite queries, transactions and migrations |

**Future extension:** FastAPI, PostgreSQL, authentication and cloud synchronization will be evaluated in a later phase. Cloud synchronization requires an explicit design for identity, conflicts and offline updates.

[Read the architecture documentation →](docs/architecture/README.md)

## Documentation hub

| Start here | What you will find | Current state |
| :--- | :--- | :--- |
| [Documentation index](docs/README.md) | A single entry point to all engineering documents | Available |
| [Product](docs/product/README.md) | Scope, requirements and acceptance criteria | Section initialized |
| [Architecture](docs/architecture/README.md) | Proposed layers, data flows, schema and decisions | Section initialized |
| [Development](docs/development/README.md) | Setup, actual code structure and Git workflow | Section initialized |
| [Testing](docs/testing/README.md) | Test strategy, cases and verification evidence | Section initialized |
| [Project management](docs/project-management/README.md) | Delivery phases, ownership and risks | Section initialized |

Detailed documents will be linked as they are written and checked against the implementation.

## Delivery roadmap

| Phase | Outcome | Exit criteria | Status |
| :--- | :--- | :--- | :--- |
| **01 · Foundation** | A readable repository and agreed collaboration process | Documentation index, contribution guide, issue and PR templates | In progress |
| **02 · Runnable baseline** | Existing Flutter work imported and reproducible | Verified setup steps and a successful local run | Planned |
| **03 · Connected Alpha** | Academic, finance and RPG progress work together | Core journeys persist data and provide correct feedback | Planned |
| **04 · Verified demo** | A reviewable course-project release | Executed tests, applicable CI checks, screenshots and demo | Planned |
| **05 · Cloud extension** | Evaluate accounts and synchronization | Approved architecture decision and a scoped implementation plan | Future |

## Development and contribution

The team workflow is **Issue → Branch → Pull Request → Review → Merge**. Each development issue should define acceptance criteria; each PR should include validation evidence and update the affected documents.

The documentation setup uses direct commits as a bootstrap exception. Branch protection, issue templates, PR templates and CI are not configured yet.

<details>
<summary><strong>Running the application</strong></summary>

Application source code is not present in this repository yet. Exact prerequisites, working directories and startup commands will be published in the [development documentation](docs/development/README.md) after the code is imported and the commands are verified.

</details>

<details>
<summary><strong>How we will demonstrate quality</strong></summary>

- Link requirements to issues, implementation PRs and test cases.
- Test GPA, budgets, task completion and reward rules.
- Verify persistence and complete user journeys.
- Check RPG movement, collision and interaction behavior.
- Record the tested revision, result and supporting evidence.
- Add automated checks once the application structure and SDK are confirmed.

See the [testing documentation](docs/testing/README.md). No passing-test, coverage or CI claims are made before execution.

</details>

---

<div align="center">

**Student Life RPG** · A university software engineering project

Build useful daily habits. Give progress a place in your world.

</div>
