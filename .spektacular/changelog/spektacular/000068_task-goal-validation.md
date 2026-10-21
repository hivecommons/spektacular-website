---
created_date: "2026-10-21"
document_status: draft
project: spektacular
spec: 000068_task-goal-validation
plan: 000068_task-goal-validation
---

# The docs describe the implement goal check

The documentation site now explains that implement runs have an independent reviewer check each task's goal before anything is ticked. The workflow reference covers the reviewer's three verdicts (met, not yet met, impossible) and what each one does. The configuration reference shows how to switch the check off and how to pick the reviewer's model for each coding agent, with each agent's limits.

> Derived from project spektacular, spec/plan 000068_task-goal-validation. See the project-level record for the full feature.

## What changed in this repo

**How it works**

- The Implement stage's step tree now reads `read_plan → analyze → implement → test → verify → check_goal → update_plan → ...`.
- The Implement pipeline node now reads "independent reviewer checks each criterion". The homepage's copy of the node changed too.
- A new paragraph describes:
  - the fresh-context, read-only reviewer;
  - the three verdicts;
  - the two-retry rule;
  - the keep fixing, accept or skip stop;
  - `spektacular implement goal show`;
  - the stop in an epic;
  - the off switch.

**Plan tasks**

- The `Acceptance criteria` key says criteria are ticked only when the goal check judged them met, or from verification with the check off.

**Configuration**

- The YAML example adds `implement.goal_check`.
- The `implement` key documents `implement.goal_check.enabled` and `implement.goal_check.models.<agent>`.
- It lists each agent's default reviewer model: `haiku`, `gpt-6-luna`, `Claude Haiku 4.5`, `@smol`, and Bob's `explore` helper.
- It states the limits: Bob has no per-helper model, Copilot ignores the helper's model under `Auto`, and Codex's reviewer is read-only by instruction only.

**Changelog**

- `CHANGELOG.md` has a new entry.

## Why

The tool's implement workflow now judges every acceptance criterion with a separate reviewer before ticking it. The site's workflow and configuration reference had to describe the check, its verdicts, its settings and each agent's model limitations.
