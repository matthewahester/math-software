# CLAUDE.md — math-software

Notes for Claude Code (or any AI assistant) working in this repo.

## What this repo is

A **public-facing course resource site** for Matt Hester's Intro to
Mathematical Software course. It is a sibling of the main site at
[matthewhester.com](https://matthewhester.com) and will eventually
live at `/math-software/` under that domain.

This is **not** a raw course archive. The LMS still owns dates,
rosters, grades, and the full syllabus. This site holds curated,
sanitized, public-safe material: tool walkthroughs, conceptual notes,
small reproducible code examples, and links to outside resources.

## Privacy and publication rules

**Do not publish:**

- Student data (any kind: identifiable, deidentified, or aggregated
  from a small section).
- Class rosters, grade distributions, or anything pulled from the LMS.
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

## Design intent

- Loose visual match to the main site and `intro-stats` — same
  stone/iron palette and restraint. Do not introduce new accent
  colors.
- Quarto sidebar/book-like structure. Navbar holds Home / Syllabus /
  Schedule; sidebar holds Notes / Labs / Assignments / Examples /
  Resources.
- Plain CSS, no JS, no SCSS pipeline.
- Code blocks get slightly heavier styling than on `intro-stats`
  because this course shows more code.

## Editing rules

- Top-level pages: `index.qmd`, `syllabus.qmd`, `schedule.qmd`.
  Section landing pages: `notes/index.qmd`, `labs/index.qmd`,
  `assignments/index.qmd`, `examples/index.qmd`,
  `resources/index.qmd`.
- Each section will grow into multiple sibling `.qmd` files; add new
  files in the matching directory and update the sidebar in
  `_quarto.yml`.
- Supporting figures and screenshots go in `assets/`.
- `_site_planning/` is local-only — excluded from render and not part
  of the public site.

## Build

- `quarto render` from repo root.
- Output goes to `_site/` (gitignored).
- No CI yet. Local-only until the main site goes live.
