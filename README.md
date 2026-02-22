![Version 0.4.0](https://img.shields.io/badge/version-0.4.0-2ea44f)

## Installation

```bash
poetry install
```

## Commit Naming Allowed

Allowed commit types:

- `feat`
- `fix`
- `docs`
- `style`
- `refactor`
- `test`
- `chore`
- `ci`
- `build`
- `perf`
- `revert`

Format:

`type(scope): message`

Example:

`feat(auth): add jwt login endpoint`

## CI

- Commit message lint runs on PRs.
- Version bump and tag run on `main` merges.

## Local git hook

Install the commit message hook:

```bash
poetry run pre-commit install --hook-type commit-msg
```
