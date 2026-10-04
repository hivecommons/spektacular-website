## 000062_epic-plan-and-implement

The Epics page gains a "Planning and implementing an epic" section, linked from the page's opening explanation. It explains the two requests, "plan this epic" and "implement this epic": ready speks are worked on side by side by separate agents in dependency order, planning ends with a review of every plan produced, and implementing refuses up front when a spek has no plan or the dependencies are broken. It covers how each spek is built in its own git worktrees, one per repo it changes, and merged into every repo together before the speks that depend on it start, with a conflict stopping the run. It also says what still stops for you, what happens when a spek fails, and that repeating a request resumes where the epic stands and skips completed work, with an example of the `run` view `spektacular status` now reports for an epic.

## 000060_epics-and-seeded-specs

A new "Epics" reference page, reachable from the site's "Resources" menu right after Design Documents, explains how a request too big for one spek becomes an epic of speks that each carry their own acceptance criteria. It covers what an epic holds and how it links to its speks, when Spektacular offers a split and the signals and gate behind that offer, the `epic_split_threshold` sensitivity setting, what a split produces, starting from a tracker epic and chaining to its next child item, joining an epic and adding to a completed one, how dependencies between an epic's speks are checked when implementation starts (warning by default, refusing under `epic.strict_dependencies`), and the `epic` commands. The "How Spektacular Works" page now explains starting a spek from existing material such as an issue, a design document or a file, where the interview asks only about the gaps the material leaves and the spek records its `sources`, and the site now describes implementation as implementing a spek rather than a plan, on that page, the homepage pipeline and the getting-started tutorial. The Configuration page documents the new `epic_split_threshold` key and the `epic` section (`epic.provider`, `epic.strict_dependencies`, `epic.config.directory`), counts sixteen top-level keys, and notes that `migrate` adds both to existing projects.

The Plan Tasks page now documents the `status` command, which replaces `spec status`, `plan status`, `implement status` and `plan export`: one report, readable or JSON, covering an epic, each of its speks and every plan task, with the workflow in progress when there is one. Its "Status fields" reference replaces the old export fields, the Documents page's upgrade section gains a table mapping each removed command to its `status` replacement, and the "How Spektacular Works" page points at `spektacular status`.

## 000044_projects-feature-documentation

A new "Multi-Repo Projects" reference page explains how a Spektacular project can span more than one repository: why that's useful, how a repository is registered, how project and repository configuration relate to each other as one topic, how planning and implementation work is attributed across repos, how a repository becomes available locally, and how paths can be excluded from search. The page is reachable from the site's "Resources" navigation menu (listed first), and the getting-started tutorial now links to it at the point a reader following the single-repo walkthrough might otherwise assume a project can only ever contain one repository. The former separate "Repository Configuration" page has also been folded into the "Configuration" page, so project-level and per-repository configuration now read as one document instead of two.

## 000043_flipped-interaction-spec-interview

The "How Spektacular Works" page now describes the adaptive interview that opens every new spec, names it as the Flipped Interaction pattern with attribution to the prompt-engineering research it draws from, and walks through a worked example exchange along with a second example showing the interview asking about impact on another registered repo in a multi-repo project. The homepage's features grid now features this interview as one of its cards, so the capability is visible to a first-time visitor rather than only described on the deeper reference page.

## 000042_repo-self-describing-metadata

The Configuration page's registered-repository entry now documents only membership fields — name, address or local path, provider, and dependencies — since a repository's description, role, tags, and deployment moved to the repository's own configuration file. A new Repository Configuration reference page, linked from the Configuration page and added to the site's Resources navigation, documents that repository-level file in full, including its descriptive metadata alongside its existing knowledge and changelog settings.

## 000009_document-artifact-metadata-and-historical-artifacts

The "How Spektacular Works" page now explains that once a spec or plan is
written, coding agents treat it as a historical record of past intent
rather than a live description of current behavior, answering "how does
this work today" from the code itself, while still opening and citing the
original spec, plan, or changelog entry when asked why something was built
a certain way. The Configuration page now notes that every spec, plan, and
changelog record automatically tracks a creation date, a status, and a
closed date, and adds a new section with example commands for listing and
filtering a project's own records by that metadata, including one command
that queries across specs, plans, and changelog entries at once.

