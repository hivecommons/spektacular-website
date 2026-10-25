---
created_date: "2026-10-25"
document_status: draft
project: spektacular
spec: 000075_run-stats-command
plan: 000075_run-stats-command
---

# Run statistics page

The documentation site has a new "Run statistics" page explaining `spektacular stats`. It covers listing recorded runs, reporting where one run's time went, choosing runs, comparing runs side by side, summarising many runs, and reporting on a logs directory copied from elsewhere. It also defines every figure the report shows and how unfinished work and damaged log lines appear.

> Derived from project spektacular (spektacular), spec/plan 000075_run-stats-command. See the project-level record for the full feature.

## What changed in this repo

- **`src/pages/run-stats.mdx` (new)**: the Run statistics page, built from `Hero`, `Prose` and `CtaBanner`, with fenced examples of the real table layouts and an abridged JSON report. It defines:
  - wall time, working time, user wait and helper wait;
  - command time, commands, duration, entries and incomplete;
  - the helper and wait counts;
  - gaps and the gap total.
- **`src/components/Nav.astro`**: the Resources menu links to the page, after "Logging and debugging".
- **`src/pages/debugging.mdx`**: the span records section ends with a pointer to the page.

## Why

Spektacular now ships a report over its own logs. Users need to know how to run each form, what each figure means, and what to expect from unfinished runs and copied logs directories.
