---
created_date: "2026-10-25"
document_status: draft
project: spektacular
spec: 000074_trace-spans-for-agent-work
plan: 000074_trace-spans-for-agent-work
---

# Spans on the logging page

The "Logging and debugging" page now explains spans: how a run's log shows where its time went, the six span types and which ones Spektacular records by itself, how agents mark helper agents and waits on the user with `spektacular trace start` and `spektacular trace stop`, how spans nest and end, and what the new span records look like.

> Derived from project spektacular (git@github.com:hivecommons/spektacular.git), spec/plan 000074_trace-spans-for-agent-work. See the project-level record for the full feature.

## What changed in this repo

- `src/pages/debugging.mdx`: new sections "Spans: where the time went", "Span types", "Marking spans", "How spans end" and "Span records" between "Reading a record" and "Upgrading from debug mode", and a page description that mentions spans.

## Why

Spektacular now records steps, plan tasks, helper agents and waits on the user as spans, and agents use two new commands to mark the ones the CLI cannot see. The logging page is where users read what the log holds, so it describes the spans, the commands and the record format.
