---
created_date: "2026-09-21"
document_status: draft
project: spektacular
spec: 000056_store_delete_and_knowledge_maintenance
plan: 000056_store_delete_and_knowledge_maintenance
---

# Documentation for removing knowledge entries and design documents

The knowledge base and design documents pages now cover removal. An entry's documented life gains a
fourth thing that can happen to it, and the design page explains something it previously left
implicit: removing a design is not the same as removing a reference to one. Anyone looking for a way
to delete a design meets the reference command first, and it appears to succeed while the document
is still sitting where it was.

> Derived from project spektacular (git@github.com:jumppad-labs/spektacular.git), spec/plan
> 000056_store_delete_and_knowledge_maintenance. See the project-level record for the full feature.

## What changed in this repo

**`src/pages/knowledge-base.mdx`** — the "lifecycle of an entry" section previously framed an
entry's life as creating it, searching and reading it back, and rewriting it. It now includes
removing it. A new **Removing** paragraph after "Keeping it up to date" covers `knowledge delete`
with its address, states that naming an undeclared store is refused while naming a path that holds
nothing simply succeeds, explains that the result distinguishes the two so you can tell a removal
from a no-op, and notes the one entry that cannot be removed: a category's own `README.md`, which is
generated rather than written and whose refusal points at `spektacular init`. It also says plainly
that removal is immediate with no undo, and that recovery is whatever version control already gives
you.

**`src/pages/design-documents.mdx`** — two additions in the sections that already cover the
command line and refusals:

- `design delete` now sits with the other document verbs, between `design author` and the reference
  verbs. That placement is deliberate: the delete-versus-remove-a-reference distinction is the
  bridge into the reference commands. The prose states what each one leaves behind — `design ref
  remove` drops the pointer and leaves the document, `design delete` removes the document and
  refuses while any pointer remains — and names the trap explicitly.
- The `design_referenced_delete` refusal is shown in the "When a reference cannot be found" section,
  in the same JSON response shape that section already uses for `design_not_found`, including the
  runnable `design ref remove` steps its next action carries.

Both additions use the components and voice each page already has. No new component, no new import,
and no navigation change. The two pages differ in house style and each addition follows its own
page: the knowledge page uses a bolded lead-in, spaced JSON and `--file`, while the design page uses
compact JSON and `--from`.

## Why

The CLI gained removal for knowledge entries and design documents, and documentation that does not
mention a command is documentation that is wrong the moment the command exists. The design page's
addition does more than catch up, though: the distinction between deleting a design and dropping a
reference to one was already a trap for anyone reading that page, because the reference command
appears first and appears to succeed. Stating it explicitly is the point, not a side effect of
documenting a new verb.
