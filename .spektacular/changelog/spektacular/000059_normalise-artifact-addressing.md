---
created_date: "2026-09-25"
document_status: draft
project: spektacular
spec: 000059_normalise-artifact-addressing
plan: 000059_normalise-artifact-addressing
---

The documentation site now explains how specs, plan documents and changelog records are addressed. A new Documents page, reachable from the Resources menu, covers the bare-name rules, what the list commands print, the `unexpected_extension` and `document_required` error codes, and an upgrade table mapping every old spelling to its new form. The configuration reference now says that locations the CLI reports are relative to the folder holding `config.yaml`.

> Derived from project spektacular, spec/plan 000059_normalise-artifact-addressing. See the project-level record for the full feature.

## What changed in this repo

- New page `src/pages/documents.mdx`: addressing rules, sections for `spec file`, `plan file` and `changelog file` with examples, `name` versus `path`, the status plan fields, an Error codes block (`unexpected_extension`, `document_required`, `not_found`) with a sample error envelope, and an "Upgrading from earlier spellings" table.
- `src/components/Nav.astro`: a Documents entry under Resources, after Design Documents.
- `src/pages/configuration.mdx`: the `spec`, `plan` and `changelog` keys note that reported locations are relative to the folder holding `config.yaml` and link to the new page.
- `src/pages/plan-tasks.mdx`: an `implement status` sample showing `plan_name`, `plan_document` and the relative `plan_path`.

## Why

The CLI change is a hard break for external callers, so the site needed a command reference, the error codes and a migration path in the place users look for them.
