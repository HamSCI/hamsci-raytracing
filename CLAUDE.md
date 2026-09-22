# {{PROJECT_NAME}}

## Project Overview
{{ONE-PARAGRAPH DESCRIPTION OF THE WORKING GROUP: what it is investigating or building, its
purpose, and its audience.}}

This repository holds a HamSCI working group's public website and the group's shared work. It
combines two HamSCI scaffolds:

- the working group website template
  ([`HamSCI/hamsci-wg`](https://github.com/HamSCI/hamsci-wg)), which supplies `docs/`,
  `Gemfile`, and the GitHub Pages workflow, and
- the AI project template
  ([`HamSCI/ai_project_template`](https://github.com/HamSCI/ai_project_template)), which supplies
  this file, `.claude/`, and `ai/`.

**Lead**: {{LEAD_NAME_CALLSIGN_AND_AFFILIATION}}
**Collaborators**: {{COLLABORATORS: names, callsigns, and roles}}
**HamSCI Working Group**: {{WORKING_GROUP}}
**Institution**: {{INSTITUTION, or "none: this is a volunteer project"}}
**Funder**: {{FUNDER_AND_GRANT_NUMBER, or "unfunded"}}
**Project period**: {{PROJECT_PERIOD}}
**Website**: https://hamsci.github.io/{{REPO_NAME}}
**Mailing list / meetings**: {{HOW TO JOIN, or "none"}}

## Project Goal
{{PROJECT_GOAL, 1 to 3 sentences.}}

## Standing Rules

These two are binding on every HamSCI project and are imported here so they load into context
automatically:

@.claude/rules/ai-governance.md
@.claude/rules/hamsci-data.md

Two further rule files are optional, and are scoped by their own `paths:` frontmatter to the
file types they govern:

- `.claude/rules/latex-writing.md` applies to `.tex`, `.bib`, `.cls`, and `.sty` files
- `.claude/rules/python-code.md` applies to `.py`, `pyproject.toml`, and `requirements*.txt`

Delete whichever the project does not use. To have one of them load unconditionally instead, add
an `@` import line for it above.

## Repository Structure

```
{{REPO_NAME}}/
├── CLAUDE.md                     ← this file; project instructions for Claude
├── README.md                     ← working group description and setup checklist
├── LICENSE                       ← add one; see the README checklist
├── CITATION.cff                  ← make the repository citable
├── Gemfile                       ← Jekyll dependencies
├── .gitignore
├── .claude/
│   ├── settings.json
│   ├── commands/commit.md        ← /commit workflow
│   └── rules/
│       ├── ai-governance.md      ← required
│       ├── hamsci-data.md        ← required
│       ├── latex-writing.md      ← delete if no LaTeX
│       └── python-code.md        ← delete if no Python
├── .github/
│   ├── ISSUE_TEMPLATE/
│   └── workflows/pages.yml       ← builds and deploys the website
├── ai/
│   ├── ai_usage_log.md           ← mandatory AI session log
│   └── GETTING_STARTED.md        ← delete once the project is running
├── docs/                         ← the public website (Jekyll source)
│   ├── _config.yml
│   ├── index.md, 1_about.md, …   ← pages appear in the nav in filename order
│   ├── _bibliography/            ← jekyll-scholar .bib files
│   ├── _includes/
│   └── assets/
├── hardware/                     ← board layouts, 3D printing files, editable sources
└── src/                          ← software, or a pointer to the repository that holds it
```

Add or remove top-level directories to match the working group: `notes/`, `data/`, `posters/`,
`manuscript/`. Delete `hardware/` or `src/` if the group has no hardware or software.

## The Website

`docs/` is the source of a Jekyll site built with the `minima` theme and the `jekyll-scholar`
plugin, deployed to GitHub Pages by `.github/workflows/pages.yml` on every push to `main`.

**Everything committed under `docs/` is published on the public web.** Treat AI-drafted page copy
as published output: a human reviews it before it is committed, and the AI-use rules in
`.claude/rules/` apply to it in full. Roster and station pages need particular care, because
callsigns and grid squares identify real operators (`.claude/rules/hamsci-data.md`).

- Pages carry `layout`, `title`, and `permalink` front matter; the header nav lists pages that
  have a `title`, in filename order, which is what the numeric filename prefixes control.
- Bibliographies live in `docs/_bibliography/` and are rendered by `jekyll-scholar`. Cite only
  work that has been verified against the actual source.
- `docs/_config.yml` carries the site `title`, `description`, and `baseurl`. The `baseurl` must
  match the repository name for links to resolve.
- Build locally with `cd docs && bundle install && bundle exec jekyll serve`.
- Do not edit `_site/`; it is generated output and is gitignored.

## Working Conventions

**Session notes.** Keep one dated notes file per working session in `notes/`, named
`YYYY-MM-DD_<topic>.md`, recording what was decided, why, what it depends on, and what is still
open. Write them for a reader with no context, which in practice means a future Claude session
and a future you.

**Commits.** Use the `/commit` command. It logs the AI session, commits submodules first, then
commits the main repo. Prefix AI-assisted commits with `[AI-assisted]`. Reference tracking
issues (`refs #N`, or `closes #N` only when completion is yours to declare).

**Never push without explicit instruction.** Never force-push or hard-reset. Fetch and verify
remote state before any push. A push to `main` republishes the website.

**Project boards and issue status are human-curated.** Read them freely; propose changes and
name the exact command rather than running it.

## Submodules (optional)

If the project includes submodules (an Overleaf manuscript, a separate code repository, a
hardware design repo), the commit and push order is fixed:

1. Commit **inside** the submodule
2. Commit the updated submodule pointer in this repo
3. Push the submodule
4. Push this repo

Never the reverse at either stage. A parent pushed ahead of its submodule looks correct on the
machine that did it and breaks for every clone, because the recorded pointer names a commit no
remote has. Verify before pushing a parent:

```bash
git -C <submodule> branch -r --contains HEAD   # empty output = local only; push the submodule first
```

Add submodules with:

```bash
git submodule add https://git.overleaf.com/<id> overleaf      # Overleaf manuscript
git submodule add git@github.com:HamSCI/<repo>.git <path>     # HamSCI code repo
```

The `/commit` workflow auto-detects submodules via `git submodule status`.

## AI Governance

Every substantive AI session is logged in `ai/ai_usage_log.md` **before** the work is committed.
Use `/commit`, which enforces the ordering. The full policy stack is in
`.claude/rules/ai-governance.md`, which is imported above. Published outputs, including the
website, disclose AI use where AI produced or substantially shaped their content.
