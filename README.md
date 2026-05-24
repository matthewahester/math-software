# math-software

Public-facing course resource site for **Intro to Mathematical
Software**, taught by Matt Hester at UA Little Rock. Sibling to the
main site [matthewhester.com](https://matthewhester.com); eventually
lives at `/math-software/` under that domain.

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
│   └── index.qmd                     # short conceptual notes (roadmap)
├── labs/
│   ├── index.qmd
│   └── lab01-install-stack.qmd       # install + render walkthrough
├── assignments/
│   ├── index.qmd
│   ├── hw01-setup.qmd
│   ├── project-latex.qmd
│   ├── project-r.qmd
│   └── final-portfolio.qmd
├── examples/
│   └── index.qmd                     # small code examples (roadmap)
├── resources/
│   ├── index.qmd
│   ├── software-setup.qmd
│   ├── ai-use-guidelines.qmd
│   └── cas-options.qmd
├── assets/README.md                  # figures and screenshots
├── styles.css                        # stone-toned palette + code-block tweak
├── CLAUDE.md                         # privacy + editing rules
└── _site_planning/                   # local-only planning (not published)
```

No CI, no deploy. Local builds only for now.
