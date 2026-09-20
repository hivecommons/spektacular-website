---
created_date: "2026-09-16"
document_status: draft
project: spektacular
spec: 000052_document-status-vocabulary
plan: 000052_document-status-vocabulary
---

# Website describes document status

The website now describes the lifecycle metadata on specs, plans and changelog records as a *document status*, with the values `draft`, `final`, `superseded` and `archived`. The example frontmatter and the lifecycle descriptions no longer mention `in-progress` or `completed`, matching the current Spektacular CLI.

> Derived from project spektacular (git@github.com:jumppad-labs/spektacular.git), spec/plan 000052_document-status-vocabulary. See the project-level record for the full feature.

## What changed in this repo

- **Projects page.** The derived changelog frontmatter example shows `document_status: draft`.
- **How it works page.** The lifecycle list item is now "Document status", listing the four values, and the summary paragraph refers to "document status and dates".
- **Configuration page.** The spec, plan and changelog sections say each record carries "a document status".

## Why

Spektacular renamed the field and its values so that agents stop reading a finished document as finished work. The website's examples and descriptions have to match what the CLI actually writes.
