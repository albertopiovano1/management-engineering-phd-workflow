# AGENTS.md — Codex workflow for PhD research

## Context

This repository supports PhD work in management engineering:
literature reviews, academic papers, R analyses, slides, and replication packages.

The `.claude/` directory is a reference library from the original Claude Code workflow.
Use it for ideas and checklists, but do not treat Claude-specific commands, hooks, or agents
as Codex runtime features.

## Core rules

- Plan before editing non-trivial files; explain the intended changes first.
- Keep changes small, reversible, and scoped to the task.
- Do not rewrite large parts of the repository unless explicitly asked.
- Prefer relative paths and reproducible workflows.
- Verify outputs when tools are available.

## Main workflows

### Literature review

- Start from the user's research question or seed papers.
- Search for seminal and recent work when requested.
- Organize findings by theory, empirical evidence, methods, and gaps.
- Do not invent citations; flag uncertain references for manual verification.
- Save substantial review notes under `quality_reports/`.

### Paper review and writing

- Preserve the author's argument and academic voice unless asked to rewrite.
- Separate substantive feedback from copyediting.
- Check research question, contribution, theory, data, methods, results, and limitations.
- Verify numerical claims against code outputs when possible.

### R data analysis

- Inspect data before writing analysis code.
- Put R scripts in `scripts/R/` and generated outputs in `scripts/R/_outputs/` when appropriate.
- Use `library()` calls at the top, relative paths, and `file.path()`.
- Use one `set.seed()` near the top when randomness is involved.
- Save important intermediate objects with `saveRDS()`.

### Slides

- Ask whether the target format is Beamer, Quarto, or both.
- Use `Slides/` for Beamer and `Quarto/` for Quarto.
- Avoid maintaining duplicate versions unless explicitly requested.
- Compile or render after material edits when the tools are available.

### Replication packages

- Inventory data, scripts, inputs, outputs, and expected results first.
- Record target numbers from the paper before modifying code.
- Reproduce baseline results before extending the analysis.
- Document mismatches, tolerance rules, software versions, and run instructions.

## Git

- Do not commit unless explicitly asked.
- Before committing, summarize changed files and checks run.
