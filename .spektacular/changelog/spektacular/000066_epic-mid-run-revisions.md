---
created_date: "2026-10-08"
document_status: draft
project: spektacular
spec: 000066_epic-mid-run-revisions
plan: 000066_epic-mid-run-revisions
---

# Docs: correcting a spek or design during implementation

The documentation now explains what happens when implementing shows that a spek, or a design it references, is wrong. The run stops and the amendment is proposed. In an epic, the orchestrator brings it to you. Once you approve, the change is applied with `spektacular spec amend` and recorded on the spek, and the run carries on. The reference pages document the command and the `plan.strict_spec_changes` setting it interacts with.

> Derived from project spektacular, spec/plan 000066_epic-mid-run-revisions. See the project-level record for the full feature.

## What changed in this repo

- `src/pages/how-it-works.mdx`: the implement stage describes the stop, the approval and `spec amend`, and points to the Epics page.
- `src/pages/epics.mdx`: "What still stops for you" points to a new "When the spek or a design is wrong" subsection. It covers the hand-back, applying the amendment in the project, the amendable sections, design revisions, a sample `## Amendments` entry, the plan changelog record and the strict-mode exemption.
- `src/pages/documents.mdx`: a new "Amending a spek during implementation" subsection with a `spec amend` example.
- `src/pages/design-documents.mdx`: a design can be corrected during a run after approval, keeping its capture date and references.
- `src/pages/configuration.mdx`: documents `plan.strict_spec_changes`, its default and the exemption, and adds it to the example.
- `src/pages/plan-tasks.mdx`: the `stale` state notes the exemption.
- `CHANGELOG.md`: a `000066_epic-mid-run-revisions` entry.

## Why

Users running epics and interactive implement runs need to know that a wrong spek or design is raised with them, how they approve a fix, and that a recorded fix does not stall the run.
