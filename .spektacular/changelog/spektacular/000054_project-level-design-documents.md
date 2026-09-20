---
created_date: "2026-09-20"
document_status: draft
project: spektacular
spec: 000054_project-level-design-documents
plan: 000054_project-level-design-documents
---

# Design Documents page, and the design settings key in the configuration reference

The site gained a page explaining design documents: what one is, when to reach for one instead
of putting the detail in a spec, how a design relates to the specs and plans that point at it,
and the full command surface with worked examples. It is reachable from the Resources menu. The
configuration reference now documents the new `design` settings key alongside the existing ones.

> Derived from project spektacular, spec/plan 000054_project-level-design-documents. See the
> project-level record for the full feature.

## What changed in this repo

**New page, `src/pages/design-documents.mdx`.** Seven sections after the hero, shading
alternating from plain, built from the existing Hero, Section, Prose, CtaBanner and Button
components with no new markup:

- what a design document is, and that Spektacular owns the reference rather than the document
- when to use one instead of a spec section, as three tests that must all hold, with the
  constraint versus technical-direction versus design-document split spelled out
- how designs relate to specs and plans, including a worked example of a spec's recorded
  references
- declaring where designs live, with both a relative and an absolute location
- the command surface, one fenced example per verb, with a sample reference-resolution response
  showing a resolved and an unresolved entry
- what an unresolvable reference looks like, and why it is a failure rather than an empty result
- why it works this way: the spec stays readable, a shipped design is never force-synced, and
  storage is declared rather than imposed

**Navigation.** One entry added to the Resources group, after Projects.

**Configuration reference, `src/pages/configuration.mdx`.** A `design` key entry in the project
settings key list, placed between `knowledge` and `repos` and following the existing key's exact
shape: what the section is for, a bullet per sub-key, and a link out to the new concept page
rather than a restatement of it. The worked settings example gained the matching block with its
relative-location rule noted inline, and the stated top-level key count was corrected from
twelve to thirteen. The repository keys block deliberately gains nothing, because a repository
does not declare design sources.

One deviation from what was planned: the when-to-use rule of thumb was specified as a short
table, and is bullets instead. The body stylesheet carries no table styling, so a markdown table
would have rendered as a bare unstyled HTML table, and adding table CSS would be a site-wide
change well outside this work.

## Why this repo got the change

Design documents are a concept, not just a settings key, and a reader who meets the key first
has no way to infer why it exists or when to use it. The site explains concepts; the
configuration reference lists keys and links out. Splitting it that way follows the division
already established here, and keeps the concept in one place rather than half-stated in two.

Both pages build and type-check with no errors and no warnings, and the added prose carries no
em dashes.
