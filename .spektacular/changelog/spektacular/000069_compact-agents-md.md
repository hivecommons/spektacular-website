---
created_date: "2026-10-21"
document_status: draft
project: spektacular
spec: 000069_compact-agents-md
plan: 000069_compact-agents-md
---

# Docs: the compact AGENTS.md layout

The configuration reference now explains how Spektacular lays out its standing rules. Each rule is a short statement in your root `AGENTS.md`, with its full guidance in `.spektacular/guidance/`, one file per rule, which agents read only when a rule applies. It also explains that upgrading with `migrate` converts an existing project and refreshes the guidance, leaving your own content alone.

> Derived from project spektacular, spec/plan 000069_compact-agents-md. See the project-level record for the full feature.

## What changed in this repo

- `src/pages/configuration.mdx`:
  - A new section, "Standing rules: AGENTS.md and .spektacular/guidance/". It explains:
    - what a short statement holds;
    - the eight-file guidance folder;
    - that the folder is committed and read on demand;
    - that the files are regenerated rather than edited;
    - how each agent reads `AGENTS.md`.
  - A new bullet in the migrate section's "One run:" list, about converting the rules and refreshing the guidance.
- `src/pages/plugins.mdx` and `src/content/tutorials/getting-started.mdx`: the omp text now says the omp rules mirror the short standing-rule sections and link to the full guidance.

## Why

Users upgrading Spektacular will see their `AGENTS.md` shrink, and a new `.spektacular/guidance/` folder appear. The docs say what both are, that the folder should be committed and left unedited, and where their own rules belong.
