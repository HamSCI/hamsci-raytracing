# AI Usage Log: {{PROJECT_NAME}}

This log records every substantive AI-assisted session on the project "{{PROJECT_TITLE}}".

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

<!-- Append new entries below this line, newest at the bottom.
     On instantiating a new working group repository from this template, delete every entry
     below: they belong to the template's own development, not to your project. -->

## [2026-09-22 21:03 UTC]
- **Tool**: Claude (Anthropic), claude-opus-5[1m]
- **Session Purpose**: Make the HamSCI working group website template compatible with
  `HamSCI/ai_project_template`, by merging that template's governance scaffolding (CLAUDE.md,
  `.claude/` rules and commands, the AI usage log, and the getting-started guide) into the
  working group scaffold without disturbing the Jekyll site under `docs/`.
- **Sections/Files Affected**: `CLAUDE.md` (new), `.claude/settings.json` (new),
  `.claude/commands/commit.md` (new), `.claude/rules/ai-governance.md`,
  `.claude/rules/hamsci-data.md`, `.claude/rules/latex-writing.md`,
  `.claude/rules/python-code.md` (all new, copied unchanged from the AI project template),
  `ai/ai_usage_log.md` (new), `ai/GETTING_STARTED.md` (new, adapted from the AI project
  template's `docs/GETTING_STARTED.md`), `.gitignore` (new), `README.md`, `CITATION.cff`
- **Nature of Contribution**: Scaffolding and adaptation of two existing templates
- **Human Review Status**: Pending review by N. A. Frissell (W2NAF)
- **Git Hash**: [pending commit]
