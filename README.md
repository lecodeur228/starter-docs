# Starter Docs

Template documentation for a new project. Use it as the **docs** pillar next to **mobile** and **backend**.

```text
nouveau-projet/
├── docs/       ← this starter (starter-docs)
├── mobile/     ← Flutter (or other) starter
└── backend/    ← Laravel / Adonis starter
```

No product content is pre-written — only structure and conventions. Fill pages when you start a project (typically from a **PRD**).

## Quick start

1. Use this repo as a GitHub Template (or clone it)
2. Rename / place it under your monorepo or as `docs/`
3. Give agents / yourself the PRD → follow [docs/00-overview/from-prd.md](docs/00-overview/from-prd.md)
4. Replace placeholders (`TODO`, `[Project]`)
5. Keep docs in sync with mobile + backend changes

## Layout

| Folder | Purpose |
|--------|---------|
| [docs/00-overview](docs/00-overview) | Project map, glossary, [PRD workflow](docs/00-overview/from-prd.md) |
| [docs/01-product](docs/01-product) | Vision, personas, stories, specs, roadmap |
| [docs/02-tech](docs/02-tech) | Architecture, API, auth, security, testing, … |
| [docs/03-decisions](docs/03-decisions) | Architecture Decision Records (ADR) |
| [docs/04-runbooks](docs/04-runbooks) | Local setup, envs, deploy |

## AI agents

When you drop a PRD into chat, agents must **spread** it across the folders above (not one dump file).

| File | Role |
|------|------|
| [AGENTS.md](AGENTS.md) | Full source of truth (PRD → docs map, always/never) |
| [CLAUDE.md](CLAUDE.md) | Short Claude Code pointer |
| [.cursor/rules/](.cursor/rules/) | Cursor rules (global + product / tech / ADR) |

## Conventions

- Language: French or English — pick one per project and stay consistent
- Clients branch on **stable error codes**, never on translated messages
- Every endpoint / auth / env change updates the matching doc page
- Prefer short pages with one job each
- Decisions that change the stack go in `03-decisions/` (see template)

## License

MIT
