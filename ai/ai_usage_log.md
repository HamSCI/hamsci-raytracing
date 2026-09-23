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
