# CLAUDE.md — math-software

Notes for Claude Code (or any AI assistant) working in this repo.

## What this repo is

A **public-facing course resource site** for Matt Hester's Intro to
Mathematical Software course. It is a sibling of the main site at
[matthewhester.com](https://matthewhester.com) and is served at
`/math-software/` under that domain via the hub repo's GitHub Pages
workflow.

This is **not** a raw course archive. The course LMS owns dates,
rosters, grades, assignment prompts, rubrics, and submission
contracts. This site holds curated, sanitized, public-safe material:
conceptual notes, hands-on labs, software/resource references, and
the high-level syllabus and schedule outlines.

## Privacy and publication rules

**Do not publish:**

- Student data (any kind: identifiable, deidentified, or aggregated
  from a small section).
- Class rosters, grade distributions, or anything pulled from the
  course LMS.
- Internal school documents (committee notes, internal policy memos,
  emails, accreditation materials).
- FERPA-adjacent material — work samples that came from identifiable
  students, recorded class sessions, gradebook screenshots, etc.
- Verbatim institutional policy text. Summarize and link instead.

**Be careful with:**

- Material copied wholesale from the school archive. Do **not** bulk-
  import; curate piece by piece and sanitize each one.
- Screenshots that incidentally include student names, emails,
  repository URLs, or anything from a class section.
- Code examples derived from student submissions.

When unsure, default to **don't publish** and ask.

## Public/private boundary

- **This site = course-text spine.** Conceptual notes, lab
  walkthroughs, resources, syllabus summary, schedule outline.
- **Course LMS = graded prompts.** Assignment prompts, rubrics,
  point values, file-naming conventions, submission instructions,
  due dates.
- **Do not reintroduce** an `assignments/` directory, a
  `coursework.qmd` page, HW-numbered prompts, rubrics, or submission
  contracts on this site.

## Standard course stack

The course standard is **VS Code + R + Quarto + TinyTeX**. VS Code is
the editor; R is the primary computation language. **RStudio is not
the standard** — it is mentioned only as an optional alternative in
[`resources/software-setup.qmd`](resources/software-setup.qmd) and in
the "I keep finding RStudio instructions online" troubleshooting
section of [`labs/lab01-install-stack.qmd`](labs/lab01-install-stack.qmd).
Do not lead with RStudio anywhere on the site.

## Design intent

- Loose visual match to the main site and `intro-stats` — same
  stone/iron palette and restraint. Do not introduce new accent
  colors.
- Quarto sidebar/book-like structure. Navbar holds Home / Syllabus /
  Schedule; sidebar holds Notes / Labs / Examples / Resources.
- Plain CSS, no JS, no SCSS pipeline.
- Code blocks get slightly heavier styling than on `intro-stats`
  because this course shows more code.

## Editing rules

- Top-level pages: `index.qmd`, `syllabus.qmd`, `schedule.qmd`.
  Section landing pages: `notes/index.qmd`, `labs/index.qmd`,
  `examples/index.qmd`, `resources/index.qmd`.
- Each section will grow into multiple sibling `.qmd` files; add new
  files in the matching directory and update the sidebar in
  `_quarto.yml`.
- Supporting figures and screenshots go in `assets/`.
- `_site_planning/` is local-only — excluded from render and not part
  of the public site.

## Build and deploy

- Local: `quarto render` from repo root. Output goes to `_site/`
  (gitignored).
- Live deploy: the hub repo `matthewahester/matthewhester-site` has
  a `workflow_dispatch` GitHub Actions workflow that checks out this
  repo, renders it, and assembles `_site/math-software/` for the
  combined Pages deployment at `matthewhester.com/math-software/`.
  This repo itself has no GitHub Pages config.
