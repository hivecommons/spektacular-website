---
created_date: "2026-09-20"
document_status: draft
project: spektacular
spec: 000055_design-authoring-skill
plan: 000055_design-authoring-skill
---

# The site explains both kinds of design document

The design documents page now explains that Spektacular can help you work a design out through a
guided conversation, not only store one you had already written. It sets out what the resulting
document records and, importantly, corrects a claim that had become misleading: the site used to
say flatly that Spektacular never adds frontmatter to a design document, which is still true of
the documents it did not write and no longer true of the ones it now authors with you. A reader
can now tell, without reading any code, which of their files Spektacular will change and which it
will leave exactly as they are.

> Derived from project spektacular (file), spec/plan 000055_design-authoring-skill. See the
> project-level record for the full feature.

## What changed in this repo

**`src/pages/design-documents.mdx`**

- The "What a design document is" section was reworked rather than added to. Its unqualified
  guarantee is now a two-class statement: a design your team already had gains no frontmatter, is
  never reformatted, and comes back byte for byte as you supplied it, while a design Spektacular
  authors with you carries the same lifecycle record every spec and plan carries.
- A new section, "Working a design out with Spektacular", explains the guided interview, notes it
  is the same Flipped Interaction pattern used for specs, and shows a worked transcript. It states
  the stopping condition explicitly, that the interview ends once a further answer would not change
  the document, and that what gets written is the design rather than a transcript of the
  conversation.
- A new section, "What an authored design records", lists the four fields as bullets with a worked
  YAML example, and states plainly that a pre-existing design carries no such block at all.
- The command reference gained `design author` alongside the existing verbs, with a sentence on
  when to use each and a note that running the verbatim write over an authored design is refused.
- The "When a reference cannot be found" section gained a paragraph on a reference operation
  failing as a unit, so a spec and a design are never left contradicting each other.

**`src/pages/configuration.mdx`** — the `design` section now says a source can hold both kinds of
document side by side, so it agrees with the main page rather than leaving a reader to find the
old framing in whichever place they happen to look first.

Both pages compose from the existing `Section` and `Prose` components with no new band type, and
no layout markup was added to any page body. The two new sections were inserted as a pair, plain
then shaded, after a shaded section, which preserves the page's alternating background run without
changing any existing section's `surface` value.

## Why this repo got the change

Two classes of design document is exactly the kind of distinction users get wrong when it is not
written down, which is why the documentation was a requirement of this feature rather than a
courtesy. It is also the mitigation for the one real conceptual cost the approach carries: the
guarantee that Spektacular never touches a design document had to narrow, and a narrowed guarantee
that nobody explains is worse than the original.

## Verification

`npm run build` succeeds and `npx astro check` reports zero errors and zero warnings. Note that
`astro check` is not an npm script and CI runs only `npm run build`, so type-checking is a local
gate that has to be run deliberately. One pre-existing hint about `document.execCommand` in an
unrelated component is neither an error nor a warning and was not in scope.
