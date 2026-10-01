# Git Workflow and Code Review

> Team working agreement. Repository enforcement settings are not yet configured.

## Normal development

1. Select an issue with a requirement ID, scope and acceptance criteria.
2. Assign one main development issue per person at a time.
3. Create a branch from current main; use feature/<issue>-<description>, fix/<issue>-<description> or docs/<issue>-<description>.
4. Keep changes focused and update the relevant documentation.
5. Open a PR linking the issue, explain behavior and record validation.
6. Obtain review from at least one teammate; request affected module owners for shared-contract changes.
7. Resolve comments and applicable failing checks, then merge using the agreed repository merge method.

Direct main commits are limited to initial repository setup. After that, code and substantive documentation changes follow review. This document does not claim that branch protection is enabled.

## Issue contents

Include the user-visible problem, requirement/story reference, module, scope, dependencies, acceptance criteria and validation plan. Bugs also need reproduction steps, expected/actual behavior, revision and environment.

Priority meanings: P0 is necessary for the Alpha acceptance journey; P1 supports it after P0; P2 is deferred polish or expansion. These labels are planning priorities, not severity ratings.

## PR review

| Area | Reviewer checks |
| --- | --- |
| Behavior | Acceptance criteria and failure paths are handled |
| Boundaries | UI does not query SQL; shared contracts remain coherent |
| Data | Constraints, migrations and transaction behavior are covered |
| Evidence | Executed checks are distinguishable from planned checks |
| Documentation | Requirements, decisions and progress reflect the change |
| Hygiene | No credentials, personal records, build outputs or unrelated edits |

Use concise commit messages such as feat(academic): add course validation or docs: define reward policy. Resolve conflicts on the working branch and rerun affected checks. Do not rewrite shared history or force-push main.

## Definition of ready

Scope, owner, dependencies, acceptance criteria and affected contracts are known.

## Definition of done

Implementation is reviewed, applicable checks have executed successfully, acceptance evidence is linked and documentation is updated. An issue with code merged but no acceptance evidence is implemented, not verified.

[Development index](README.md)
