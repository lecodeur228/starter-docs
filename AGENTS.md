# AGENTS.md — Starter Docs

Source of truth for AI agents working in this documentation template.

## Scope

This repo is **documentation only**. Do not invent app code here. Point to `mobile/` and `backend/` for implementation.

## Always

- Keep structure under `docs/00-overview` … `docs/04-runbooks`
- Leave `TODO` placeholders until the project fills them — do not invent fake product facts
- When adding a decision, copy `docs/03-decisions/template.md` → `NNNN-short-title.md`
- Cross-link related pages instead of duplicating long text
- Update `docs/00-overview/README.md` links if mobile/backend paths change

## Never

- Commit secrets, tokens, or real credentials into docs
- Duplicate full API contracts in three places — one source in `02-tech/api.md` (or OpenAPI in backend)
- Mix product vision and low-level API details in the same page

## New project checklist

1. Fill `01-product/vision.md` and `cahier-des-charges.md`
2. Record stack in `02-tech/stack.md` + first ADRs in `03-decisions/`
3. Document auth modes actually enabled on the backend
4. Wire runbooks to real local ports and deploy targets
