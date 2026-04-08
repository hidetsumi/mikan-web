# mikan-web

Frontend for the Mikan collaborative todo application. Built with TanStack Start (React, TypeScript, Vite, TanStack Router, TanStack Query). Consumes the [mikan-api](https://github.com/hidetsumi/mikan-api) REST API.

## Features

- **Auth** — register, login, JWT access + refresh token handling
- **Todos** — full CRUD with pagination, scoped to authenticated user
- **Rooms** — join shared rooms via slug (anonymous access)
- **SSR-ready** — TanStack Start with server-side rendering support

## Tech stack

| Layer | Technology |
|-------|-----------|
| Framework | TanStack Start (React + TypeScript) |
| Routing | TanStack Router |
| Data fetching | TanStack Query |
| Bundler | Vite |
| Package manager | pnpm |
| CI/CD | GitHub Actions |
| Deploy | Railway |

## Getting started

### Prerequisites

- Node.js 20+
- pnpm

### Setup

```bash
# 1. Clone the repo
git clone https://github.com/hidetsumi/mikan-web.git
cd mikan-web

# 2. Install dependencies
pnpm install

# 3. Copy env file and fill in values
cp .env.example .env

# 4. Start the dev server
pnpm dev
```

The app will be available at `http://localhost:3001`.

## Environment variables

See `.env.example` for all required variables.

```env
VITE_API_URL=http://localhost:3000
```

## Scripts

```bash
pnpm dev          # development server
pnpm build        # production build
pnpm start        # run production build
pnpm lint         # eslint
```

## Branch strategy

| Branch | Purpose |
|--------|---------|
| `main` | Production — protected |
| `develop` | Integration — all PRs target here |
| `feature/xxx` | New features |
| `fix/xxx` | Bug fixes |
| `chore/xxx` | Config, tooling |
| `release/vX.Y.Z` | Release candidates |

## Roadmap

See the [GitHub Project board](https://github.com/users/hidetsumi/projects/6) for current progress.

## License

MIT
