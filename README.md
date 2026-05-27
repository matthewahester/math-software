# math-software

Public-facing course resource site for **Intro to Mathematical
Software**, taught by Matt Hester at UA Little Rock. Sibling to the
main site [matthewhester.com](https://matthewhester.com); served at
`/math-software/` under that domain via the hub repo's GitHub Pages
workflow.

This is a **curated public resource site**, not a raw course archive.
See [`CLAUDE.md`](CLAUDE.md) for what does and does not belong here.

## Local development

```bash
quarto render     # build to _site/
quarto preview    # live preview
```

## Layout

```
math-software/
├── _quarto.yml                       # site config, navbar, sidebar
├── index.qmd                         # landing page
├── syllabus.qmd                      # public syllabus summary
├── schedule.qmd                      # generic week-by-week topic map
├── notes/
│   ├── index.qmd                     # short conceptual notes (roadmap)
│   └── week01-first-render.qmd       # first conceptual note
├── labs/
│   ├── index.qmd
│   └── lab01-install-stack.qmd       # install + render walkthrough
├── examples/
│   └── index.qmd                     # small code examples (roadmap)
├── resources/
│   ├── index.qmd
│   ├── software-setup.qmd
│   ├── data-guidelines.qmd
│   ├── ai-use-guidelines.qmd
│   ├── ai-reading-spine.qmd
│   └── cas-options.qmd
├── assets/README.md                  # figures and screenshots
├── styles.css                        # stone-toned palette + code-block tweak
├── CLAUDE.md                         # privacy + editing rules
└── _site_planning/                   # local-only planning (not published)
```

## Public/private boundary

This site is the **course-text spine** only — notes, labs, resources,
syllabus summary, schedule outline. **Assignment prompts, rubrics,
file-naming conventions, submission instructions, due dates, and any
graded-prompt material live in the course LMS**, not on this site.
Do not reintroduce an `assignments/` directory or a `coursework.qmd`
page.

## Deploy

This site is rendered and deployed as part of the hub workflow in
`matthewahester/matthewhester-site` (manual `workflow_dispatch`). The
math-software repo itself has no GitHub Pages of its own.

## Standard stack

The course teaches a **VS Code + R + Quarto + TinyTeX** workflow.
See [`resources/software-setup.qmd`](resources/software-setup.qmd) and
[`labs/lab01-install-stack.qmd`](labs/lab01-install-stack.qmd).
