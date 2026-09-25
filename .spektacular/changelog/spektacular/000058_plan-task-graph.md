---
created_date: "2026-09-25"
document_status: draft
project: spektacular
spec: 000058_plan-task-graph
plan: 000058_plan-task-graph
---

# 000058_plan-task-graph: documentation for plan tasks

The documentation site now explains how a plan breaks its work into tasks, which tasks need a person and why, how to export a plan's task graph (with every output field described), how to track per-task progress, and how to implement a single task. How it works and Configuration reflect the new vocabulary and setting.

> Derived from project spektacular, spec/plan 000058_plan-task-graph. See the project-level record for the full feature.

## What changed in this repo

- New page `src/pages/plan-tasks.mdx` ("Plan tasks"), linked from the Resources menu in `src/components/Nav.astro`.
- `src/pages/how-it-works.mdx`: a task replaces a phase in the core concepts and step tree, the plan walkthrough is described as mandatory and naming human tasks, and Implement can run one task.
- `src/pages/configuration.mdx`: documents `plan.task_id.provider` (default `uuid`).

## Why

Users and orchestrator authors need a public reference for the task format, the `plan export` fields and single-task implement.
