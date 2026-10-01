# Contributing to Student Life RPG

Start with the [product baseline](docs/product/overview.md), [requirements](docs/product/requirements.md) and [Git workflow](docs/development/git-workflow.md).

## Before development

Choose one assigned issue with clear acceptance criteria. Confirm shared-model changes with the owner. Develop on a dedicated feature, fix or docs branch; keep unrelated changes separate.

## Before opening a PR

- Link the issue and relevant requirement/test IDs.
- Explain the resulting behavior and failure handling.
- Run applicable checks once commands are established; report exactly what ran.
- Update affected documentation and include UI evidence for visible changes.
- Review your changes for secrets, personal data, generated artifacts and unapproved assets.

Request teammate review before merging. Repository initialization is the documented direct-main exception. Protection and CI enforcement will be configured separately; their absence does not remove the review agreement.

## Reporting bugs

Use a reproducible synthetic example, identify environment and revision, state expected/actual behavior, and attach relevant sanitized evidence. Never include passwords, tokens or personal student records.

## Documentation conventions

Use clear headings, relative links and compact tables. Label proposed decisions explicitly. Record implementation paths and results only after verification. Keep requirement IDs stable and link superseded decisions instead of silently overwriting them.

[Setup record](docs/development/setup.md) · [Test strategy](docs/testing/strategy.md)
