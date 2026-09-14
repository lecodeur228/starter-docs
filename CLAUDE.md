# CLAUDE.md

Guidance for Claude Code (and compatible agents) in this repository.

## Project

**starter-docs** — empty documentation template (product + tech) for new projects. Pillar **docs** next to **mobile** and **backend**.

## Source of truth

Follow **[AGENTS.md](AGENTS.md)** for the full PRD → docs workflow and folder map.

## DO

- Spread a PRD across `00-overview` → `01-product` → `02-tech` → `03-decisions` → `04-runbooks`
- Keep one concern per file
- Create ADRs from `docs/03-decisions/template.md`
- Leave `TODO` when information is missing
- Cross-link pages instead of duplicating

## DO NOT

- Invent features or endpoints not in the PRD / user input
- Commit secrets
- Write app code here
- Dump the whole PRD into a single markdown file
- Mix product vision with API implementation details on the same page

## Key paths

- Overview: `docs/00-overview/README.md`
- Product: `docs/01-product/`
- Tech: `docs/02-tech/`
- ADR: `docs/03-decisions/`
- Runbooks: `docs/04-runbooks/`
- Agent rules: `AGENTS.md`
