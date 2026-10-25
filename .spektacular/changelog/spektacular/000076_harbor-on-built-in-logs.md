---
created_date: "2026-10-25"
document_status: draft
project: spektacular
spec: 000076_harbor-on-built-in-logs
plan: 000076_harbor-on-built-in-logs
---

# Run statistics: listing commands and spans

The Run statistics page now explains two more reports: `spektacular stats commands`, which lists every command Spektacular recorded with its step, arguments, timing and exit code, and `spektacular stats spans`, which lists every helper agent, wait on you and other marked span. It shows how to narrow them to some runs and how to see what an epic orchestrator did outside any run with `--outside-runs`.

> Derived from project spektacular, spec/plan 000076_harbor-on-built-in-logs. See the project-level record for the full feature.

## What changed in this repo

- `src/pages/run-stats.mdx`:
  - a new "Listing commands and spans" section, placed after "Summarising runs": what each listing shows, the shared selection flags, `--outside-runs`, and the JSON fields each carries;
  - "Reports for programs" names the `commands` and `spans` arrays as stable fields.

## Why

Spektacular gained these listings so the Harbor test harness, and anyone else, can read every recorded command and helper span through the run statistics report rather than parsing the log files.
