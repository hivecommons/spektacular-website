---
created_date: "2026-10-07"
document_status: draft
project: spektacular
spec: 000065_implement-in-worktrees
plan: 000065_implement-in-worktrees
---

# 000065_implement-in-worktrees

The documentation now explains that every implement run builds a spek in its own git worktrees and merges back into every repo together when the plan is complete, with conflicts left to you, and how to turn that off. It documents the new per-repository setup command for preparing worktrees, and that an epic's uncommitted-work check covers only the repositories it builds.

> Derived from project spektacular (hivecommons/spektacular), spec/plan 000065_implement-in-worktrees. See the project-level record for the full feature.

## What changed in this repo

- `src/pages/configuration.mdx`: the `implement` section (`implement.worktrees`) in the example config and project keys (now seventeen), and the `worktree_setup` key in the example `repo.yaml` and repository keys.
- `src/pages/how-it-works.mdx`: the implement stage describes worktree runs, merging back, conflict handling, the opt-out, and unmerged dependencies.
- `src/pages/epics.mdx`: "Implement this epic" covers the narrowed uncommitted-work check and the setup command; the status example shows `dirty_repos`.
- `src/pages/projects.mdx`: `worktree_setup` listed with a repository's own settings.
- `CHANGELOG.md`: entry for this change.

## Why

The site is the configuration and workflow reference, so users need the new setting, the setup command and the changed implement behaviour described where they look them up.
