# Repository Guidelines

## Project Structure & Module Organization
This repository currently contains a single source document: `白塞病（Behçet）难治型病例完整分析与就医策略.md`. Keep all primary content in Markdown at the repository root unless the project grows.

If you add supporting material, use a simple layout:
- `docs/` for additional long-form references or drafts
- `assets/` for images, charts, or exported figures linked from Markdown
- `templates/` for reusable document skeletons

Use descriptive file names that mix Chinese titles with English medical terms only when that improves clarity, as in the existing document.

## Build, Test, and Development Commands
There is no build system in this repository today. Use lightweight Markdown checks before submitting changes:

```sh
ls
markdownlint '**/*.md'
open '白塞病（Behçet）难治型病例完整分析与就医策略.md'
```

- `markdownlint '**/*.md'`: checks heading, spacing, and list consistency
- `open ...`: previews the document locally on macOS

If `markdownlint` is not installed, run it through your preferred Node toolchain or editor integration.

## Coding Style & Naming Conventions
Write in clear, professional Markdown with short sections, informative headings, and compact bullet lists. Prefer:
- ATX headings (`#`, `##`, `###`)
- Sentence-style explanatory text under each heading
- Tables only when they improve scanability

Preserve medical terminology accuracy. Keep punctuation and list formatting consistent within each section. When renaming files, avoid vague names like `notes.md`; prefer specific titles tied to the topic.

## Testing Guidelines
Testing in this repository means document validation and review:
- Run `markdownlint '**/*.md'` before opening a PR
- Verify links, table rendering, and heading order in a Markdown preview
- Re-read medical claims for wording precision and unsupported certainty

For new documents, match the title and file name to the subject matter.

## Commit & Pull Request Guidelines
This checkout does not include `.git` history, so no repository-specific commit pattern can be confirmed. Use concise, imperative commit messages such as `Refine treatment strategy summary` or `Add supporting references`.

Pull requests should include:
- A short summary of the content change
- Any medical or editorial assumptions made
- Screenshots only if formatting, tables, or embedded assets changed
