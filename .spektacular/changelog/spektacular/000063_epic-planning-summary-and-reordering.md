---
created_date: "2026-10-04"
document_status: draft
project: spektacular
spec: 000063_epic-planning-summary-and-reordering
plan: 000063_epic-planning-summary-and-reordering
---

# 000063_epic-planning-summary-and-reordering

The Epics page now explains the summary document planning an epic leaves behind. It describes how speks that change the same files are ordered automatically, and how to undo an added order at the review. It also explains the new questions planning stops to ask about decisions you already made and disagreements between plans.

> Derived from project spektacular (git@github.com:hivecommons/spektacular.git), spec/plan 000063_epic-planning-summary-and-reordering. See the project-level record for the full feature.

## What changed in this repo

- **"Plan this epic":** describes the summary document (decisions first, then any added order, then one section per plan), the automatic ordering of overlapping speks, and the review that walks the summary, where an added order can be removed for good.
- **"What still stops for you":** adds the stops for contradicting a recorded decision or a knowledge entry, and how cross-plan disagreements are listed with a proposed answer.
- **"Dependencies between specs":** links to the automatic ordering.
- **"Working with epics from the command line":** adds `epic summary read`, `epic summary write` and `epic order` (with unorder), and says deleting an epic deletes its summary.
- **Frontmatter description and `CHANGELOG.md`:** updated.

## Why

Users need to know what planning an epic now produces, why a dependency may appear that they did not write, and which new questions to expect while planning runs.
