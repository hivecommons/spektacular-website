---
created_date: "2026-10-04"
document_status: draft
project: spektacular
spec: 000062_epic-plan-and-implement
plan: 000062_epic-plan-and-implement
---

# 000062_epic-plan-and-implement

The Epics page now explains how to plan and implement a whole epic with two requests, "plan this epic" and "implement this epic". It also explains what still stops for you, what happens when something fails, and that repeating a request resumes where the epic stands and skips completed work.

> Derived from project spektacular (git@github.com:hivecommons/spektacular.git), spec/plan 000062_epic-plan-and-implement. See the project-level record for the full feature.

## What changed in this repo

- **New Epics page section:** "Planning and implementing an epic". It covers:
  - the two requests, and planning in dependency order with parallel agents;
  - implementing in per-repo git worktrees, merged into every repo together before dependents start, or not at all if any repo would conflict;
  - refusal of unplanned or broken epics;
  - genuine questions, failures and resuming;
  - an example of the `run` view `spektacular status` reports for an epic.
- **Opening explanation:** it now points to the new section.
- **Page description:** updated.
- **Site changelog:** gains an entry for 000062.

## Why

The documentation site is where users learn how to work with epics. It needed to describe the new one-request planning and implementation, including the resume and skip behaviour.
