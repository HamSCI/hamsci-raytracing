# HamSCI Ray Tracing

## Project Overview
HamSCI Ray Tracing is a HamSCI working group for amateur radio operators, citizen scientists,
software developers, and professional researchers interested in HF propagation and ionospheric
science. It develops and promotes open-source HF ray-tracing tools — a 3D HF ray-tracing engine
implemented natively in Python from the Jones & Stephenson ray-tracing formulation, rather than
wrapping the team's earlier PyLap/PHaRLAP toolchain — validates ionospheric models (e.g., IRI,
SAMI3, coupled SAMI3/WACCM-X) against
HamSCI observational data (RBN, PSKReporter, WSPRNet, and PSWS/GRAPE Doppler receivers), and
studies space weather effects on anomalous HF propagation, including Equatorial Plasma Bubbles
(EPBs) and understudied off-great-circle (side-scatter) paths. The audience is HamSCI volunteers,
licensed amateur radio operators, students, and ionospheric/HF propagation researchers.

This repository holds the working group's public website and the group's shared work. It
combines two HamSCI scaffolds:

- the working group website template
  ([`HamSCI/hamsci-wg`](https://github.com/HamSCI/hamsci-wg)), which supplies `docs/`,
  `Gemfile`, and the GitHub Pages workflow, and
- the AI project template
  ([`HamSCI/ai_project_template`](https://github.com/HamSCI/ai_project_template)), which supplies
  this file, `.claude/`, and `ai/`.

**Lead**: Dr. Kornyanat Hozumi (PI), University of Scranton
**Collaborators**:
- Dr. Nathaniel Frissell, W2NAF (Co-I and Scientific PI; HamSCI founder), University of Scranton
- Dr. Mark Fenner (Co-I; software engineering, numerical methods), University of Scranton
- Gary Mikitin, AF8A (Amateur Radio Coordinator)
- Gwyn Griffiths, G3ZIL (off-great-circle/side-scatter propagation)
- Bob Gerzoff, WK2Y (model validation techniques)
- Dr. Mary Lou West, KC2NMC (tutorials), Professor Emerita, Montclair State University
- Dr. Joseph Huba (Ionospheric Model Consultant; SAMI3 and SAMI3/WACCM-X model output)
- A Scranton Graduate Research Assistant (software engineering, model validation) — not yet named

**HamSCI Working Group**: HamSCI Ray Tracing (https://hamsci.org/working-group/raytracing-wg)
**Institution**: University of Scranton
**Funder**: Two awards, both PI Kornyanat Hozumi / University of Scranton:
- NASA ROSES 2024 B.21 Heliophysics Citizen Science Investigations (H-CSI), award/grant no.
  80NSSC26K0051, "Ionospheric Model Validation and Development of an Open-Source HF Ray-Tracing
  Toolkit Leveraging HamSCI Citizen Science Data" — this is the primary funder for the whole
  project described in this file.
- ONR (Office of Naval Research), award N000142612000, "Crowdsourced Observations for
  Ionospheric Model Validation and a Diagnostic Approach for Forecasting Equatorial Spread F",
  period of performance **December 1, 2025 – November 30, 2028** (the ONR proposal's own schedule
  assumed a ~September 2025 start, labeled FY26–FY28; that start was delayed, so those FY labels
  no longer line up with the actual dates — do not reuse the proposal's FY26/FY27/FY28 date
  ranges without checking against this corrected period first) — a broader Navy-focused project
  (it also funds VIPIR ionosonde deployment and ESF
  diagnostic/instrumentation work — the originally planned Ho Chi Minh City, Vietnam station has
  since been canceled; do not name it anywhere, public or internal notes, without checking with
  the PI for current status). **Only its ray-tracing-related portion belongs on this
  public site**: (1) validating Navy models (e.g., NIMO) via the same raytracing-against-HamSCI
  methodology as the NASA work, and (2) using 3D raytracing on parametric ionospheric scenes to
  synthesize ionogram-like signatures for Equatorial Spread F (ESF) diagnostics. The ONR
  proposal's written text names PHaRLAP/PyLap as the raytracing tool for this; that has since
  changed (PI-confirmed, ONR program manager approved) to the same open-source native-Python
  engine the PI is developing with NASA funding — do not describe the ONR work as using
  PHaRLAP/PyLap, and do not describe the engine itself as "NASA-developed" (NASA funds the work;
  the PI wrote the code). Do not add the ONR award's VIPIR/SEALION/AOSWA/instrumentation content
  here — that is out of scope for the
  ray-tracing working group's site. This same ray-tracing-only scoping applies to
  `docs/1_about.md`, `docs/2_mission.md`, and `docs/3_goals.md`. Settled layout (2026-10-23,
  after the PI flagged an earlier draft as redundant/asymmetric — do not revert to per-bullet
  "(ONR-funded)"/"through separate funding" tags, and do not re-duplicate the two ONR objectives'
  full descriptions onto the About page):
  - `docs/1_about.md`: brief, symmetric acknowledgment of both funders only (one short paragraph
    each, same level of detail) — no objective-level bullets; points to Goals for specifics.
  - `docs/3_goals.md`: the one place with objective-level detail. One line states the funder
    split ("Objectives 1–5 ... NASA ...; objectives 6–7 ... ONR") before the combined numbered
    list; individual objectives are not re-tagged by funder.
  - `docs/2_mission.md`: describes the mission/scope with no inline funder mentions at all
    (NASA's parts aren't tagged either, so tagging only ONR's was asymmetric); points to About
    for funding.
**Project period**: February 2026 – January 2029 (official period of performance; the proposal's
nominal period was September 2025 – August 2028, a 5-month shift). Active work practically began
mid-May 2026 (PI's leave); the official end date, January 2029, has **not** been extended to
compensate — see the Work Plan note on `docs/3_goals.md`.
**Website**: https://hamsci.github.io/hamsci-raytracing
**Mailing list / meetings**: [Google Group](https://groups.google.com/g/hamsci-ray-tracing?pli=1);
bi-weekly meetings, announced on the mailing list

## Project Goal
Develop and validate an open-source, 3D HF ray-tracing toolkit — implemented natively in Python
from the Jones & Stephenson ray-tracing formulation — using HamSCI citizen-science data to
validate ionospheric models and to study space-weather-driven anomalous HF propagation (EPBs,
off-great-circle paths), while training and engaging citizen scientists through documentation and
bi-weekly seminars.

## Software: `src/`
The 3D ray-tracing toolkit is under active development in the PI's private repository. `src/`
here is currently a **placeholder**: vetted, publishable components will be ported in as they
mature (see `src/README.md`). Do not assume ray-tracing code exists in this repo yet.

**Technical approach note**: the funded proposal's text (and this repo's early scaffolding)
describes extending the team's 2D PyLap/PHaRLAP toolchain to 3D. As of September 2026 the PI has
instead moved to a from-scratch 3D ray-tracing engine implemented natively in Python, based on
the Jones & Stephenson ray-tracing formulation, independent of PyLap/PHaRLAP's proprietary core.
PyLap remains relevant as the team's prior related work. Do not assume PyLap-extension framing
elsewhere (older notes, the proposal PDF) reflects the current implementation plan.

## Standing Rules

These two are binding on every HamSCI project and are imported here so they load into context
automatically:

@.claude/rules/ai-governance.md
@.claude/rules/hamsci-data.md

One further rule file is optional, scoped by its own `paths:` frontmatter to the file types it
governs:

- `.claude/rules/python-code.md` applies to `.py`, `pyproject.toml`, and `requirements*.txt`

(`.claude/rules/latex-writing.md` was removed: there is no LaTeX in this repo. Re-add it, e.g.
from `HamSCI/ai_project_template`, if a manuscript or Overleaf submodule is added later.) To have
a rule file load unconditionally instead, add an `@` import line for it above.

## Repository Structure

```
hamsci-raytracing/
├── CLAUDE.md                     ← this file; project instructions for Claude
├── README.md                     ← working group description
├── LICENSE.txt                   ← MIT
├── CITATION.cff                  ← make the repository citable
├── Gemfile                       ← Jekyll dependencies
├── .gitignore
├── .claude/
│   ├── settings.json
│   ├── commands/commit.md        ← /commit workflow
│   └── rules/
│       ├── ai-governance.md      ← required
│       ├── hamsci-data.md        ← required
│       └── python-code.md        ← delete if no Python
├── .github/
│   ├── ISSUE_TEMPLATE/
│   └── workflows/pages.yml       ← builds and deploys the website
├── ai/
│   └── ai_usage_log.md           ← mandatory AI session log
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
