<!--
Guidance for AI coding agents working in this repository.
Focus: concise, actionable notes tailored to this docs/portfolio repo.
Do not add speculative steps — document only what is discoverable from the repository.
-->

# Copilot instructions — technical-writer-portfolio

Purpose
- This repository is a documentation portfolio (markdown-first, docs-as-code). Your tasks will usually be content edits, small tooling config changes, or adding examples (OpenAPI, Postman) under `samples/` or site pages under `docs/`.

What to read first
- `README.md` — project intent and repo map (single-source summary).

Key locations (source-discoverable)
- `README.md` — high-level architecture and build notes.
- `docs/` — GitHub Pages website content (if present). Edit pages here when changing site content.
- `samples/` — source examples (OpenAPI, Postman, templates). Add small sample files or update examples here.
- `.github/workflows/` — CI checks (lint, link checks) referenced in README; update only if a clear workflow file exists and you verified CI expectations.

Project conventions and patterns
- Markdown-first: prefer clear, accessible Markdown with front-matter where site expects it. Keep pages small and focused (one reader goal per page).
- Docs-as-code: treat docs like code — use small, atomic commits and include explanation for content changes in PR descriptions.
- Samples are canonical examples: preserve formatting and any embedded metadata (OpenAPI YAML, Postman JSON). When adding samples, include a short README or comment explaining the intent and how it maps to docs pages.

Developer workflows (discoverable/assumed)
- Local preview: the README mentions `docs/` (GitHub Pages). If you need to preview locally, prefer using a static site generator that the repo uses — but only add tooling after confirming an existing build config (e.g., `package.json`, `mkdocs.yml`, or similar).
- CI: the README references `.github/workflows/` for quality checks. Before editing workflows, verify a workflow file exists; do not add or change CI unless tests or checks are failing and the change is small and well-justified.

How to propose content/code changes
- For content updates: edit or add markdown under `docs/` or root, write a short commit message (imperative tense), and include a PR description that states the reader problem that the change solves.
- For sample updates: add tests/examples inline in `samples/` and include a note (README or adjacent file) describing how to validate.

Examples from this repo
- Use `README.md` phrasing and structure as the voice/style guide: short sections, bullets for highlights, and a `Repo Map` section.
- If adding API samples, mirror the `samples/` layout (create a clear file name and a one-line header inside the file explaining its purpose).

Rules for AI/code edits
- Keep changes minimal and atomic. Avoid broad refactors; prefer focused edits and ask for clarification when unclear.
- Do not introduce external network calls, secrets, or credentials.
- If you can't find a build or test configuration, add changes conservatively and document how you validated them locally.

When to ask the user
- If a change affects build tooling (adds `package.json`, CI workflows, or generators) — ask before proceeding.
- If the requested content conflicts with the README project intent (e.g., heavy app code vs docs), ask for clarification.

If you update this file
- Merge rather than overwrite: preserve any hand-written notes. Add short changelog bullets above the file when you make updates.

Feedback
- After making changes, ask the repo owner which pages they'd like previewed on GitHub Pages and whether CI edits are desired.
