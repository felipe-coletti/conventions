# Commits

Commits follow [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/).

## Format

```
<type>(<scope>): <description>

[body]

[footer]
```

- `type` is required. `scope` is optional.
- `description` is lowercase, imperative ("add", not "added") and has no trailing period.
- `body` explains what changed and why, when it is not obvious.
- `footer` holds `BREAKING CHANGE:` notes and issue references.

## Types

| Type | Use for |
| --- | --- |
| `feat` | A new feature |
| `fix` | A bug fix |
| `docs` | Documentation only |
| `style` | Formatting, whitespace; no change in behavior |
| `refactor` | Code change that neither fixes a bug nor adds a feature |
| `perf` | Performance improvement |
| `test` | Adding or fixing tests |
| `build` | Build system or dependencies |
| `ci` | CI configuration |
| `chore` | Maintenance that does not touch source or tests |
| `revert` | Reverting a previous commit |

## Breaking changes

Add `!` after the type or scope, and describe it in the footer:

```
feat(api)!: remove v1 endpoints

BREAKING CHANGE: clients must migrate to /v2.
```

## Examples

```
docs: add LICENSE
feat(auth): add login form
fix(nav): close menu on outside click
refactor: extract form validation into its own script
```