## 000008_debugging-docs

Spektacular's debug logging is now correctly documented and easy to find.
A new Debugging page walks through turning it on, where the resulting log
file lives, and what one logged entry looks like, replacing the
Configuration page's old, inaccurate claim that debug mode prints to the
console. The top navigation gains a "Resources" menu that groups Plugins,
Extending, and the new Debugging page together, so all three are
reachable without already knowing their URLs, and without adding a new
top-level nav item.

## 000007_video-element

Tutorials and documentation pages can now embed a YouTube video directly
alongside the written content. Authors provide a video's URL and get a
playable YouTube player rendered in the same spot, sized, and styled
consistently with how an image appears in the same location. Authors can
optionally set a start time and an end time so playback covers just the
relevant portion of a longer video, and can turn off the player's fullscreen
control when it isn't wanted. Playback itself uses YouTube's own default
controls, with no custom player UI.

## 000006_document-context

The Spektacular website has a new Knowledge Base page, reachable from the top
navigation right after "How it works". It explains what the knowledge base is
and the problem it solves, walks through the six categories of knowledge and the
two ways they are retrieved, shows how an entry is created, searched, and kept up
to date, and covers how the knowledge base is configured and where that
configuration lives, including pointing at more than one source. A closing
section explains why the subsystem is designed the way it is, so readers come
away understanding not just how to use it but why to trust it.

## 000005_tutorial-section

The Spektacular website now has a Tutorials section reachable from
the top nav. Each tutorial is a single MDX file in a new content
collection, and the index page lists every published tutorial as a
clickable card. Every tutorial page carries an agent selector
(default Bob, plus Claude and Codex) at the top that swaps per-step
instructions and screenshots between the supported coding agents
without a page reload; the choice is persisted across visits. The
first tutorial, "How to use Spektacular", walks a reader through
the end-to-end workflow from install to implement. Per-agent
screenshots ship as labelled placeholders pending real captures.

## 000004_astro-migration

The Spektacular website has moved off Hugo onto Astro 5 with MDX and
Tailwind CSS v4. Each page now lives in a single `.mdx` file that
composes named blocks (`<Hero>`, `<Pipeline>`, `<FeaturesGrid>`,
`<CtaBanner>`, etc.) and carries its own prose, so changing a sentence
or a section no longer means editing both a markdown content file and
a separate layout template. The visual design, every URL, hosting on
GitHub Pages, and the `spektacular.dev` custom domain are preserved
unchanged; contributors get a faster dev loop (Vite HMR), typed
component props, and a single file to open per page.

## 000003_update-content

The Spektacular website now matches what the tool actually does today.
Inaccurate claims about a Bubble Tea TUI, complexity-driven model
routing, and Aider/Cursor agent support have been removed from the
homepage and how-it-works page. Three new top-level pages — Configuration,
Plugins, and Extending — document the real `.spektacular/config.yaml`
schema, the pluggable Store and Agent architecture, the three shipping
agents (Claude, Bob, Codex), and the Go interfaces a developer
implements to add their own backend. The install page's broken apt
channel has been replaced with a `go install` block, and the GitHub
Releases artifact names match the current release scheme.

## 000002_static-site-generation

The Spektacular website has moved off hand-built HTML onto the Hugo
static site generator with Tailwind CSS v4. The three pages (homepage,
how-it-works, install) now share a single source of truth for
navigation, header, and footer — editing them in one place updates
every page. Hosting and the `spektacular.dev` custom domain are
unchanged; URLs adopt Hugo's defaults (`/install/` instead of
`/install.html`). Contributors can now add or update pages by editing
Markdown content and Hugo layouts instead of copy-pasting full HTML
documents.

## 1_install_instructions

Added a dedicated Install page to the Spektacular website with tabbed
instructions for Homebrew, Debian/Ubuntu, and GitHub Releases — making it
easy for new users to get Spektacular running regardless of their platform.
The Install page is now linked from the top navigation on every page, and
the homepage hero has been updated to show the Homebrew install command as
the recommended path.
