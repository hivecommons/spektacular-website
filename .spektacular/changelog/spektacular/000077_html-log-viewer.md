---
created_date: "2026-10-25"
document_status: draft
project: spektacular
spec: 000077_html-log-viewer
plan: 000077_html-log-viewer
---

# Run viewer page

The documentation site has a new Run viewer page explaining how to render any recorded workflow run as a single-file HTML waterfall with `spektacular stats view`, how to choose the run and render logs collected elsewhere, and how to read the page: span types, problem markers, gaps and the threshold, zooming, collapsing, details, totals and the side summary. It is linked from the Resources menu after Run statistics and from the Run statistics page.

> Derived from project spektacular, spec/plan 000077_html-log-viewer. See the project-level record for the full feature.

## What changed in this repo

- `src/pages/run-viewer.mdx` (new): the Run viewer page, built from `Hero`, `Prose` and `CtaBanner`, with sections on rendering a run, choosing it, logs from elsewhere, reading the waterfall (a table of each type's look), problems, gaps, zooming and collapsing, details, totals and the summary, and the JSON result for programs. Its call to action links to Run statistics.
- `src/components/Nav.astro`: a "Run viewer" entry in Resources, straight after "Run statistics".
- `src/pages/run-stats.mdx`: the "Reporting on one run" section points to the run viewer.

## Why

`spektacular stats view` is a new way to read a run, and its page has controls and visual markers a reader needs explained: which colour is which span type, what each problem marker means, and how the gap threshold, zoom and collapse behave.
