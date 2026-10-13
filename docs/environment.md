# Environment

Every project that reads environment variables ships a `.env.example` at its root. The real `.env` is never committed.

## Rules

- Variable names are `SCREAMING_SNAKE_CASE`, prefixed by the group they belong to (`APP_`, `DB_`, ...).
- No spaces around `=`: `APP_PORT=8080`, never `APP_PORT = 8080`.
- Variables are grouped under a `# Group` comment, with a blank line between groups.
- Safe defaults (host, port, environment) are filled in.
- Secrets (users, passwords, keys) are left empty or set to an obvious placeholder such as `your_api_key_here`.
- Add `.env` to `.gitignore`.

## Template

Copy [`templates/.env.example`](../templates/.env.example):

```dotenv
# Application
APP_NAME=my-app
APP_ENV=development
APP_PORT=8080

# Database
DB_HOST=localhost
DB_PORT=5432
DB_USER=
DB_PASSWORD=
DB_NAME=
DB_SSLMODE=disable

# External
API_KEY=your_api_key_here
```

## Variable Reference

| Variable                  | Description                                     |
| ------------------------- | ----------------------------------------------- |
| `APP_NAME`                | Application name, in `kebab-case`               |
| `APP_ENV`                 | `development`, `staging` or `production`        |
| `APP_PORT`                | Port the application listens on                 |
| `DB_HOST` / `DB_PORT`     | Database address                                |
| `DB_USER` / `DB_PASSWORD` | Database credentials                            |
| `DB_NAME`                 | Database name                                   |
| `DB_SSLMODE`              | SSL mode for the connection (`disable` locally) |
| `API_KEY`                 | Key for an external API                         |