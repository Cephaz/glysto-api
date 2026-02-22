# glysto-api

Version: `0.1.0`

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
