---
created_date: "2026-10-06"
document_status: draft
project: spektacular
spec: 000064_epic-worktree-store-isolation
plan: 000064_epic-worktree-store-isolation
---

# Epics page: worktrees hold only code

The epics page now explains that when an epic is implemented, each spek's worktrees hold only code. Specs, plans, changelogs and progress stay in your project, where you can follow a spek's plan being ticked off while the run is going. It also says that a spek whose branch changes Spektacular's own files is not merged.

> Derived from project spektacular (/home/nicj/code/github.com/hivecommons/spektacular), spec/plan 000064_epic-worktree-store-isolation. See the project-level record for the full feature.

## What changed in this repo

- `src/pages/epics.mdx`, "Implement this epic": the worktree bullet now says worktrees hold only code. A new bullet says records and progress stay in the project, and another describes the merge refusal for changes to Spektacular's files. The old line saying repos resolve to the spek's own copy is gone.

## Why

Spektacular changed how epics run: agents now always run Spektacular from the project, and worktrees carry only code. The docs describe that model.
