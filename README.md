# Starter Docs

Template documentation for a new project. Use it as the **docs** pillar next to **mobile** and **backend**.

```text
nouveau-projet/
├── docs/       ← this starter (starter-docs)
├── mobile/     ← Flutter (or other) starter
└── backend/    ← Laravel / Adonis starter
```

No product content is pre-written — only structure and conventions. Fill pages when you start a project.

## Quick start

1. Use this repo as a GitHub Template (or clone it)
2. Rename / place it under your monorepo or as `docs/`
3. Replace placeholders (`TODO`, `[Project]`)
4. Keep docs in sync with mobile + backend changes

## Layout

| Folder | Purpose |
|--------|---------|
| [docs/00-overview](docs/00-overview) | How to use this docs set, glossary, links to mobile/backend |
| [docs/01-product](docs/01-product) | Vision, personas, stories, specs, roadmap |
| [docs/02-tech](docs/02-tech) | Architecture, API, auth, security, testing, … |
| [docs/03-decisions](docs/03-decisions) | Architecture Decision Records (ADR) |
| [docs/04-runbooks](docs/04-runbooks) | Local setup, envs, deploy |

## Conventions

- Language: French or English — pick one per project and stay consistent
- Clients branch on **stable error codes**, never on translated messages
- Every endpoint / auth / env change updates the matching doc page
- Prefer short pages with one job each
- Decisions that change the stack go in `03-decisions/` (see template)

## Agents

See [AGENTS.md](AGENTS.md) for AI assistant rules when editing this repo.

## License

MIT
