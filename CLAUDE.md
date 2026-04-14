# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Purpose

This is a curated collection of AI articles captured in a consistent markdown format. Articles are sourced from the web (HTML pages, online PDFs, or attached PDFs) and summarised using a structured capture prompt ("Cappy") defined in `prompt/cappy_capture_articles.md`.

## Repository Structure

- `articles/` — Individual article summaries in markdown, named `kebab-case-title-YYYYMMDD.md` (date = capture date)
- `glossary/definitions-and-acronyms.md` — AI terminology organised by category in table format, alphabetically ordered within each category
- `local/` — Git-ignored directory for local working files (PDFs, downloaded articles). Used when a web source cannot be fetched directly and the user provides a local copy instead
- `prompt/cappy_capture_articles.md` — The capture prompt/instructions used to process articles
- `README.md` — Article index with links organised under five category headings

## Branching Model

- Work is done on the `agent` branch (or `wip` branch per the capture prompt)
- Never commit directly to `main`

## Article Capture Workflow

When adding a new article:

1. Read the source (web page or PDF)
2. Extract metadata and write a summary following the capture format in `prompt/cappy_capture_articles.md`
3. Save to `articles/` with filename pattern: `kebab-case-title-YYYYMMDD.md`
4. Add a link to `README.md` under the correct category heading, at the **top** of that section (most recent first)
5. Identify new AI-specific terms/acronyms not already in the glossary
6. Add new terms to `glossary/definitions-and-acronyms.md` in the correct category table, maintaining alphabetical order

## Article Categories

| Category | Description |
|----------|-------------|
| Strategy & Governance | Business adoption, ROI, responsible AI, policy, regulation |
| Security & Risk | Threats, vulnerabilities, AI safety, cybersecurity |
| Architecture & Operations | Agent patterns, frameworks, orchestration, scaling |
| Tooling & Technology | Developer tools, coding assistants, workflows |
| Technical Fundamentals | LLM internals, sampling, training, model architectures, foundational research |

## Article Format

Each article file follows this exact structure:

```
# [Title]
**Authors:** [Authors]

**Category:** [Category]

**Published:** [Publish Date]

---

## Key Points
- [Up to 5 bullet points, one sentence each]

---

## Summary
[Up to 3 paragraphs]

---
**Captured:** [Capture Date]

**Link:** [URL]

**Key Words:** [Up to 5 semicolon-separated keywords]
```

## Glossary Format

Terms are in markdown tables under category headings (`## Strategy & Governance`, etc.). Each row: `|Term|Definition|`. Definitions are 1-2 sentences plus optional bullet points. Include links to authoritative sources where helpful. Keep alphabetical order within each category.

## Validation Rules

- If metadata can't be determined (authors, publish date), use "UNKNOWN"
- Article filename date suffix uses capture date, not publish date
- Assign exactly one category per article based on primary focus
- Don't add common/general vocabulary to the glossary — only AI-specific terms
