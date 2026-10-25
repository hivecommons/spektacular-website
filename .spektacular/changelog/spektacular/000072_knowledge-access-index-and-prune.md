---
created_date: "2026-10-25"
document_status: draft
project: spektacular
spec: 000072_knowledge-access-index-and-prune
plan: 000072_knowledge-access-index-and-prune
---

# Knowledge base pages: self-written knowledge, usage and prune

The website now explains that agents write knowledge entries themselves and report what they wrote, how each knowledge store records which entries are found and read, and how `spektacular knowledge prune` removes unused entries and checks the rest, including its dry-run preview. The configuration reference documents the new `knowledge.prune.max_age_days` setting and its default of 90 days.

> Derived from project spektacular, spec/plan 000072_knowledge-access-index-and-prune. See the project-level record for the full feature.

## What changed in this repo

- `src/pages/knowledge-base.mdx`: the entry lifecycle says agents write without asking and report the entry; new "How usage is recorded" and "Pruning the knowledge base" sections (with alternating band shading kept); the tagging passage says tags are chosen and reported; the Configuration section shows `knowledge.prune.max_age_days`.
- `src/pages/configuration.mdx`: the example project config and the `knowledge` key reference document `knowledge.prune.max_age_days` (default 90, must be positive).

## Why

The website is where users learn how the knowledge base behaves, and this release changes how entries are written, adds the usage index and adds the prune command and its setting.
