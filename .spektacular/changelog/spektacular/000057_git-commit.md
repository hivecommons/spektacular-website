---
created_date: "2026-09-23"
document_status: draft
project: spektacular
spec: 000057_git-commit
plan: 000057_git-commit
---

# Configuration reference: the auto_commit setting

The configuration reference now documents `auto_commit`, the project setting
that lets Spektacular make git commits for you as a workflow runs. The entry
describes all three values, states that the default is `off`, and explains that
commits use your own git, run your hooks, honour your identity and signing
settings, and are never pushed.

> Derived from project spektacular (git@github.com:jumppad-labs/spektacular.git), spec/plan 000057_git-commit. See the project-level record for the full feature.

## What changed in this repo

In `src/pages/configuration.mdx`:

- A new `auto_commit` entry in the "Project configuration keys" block, placed
  between `spec_trigger_threshold` and `debug`. It describes `off` (the
  default, no automatic commits), `workflow` (one commit in each changed
  repository when a spec, plan or implementation completes) and `full` (as
  `workflow`, plus a commit after each milestone of an implementation), and
  notes that a repository which isn't a git repository is skipped and that the
  agent asks before sweeping in uncommitted work.
- The example project configuration gains the line `auto_commit: "off"` with
  its accepted values as a trailing comment.
- The top-level key list gains `auto_commit`, and its hand-written count moves
  from thirteen to fourteen.
- The page's frontmatter description names the new key alongside the others.

## Why

The setting is off by default and does nothing until a reader turns it on, so
the configuration reference is the only place most people will discover it
exists. Documenting the three values and the default together is also what lets
a reader judge whether `workflow` or `full` suits how they work, rather than
finding out by enabling it and watching what happens to their git history.
