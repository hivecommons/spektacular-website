---
created_date: "2026-10-02"
document_status: draft
project: spektacular
spec: 000060_epics-and-seeded-specs
plan: 000060_epics-and-seeded-specs
---

# Docs: epics, starting from existing material and the status view

The documentation site now explains epics: what they are, when Spektacular offers to split a spec,
how split sensitivity works, the epic-first route for tracker epics, chaining, and how
implementation treats dependencies between specs. It describes starting a spec from an issue or
other existing material, documents the single `status` command in place of the commands it
replaces, and covers the new epic settings.

> Derived from project spektacular, spec/plan 000060_epics-and-seeded-specs. See the project-level record for the full feature.

## What changed in this repo

- A new Epics page, linked from the Resources menu.
- How it works: starting from existing material with the recorded `sources`, "implement the spek"
  wording, and `spektacular status`.
- Plans and tasks: one "Seeing where work stands: status" section with readable and JSON examples
  and a status-fields reference, replacing the export and progress sections.
- Documents: status wording and a table mapping `spec status`, `plan status`, `implement status`
  and `plan export` to `status`.
- Configuration: `epic_split_threshold` and the `epic` section (`provider`, `strict_dependencies`,
  `config.directory`), sixteen top-level keys, and the format-4 upgrade.
- Home page and getting-started tutorial: "implement the spek" wording.
- A changelog entry for the release.

## Why

The release changes how specs are started, grouped and tracked, and removes four commands; the
site has to describe the new behaviour and tell existing users what replaces what.
