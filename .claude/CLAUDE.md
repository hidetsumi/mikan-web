# mikan-web — Shared Context

## Repos
- **This repo (Frontend):** https://github.com/hidetsumi/mikan-web (React + TanStack Start)
- **Backend API:** https://github.com/hidetsumi/mikan-api (NestJS + Prisma + PostgreSQL)
- **GitHub Project (kanban):** https://github.com/users/hidetsumi/projects/6

## Branch conventions

Format: `type/MKN-{issue-number}-short-description`

| Branch | Purpose |
|--------|---------|
| `main` | Production — protected, merge only from release branches |
| `develop` | Integration — all PRs target this branch |
| `feature/MKN-{n}-description` | New functionality |
| `fix/MKN-{n}-description` | Bug fixes |
| `chore/MKN-{n}-description` | Config, deps, tooling |
| `release/vX.Y.Z` | Release candidates |

Examples:
```
chore/MKN-1-init-tanstack-start
feature/MKN-10-auth-login-page
feature/MKN-11-todo-list
```

## Commit conventions
Follow Conventional Commits: `type(scope): description`
- `feat:`, `fix:`, `chore:`, `test:`, `docs:`, `refactor:`
- Scope is domain-based: `auth`, `todos`, `rooms`, `ui`
- Example: `feat(auth): add login form`

> Note: PR titles are auto-formatted by the `link-issue` workflow as `type(MKN-###): description`. This is different from commit message scopes (which are domain-based).

## Versioning
- Tags: `v0.1.0`, `v0.2.0` ... `v1.0.0`
- Release flow: `release/vX.Y.Z` branch → tag `vX.Y.Z-rc.1` → QA → merge to `main` → tag `vX.Y.Z`

## Milestones
| Milestone | Focus |
|-----------|-------|
| v0.1.0 | Fundación — setup, CI/CD, deploy base |
| v0.5.0 | Frontend mínimo — auth + todo list |
| v1.0.0 | Release — docs, E2E, tag |
