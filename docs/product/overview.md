# Product Overview

> Design baseline · 1 October 2026 · Implementation evidence pending

## Purpose and users

Student Life RPG is a university-life management application combining academic planning, personal finance and RPG progression. Its primary user is a university student managing courses, deadlines, grades and everyday spending.

The product aims to reduce switching between separate tools and make completed study tasks visible through character growth. The proposed experience is portrait-oriented, with a 2.5D pixel-art world and accessible conventional feature screens.

## Core modules

| Module | User value | Alpha boundary |
| --- | --- | --- |
| RPG World | A personal space that connects everyday tools | Movement, collision, interaction prompts, scenes and fixed HUD |
| Academic | A single view of academic obligations | Semesters, courses, assignments, exams, calendar and GPA |
| Finance | Awareness of spending and remaining budget | Income, expenses, monthly budgets and summaries |
| Gamification | Visible recognition of completed tasks | EXP, coins, levels and player progress |

## Experience principles

- Real-life functions remain accessible through regular navigation as well as scene interactions.
- Completing a task provides explicit feedback; saving must succeed before the UI reports success.
- HUD elements remain anchored to the screen while the world camera moves.
- Furniture and room boundaries block movement; approaching an object reveals an interaction prompt.
- Important information uses text as well as color or animation.

The proposed scene arrangement is a bedroom with a functional-hall entrance. The hall provides academic and finance access. Exact scene geometry will be verified against imported assets and code.

## Scope control

The Alpha must demonstrate one complete journey: create a task, view it, complete it, apply a reward once, refresh progress, restart and retain data. Finance and GPA must also provide independently verifiable business rules.

Cloud accounts, sync, AI assistants, social features, leaderboards, multiplayer, a shop and a complex farming system are outside Alpha scope. Garden imagery may remain part of the visual design without introducing a separate gameplay dependency.

## Success criteria

| Goal | Demonstrable evidence |
| --- | --- |
| Useful academic planning | Correctly dated courses, tasks and exam entries |
| Reliable finance | Correct totals and budget calculations |
| Meaningful progression | Completion changes progress once |
| Durable local data | Saved records survive application restart |
| Clear engineering process | Requirements linked to issues, PRs and tests |

## Open decisions

Confirm the grading scale, target demo platform, supported device sizes, course recurrence rules, SDK version and existing implementation before treating those details as established facts.

[Requirements](requirements.md) · [User stories](user-stories.md) · [Product index](README.md)
