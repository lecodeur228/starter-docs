# AGENTS.md — Starter Docs

Source of truth for AI agents working in this **documentation** template.

This repo is the **docs** pillar of a project trilogy:

```text
projet/
├── docs/      ← this repo
├── mobile/
└── backend/
```

## Mission

When the user provides a **PRD** (or cahier des charges / brief), agents must **distribute** that content into the right folders — not dump everything into one file.

## Folder map (mandatory)

| Folder | Role | Fill when PRD mentions… |
|--------|------|-------------------------|
| `docs/00-overview/` | Map of the project, glossary, links to mobile/backend | Project name, repos paths, shared vocabulary |
| `docs/01-product/` | Product intent | Vision, users, stories, requirements, roadmap |
| `docs/02-tech/` | How we build it | Stack, architecture, API, auth, errors, i18n, security, tests |
| `docs/03-decisions/` | Why we chose X over Y (ADR) | Stack choices, auth modes, providers, trade-offs |
| `docs/04-runbooks/` | How to run / deploy | Local setup, envs, deploy steps |

### Product pages (`01-product`)

| File | Put here |
|------|----------|
| `vision.md` | Problem, audience, value, out of scope, success metrics |
| `personas.md` | User types and pains |
| `user-stories.md` | Epics + “As a… I want… so that…” |
| `cahier-des-charges.md` | Formal FR / NFR, constraints, acceptance |
| `roadmap.md` | Phases MVP → v1 → later |

### Tech pages (`02-tech`)

| File | Put here |
|------|----------|
| `stack.md` | Chosen tools (mobile, backend, DB, auth flags, hosting) |
| `architecture.md` | High-level diagram and layering |
| `api.md` | Base URL, envelope, resources overview — not a novel |
| `authentication.md` | **Only enabled** auth modes + endpoints |
| `authorization.md` | Roles / permissions |
| `errors.md` | Stable error codes table |
| `internationalization.md` | Locales, `Accept-Language` |
| `files.md` | Upload / storage |
| `notifications.md` | FCM / email / SMS |
| `security.md` | Checklist + constraints |
| `testing.md` | Tools + CI expectations |
| `clean-code.md` | Shared coding principles |

### Decisions (`03-decisions`)

- Copy `template.md` → `NNNN-short-title.md` (e.g. `0001-backend-laravel.md`)
- One decision per file
- Status: Proposed | Accepted | Deprecated | Superseded
- Link from `stack.md` when the decision sets the stack

### Runbooks (`04-runbooks`)

| File | Put here |
|------|----------|
| `local-setup.md` | Clone layout, commands, default URLs |
| `environments.md` | local / staging / prod — **variable names only**, no secrets |
| `deployment.md` | How each pillar is shipped |

## PRD → docs workflow

When the user pastes or points to a PRD:

1. **Read** the PRD fully; list ambiguities (ask if blocking).
2. **Overview** — update `00-overview/README.md` (name, trilogy links, glossary, checklist).
3. **Product** — fill `01-product/*` from vision / personas / stories / requirements / roadmap. Prefer the PRD’s wording; do not invent features.
4. **Tech** — fill `02-tech/*` only where the PRD (or user) specifies stack/auth/API. Leave `TODO` if unknown.
5. **Decisions** — for each important choice (backend, auth modes, SMS provider, etc.), add an ADR.
6. **Runbooks** — fill what is known; keep secrets out.
7. **Summarize** — list files updated + remaining TODOs.

### Mapping cheat-sheet

| PRD section (typical) | Target |
|-----------------------|--------|
| Contexte / problème / objectifs | `01-product/vision.md` + `cahier-des-charges.md` |
| Utilisateurs / personas | `01-product/personas.md` |
| Fonctionnalités / stories | `01-product/user-stories.md` |
| Exigences FR / NFR | `01-product/cahier-des-charges.md` |
| Planning | `01-product/roadmap.md` |
| Stack / contraintes tech | `02-tech/stack.md` + ADR |
| Auth (password, OTP, Google, …) | `02-tech/authentication.md` + ADR |
| API / écrans liés API | `02-tech/api.md` |
| Sécurité / conformité | `02-tech/security.md` |
| Déploiement / envs | `04-runbooks/*` |

## Always

- Keep one job per page; cross-link instead of duplicating
- Replace `[Project]` / `TODO` with real content when known; keep `TODO` when unknown
- Align auth docs with backend flags: `AUTH_PASSWORD`, `AUTH_OTP_EMAIL`, `AUTH_OTP_PHONE`, `AUTH_GOOGLE`
- Document that clients branch on stable error **codes**, never on translated messages
- Update docs when mobile/backend contracts change (same PR / same request if possible)

## Never

- Invent product facts or fake API endpoints not in the PRD / codebase
- Commit secrets, tokens, passwords, private keys
- Put low-level API noise inside `vision.md` or personas
- Put product marketing copy inside `02-tech/` or ADRs
- Collapse everything into a single mega-README
- Write application code in this repo (point to `mobile/` / `backend/`)

## Auth documentation rules

When documenting auth for a project:

1. Table of **enabled** modes only (or explicitly mark disabled).
2. OTP: mention `has_account` / `profile_completed` and `PATCH /auth/profile`.
3. Google: ID token → Bearer token.
4. Incomplete profile → `PROFILE_INCOMPLETE` on most protected routes.

## Quality bar before saying “done”

- [ ] Overview checklist updated
- [ ] Product pages filled or explicitly TODO
- [ ] Tech stack + auth pages consistent with decisions
- [ ] At least one ADR for major stack choice (if stack is known)
- [ ] No secrets in any file
- [ ] French **or** English consistently (project choice)
