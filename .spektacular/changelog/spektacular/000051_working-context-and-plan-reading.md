---
created_date: "2026-09-15"
status: in-progress
project: spektacular
spec: 000051_working-context-and-plan-reading
plan: 000051_working-context-and-plan-reading
---

# Tutorial shows the working context's new name

The unknown-acceptance-criteria tutorial quotes, word for word, the instruction agents receive at the end of each workflow step. That instruction now names the working-context file `.spektacular/working-context.md`, and the tutorial's quote matches it. Other pages that mention `context.md` refer to a plan's own technical-detail document, which keeps its name.

> Derived from project spektacular (file), spec/plan 000051_working-context-and-plan-reading. See the project-level record for the full feature.

## What changed in this repo

- `src/content/tutorials/unknown-criteria.mdx`: the quoted keep-context-current paragraph inside the fenced `markdown` block now says `.spektacular/working-context.md`. The rest of the quote is byte-identical to the footer Spektacular now emits.

## Why

The published docs should show exactly what agents are told. Spektacular renamed the working-context file so it can no longer be confused with a plan's `context.md`, and this tutorial is the one page that quotes the instruction naming it.
