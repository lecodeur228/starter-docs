# From a PRD

How agents (and humans) turn a PRD into this docs tree.

## Input

A PRD, brief, or cahier des charges (paste, file, or Notion link summary).

## Output

Updated pages under:

1. `00-overview` — project map + glossary + checklist  
2. `01-product` — vision, personas, stories, specs, roadmap  
3. `02-tech` — stack, architecture, API, auth, …  
4. `03-decisions` — ADRs for important choices  
5. `04-runbooks` — local / envs / deploy  

## Rules

Full workflow: [AGENTS.md](../../AGENTS.md).

Short version:

- Split by folder — never one mega-file
- Do not invent missing requirements
- Leave `TODO` when unknown
- Auth and error codes must stay aligned with backend/mobile
