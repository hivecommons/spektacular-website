---
created_date: "2026-10-25"
document_status: draft
project: spektacular
spec: 000073_log-mode-and-logger-providers
plan: 000073_log-mode-and-logger-providers
---

# Logging and debugging page

The website's debugging page is now "Logging and debugging", at the same address. It explains that every Spektacular command is logged by default to `.spektacular/logs/`, and covers:

- what the `standard`, `verbose` and `off` levels record;
- where logs go and how to move them;
- how many runs are kept;
- how to switch logging off;
- which commands are never logged;
- how to read a record;
- what happens to an old debug setting on upgrade.

The configuration reference documents the new `log` section in place of `debug`.

> Derived from project spektacular, spec/plan 000073_log-mode-and-logger-providers. See the project-level record for the full feature.

## What changed in this repo

- `src/pages/debugging.mdx` is rewritten. Its sections are: logging on by default, with the `log` block; what each level records; where logs go, with run and day file names and `log.config.directory`; how long logs are kept; commands that are never logged (`status`, and the `spektacular stats` reports), with no environment variable; a sample record and its fields; and upgrading from debug mode.
- `src/pages/configuration.mdx`:
  - The frontmatter description and the "Seventeen top-level keys" list name `log`.
  - The example `config.yaml` shows the `log` block and `schema: 5`.
  - The `debug` key reference is replaced by a `log` key reference, with each setting and its default.
- `src/components/Nav.astro`: the navigation label reads "Logging and debugging".

## Why

Debug mode, its `debug.enabled` setting and its environment variable are gone from Spektacular, replaced by always-on logging. The debugging page and the configuration reference had to describe what now ships.
