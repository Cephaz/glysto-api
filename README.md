![Version 0.5.0](https://img.shields.io/badge/version-0.5.0-2ea44f)

## Installation

```bash
poetry install
```

## Environment files

Use one `.env` for local and Docker:

```bash
cp .env.example .env
```

## Full Docker (Django + PostgreSQL):

```bash
docker compose up --build
```

## Demarrage Django + users auth basique

Commandes utiles:

```bash
poetry run python manage.py startapp users
```

Ajoute ensuite `"users"` dans `INSTALLED_APPS` dans `config/settings.py`, puis:

```bash
poetry run python manage.py makemigrations
poetry run python manage.py migrate
poetry run python manage.py createsuperuser
```

Pour lancer le serveur:

```bash
poetry run python manage.py runserver
```

## Local git hook

Install the commit message hook:

```bash
poetry run pre-commit install --hook-type commit-msg
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

Endpoints:

- `POST /api/auth/register/`
- `POST /api/auth/login/`
- `POST /api/auth/refresh/`
- `GET /api/auth/me/`

Use token Bearer for protected routes:

```bash
Authorization: Bearer <access_token>
```
