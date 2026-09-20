---
created_date: "2026-09-20"
document_status: draft
project: spektacular
spec: 000053_config-schema-versioning-and-migrations
plan: 000053_config-schema-versioning-and-migrations
---

# Configuration reference covers settings versions, the folder rule and `migrate`

The configuration reference now documents the version fields Spektacular writes
into every settings file, the new default store folders and the rule that they
resolve from the folder holding `config.yaml`, and a new section on upgrading a
project with `migrate`. Configuration examples across the site use the new
folder values.

> Derived from project spektacular (git@github.com:jumppad-labs/spektacular.git),
> spec/plan 000053_config-schema-versioning-and-migrations. See the
> project-level record for the full feature.

## What changed in this repo

**`src/pages/configuration.mdx`.**

- The project `config.yaml` example and key reference gained `schema`,
  `written_by` and `skills_version`, each with what it means and who sets it.
  The key count in the section subtitle went from nine to twelve.
- The `spec`, `plan` and `changelog` keys show their new defaults, `specs`,
  `plans` and `changelog`, and state that each resolves from the folder holding
  `config.yaml`, the same rule as `repos[].location`, with a note that a folder
  outside the project is refused.
- The `repo.yaml` example and key reference gained `schema` and `written_by`,
  noting that a repo file carries its own format count.
- A new "Upgrading a project: migrate" section covers the `--dry-run` preview,
  what one run does (upgrading the project and every checked-out repo, keeping
  a `.v<N>.old` copy of each rewritten file, naming skipped repos, reinstalling
  stale agent skills), that out-of-date projects are blocked until upgraded and
  which commands still run, that re-running `init` applies the same upgrades,
  and that a file from a newer Spektacular is refused rather than converted.

**`src/content/tutorials/getting-started.mdx`.** The spec configuration example
now shows `directory: specs`, with a comment naming the folder it resolves
from. Prose and directory diagrams naming on-disk locations were checked and
left as they are, because those locations have not moved.

## Why

Readers configuring a project need to know that the folder settings are now
read relative to the settings file, or they will write a project-root path and
get a nested folder. They also need to know what the version fields mean and
what to do when a release stops their commands and names `migrate`. Documenting
the upgrade alongside the keys it changes keeps the reference the single place
that answers both.
