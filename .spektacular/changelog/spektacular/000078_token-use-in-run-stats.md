---
created_date: "2026-10-25"
document_status: draft
project: spektacular
spec: 000078_token-use-in-run-stats
plan: 000078_token-use-in-run-stats
---

# Token figures on the Run statistics page

The documentation site now explains the token, cost and time-per-token figures that `spektacular stats` reports for Claude Code runs: how a run is matched to its agent session with no setup, what each figure means, how to give model prices, and how unknown and incomplete values appear. The configuration reference describes the new optional `stats` key with an example price table.

> Derived from project spektacular, spec/plan 000078_token-use-in-run-stats. See the project-level record for the full feature.

## What changed in this repo

- `src/pages/run-stats.mdx`: new sections "Tokens and cost", "How a run finds its session", "What the token figures mean", "Setting prices" and "When tokens are unknown", between "Unfinished work and damaged lines" and "Reports for programs"; "Reports for programs" shows the JSON `tokens` section and names the six figures comparisons and summaries add; the page description mentions tokens and cost.
- `src/pages/configuration.mdx`: a `stats` `ConfigKey` after `log` describing `stats.prices.<model>.input`, `.output`, `.cache_read` and `.cache_write`; a `stats.prices` block in the example `config.yaml`; "Eighteen top-level keys" with `stats` in the list; `stats` in the page description.

## Why

Readers need to know where the new figures come from, which agents they cover, how to price them and why a figure can be unknown, so they can trust the numbers when they use them to judge and compare runs.
