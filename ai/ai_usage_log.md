# AI Usage Log: HamSCI Ray Tracing

This log records every substantive AI-assisted session on the project "Ionospheric Model
Validation and Development of an Open-Source HF Ray-Tracing Toolkit Leveraging HamSCI Citizen
Science Data" (NASA award 80NSSC26K0051), carried out under the HamSCI Ray Tracing working
group.

Required by the HamSCI Generative AI Use Agreement, and by any institutional or funder policy
that applies to this project (see `.claude/rules/ai-governance.md`).

**This log is the source of truth for what AI did on this project.** A disclosure paragraph in a
manuscript, poster, website page, or software release summarizes this log truthfully. Keep it
current: an entry written from memory weeks later is not a record.

## Entry format

```
## [YYYY-MM-DD HH:MM TZ]
- **Tool**: Claude (Anthropic), <exact-model-id>
- **Session Purpose**: What the session set out to accomplish
- **Sections/Files Affected**: Specific files, sections, or documents touched
- **Nature of Contribution**: Draft / Edit / Analysis / Code generation / Research / Scaffolding
- **Human Review Status**: Reviewed and verified / Partially reviewed / Pending review
- **Git Hash**: <filled in after committing>
```

The date and time come from the system clock via `date`, never from an estimate. The `/commit`
command produces this format and appends it in the right order.

---

<!-- Append new entries below this line, newest at the bottom. -->
<!-- The template-merge entry that previously stood here (git hash 8059027) belonged to the
     hamsci-wg / ai_project_template merge, not to this project, and was cleared per the
     README's instantiation checklist. -->

## [2026-09-23 02:12 EDT]
- **Tool**: Claude (Anthropic), claude-sonnet-5
- **Session Purpose**: Instantiate the HamSCI Ray Tracing working group repo from the merged
  hamsci-wg/ai_project_template scaffold with real team/funder/working-group details; replace
  leftover content from a different (WWV/H) working group on the public docs/ site; add a
  LICENSE; then, per PI direction, update the public docs and CLAUDE.md to reflect (1) the
  technical pivot from extending PyLap/PHaRLAP to a native-Python 3D ray-tracing engine based on
  the Jones & Stephenson (1975) formulation, and (2) the project's actual schedule — an official
  period of performance of February 2026 – January 2029 (5-month shift from the proposal's
  nominal Sept 2025 – Aug 2028), with active work practically starting mid-May 2026 due to the
  PI's leave while the January 2029 end date has not moved. Built and ran the Jekyll site locally
  to review before committing, which surfaced and fixed several real bugs: an empty-comment
  `datasets.bib` that crashed the BibTeX parser; two internal links (`/about/`, `/results/`) that
  ignored the site's baseurl; a "new issue" link inherited from the template that pointed at the
  wrong domain; two dead external links (PSWS/GRAPE, Madrigal Database) replaced with working
  ones found via web search and verified with curl; and a bibliography entry (Hozumi 2024b) whose
  raw `.pptx` file URL was replaced with no url field, consistent with the other entries' stable
  landing-page links. Also removed a dead-end empty "Table of Contents" block on the Mission page.
- **Sections/Files Affected**: CLAUDE.md, README.md, CITATION.cff, LICENSE.txt (new),
  .claude/rules/ai-governance.md, ai/ai_usage_log.md, docs/_config.yml, docs/index.md,
  docs/1_about.md, docs/2_mission.md, docs/3_goals.md, docs/4_minutes.md, docs/5_resources.md,
  docs/_bibliography/publications.bib, docs/_bibliography/datasets.bib, docs/Gemfile.lock,
  src/README.md; deleted .claude/rules/latex-writing.md, ai/GETTING_STARTED.md,
  docs/publications.bib (stray duplicate)
- **Nature of Contribution**: Scaffolding, edit, drafting of public-facing website copy, research
  (link verification via WebSearch/curl), local build verification
- **Human Review Status**: Reviewed and verified by the PI (Kornyanat Hozumi) during the session,
  including a live local preview of every page
- **Git Hash**: 926210f

## [2026-10-23 11:37 MDT]
- **Tool**: Claude (Anthropic), claude-sonnet-5
- **Session Purpose**: Add a second funder (ONR, award N000142612000) to the public site and
  CLAUDE.md, scoped per the PI's explicit instruction to only the ray-tracing-relevant parts of
  that broader ONR proposal (Navy operational model validation; ESF diagnostic ray tracing),
  excluding VIPIR instrumentation, SEALION/AOSWA collaboration, and other non-raytracing content.
  Corrected two issues during drafting at the PI's direction: (1) wording that implied the
  ray-tracing engine was "NASA/ONR-developed" rather than developed by the PI with NASA/ONR
  funding, and (2) a now-canceled VIPIR station location (Ho Chi Minh City, Vietnam) that the PI
  asked not to name anywhere, public or internal. Verified with a local Jekyll build that the
  canceled station name does not appear anywhere in the built site.
- **Sections/Files Affected**: CLAUDE.md, README.md, docs/index.md, docs/1_about.md
- **Nature of Contribution**: Edit, drafting of public-facing website copy
- **Human Review Status**: Reviewed and verified by the PI (Kornyanat Hozumi); final About-page
  wording shown to and approved by her before committing
- **Git Hash**: 8dafe9e

## [2026-10-23 11:39 MDT]
- **Tool**: Claude (Anthropic), claude-sonnet-5
- **Session Purpose**: Fix a broken deployment discovered right after pushing the ONR commit
  above: the just-run "Deploy Jekyll with Plugins" workflow failed because `ubuntu-latest`
  migrated to Ubuntu 26.04 (GitHub's scheduled Oct 19, 2026 migration, flagged as a warning in
  this workflow's runs since September), and the pinned `ruby-version: '2.7'` has no prebuilt
  release for that image. Pinned both jobs to `ubuntu-24.04` (the image this workflow ran on
  successfully before) instead of the floating `ubuntu-latest` tag, to fix the immediate break
  and avoid the same failure on the next scheduled image migration. Not a content change; this
  was caught and fixed without separate PI review given its mechanical, low-risk nature, then
  reported to her.
- **Sections/Files Affected**: .github/workflows/pages.yml
- **Nature of Contribution**: Bug fix (CI/CD configuration)
- **Human Review Status**: Pending review (reported to PI; not separately re-confirmed before
  commit, per the above)
- **Git Hash**: 9fd883e

## [2026-10-23 11:53 MDT]
- **Tool**: Claude (Anthropic), claude-sonnet-5
- **Session Purpose**: Extend the ONR ray-tracing-only acknowledgment (added earlier this
  session) to the Mission and Goals pages, at the PI's request, and record the ONR award's
  corrected period of performance (December 1, 2025 – November 30, 2028, delayed from the
  proposal's nominal ~September 2025 start). Kept the same scoping discipline as the About page:
  only the two ray-tracing-relevant ONR objectives (Navy model validation; ESF diagnostic ray
  tracing) were added, as new Mission bullets and new Goals objectives 6-7, with a short timeline
  note rather than reproducing the ONR proposal's full POA&M table (most of its rows are
  VIPIR/instrumentation/diagnostic-catalog items outside ray tracing, and no revised per-milestone
  dates were provided to go with the corrected start). Updated CLAUDE.md's Funder field to match.
- **Sections/Files Affected**: CLAUDE.md, docs/2_mission.md, docs/3_goals.md
- **Nature of Contribution**: Edit, drafting of public-facing website copy
- **Human Review Status**: Reviewed and verified by the PI (Kornyanat Hozumi); final wording
  shown to and approved by her before committing
- **Git Hash**: 251b4dc

## [2026-10-23 12:07 MDT]
- **Tool**: Claude (Anthropic), claude-sonnet-5
- **Session Purpose**: Restructure the ONR funding attribution after the PI flagged the prior
  version as asymmetric (ONR objectives tagged "through separate funding"/"(ONR-funded)" inline,
  while NASA's weren't) and redundant (the two ONR objective descriptions were duplicated on both
  About and Goals). Settled on one place per kind of information: About states both funders
  briefly and symmetrically with no objective-level detail; Goals carries the objective detail
  with a single funder-split line before one combined numbered list (no more per-item tags);
  Mission describes scope with no inline funder mentions at all. Updated CLAUDE.md to document
  this settled layout so it isn't redrafted back into the asymmetric form later.
- **Sections/Files Affected**: CLAUDE.md, docs/1_about.md, docs/2_mission.md, docs/3_goals.md
- **Nature of Contribution**: Edit, drafting of public-facing website copy
- **Human Review Status**: Reviewed and verified by the PI (Kornyanat Hozumi); final wording
  shown to and approved by her before committing
- **Git Hash**: 066ad82
