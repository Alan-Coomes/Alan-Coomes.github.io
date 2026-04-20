# CLAUDE.md

Project guidance for Claude Code when working in this repository.

## Project

Personal portfolio website for **Alan Coomes**.

- **Hosting:** GitHub Pages (repo named `Alan-Coomes.github.io`)
- **Custom domain:** `alancoomes.com` (see `CNAME`)
- **Stack:** Single static `index.html` — no build step, no framework, no package manager
- **Deploy:** Push to the default branch; GitHub Pages serves the HTML directly

## Repository layout

```
index.html   # entire site: HTML + inline <style> + content
CNAME        # custom domain for GitHub Pages
README.md    # one-line project description
```

That is the whole site. There is no `src/`, no build output, no JS bundler.

## Working conventions

- **Edit `index.html` directly.** All CSS lives inside the `<style>` block in `<head>`; all content lives in the `<body>`. Keep it that way unless asked to split files.
- **No dependencies.** Fonts load from Google Fonts via `<link>`. Do not introduce npm, bundlers, frameworks, or build tooling without explicit request.
- **Design tokens** are CSS custom properties on `:root` (`--navy`, `--teal`, `--cream`, `--text`, etc.). Reuse them — do not hardcode colors.
- **Typography:** DM Serif Display (headings), DM Mono (eyebrows/tags), Figtree (body).
- **Sections** follow a numbered pattern (`01 / experience`, `02 / education`, ...). Keep numbering sequential when adding sections.
- **Responsive:** There is one `@media (max-width: 640px)` breakpoint at the bottom of the stylesheet. Add mobile rules there.

## Verifying changes

- Open `index.html` in a browser (or `python3 -m http.server` from the repo root) to preview.
- Smoke-check: hero renders, nav anchors scroll to sections, mobile layout collapses grids to one column.

## What not to do

- Do not create a README rewrite, package.json, or framework scaffolding unless asked.
- Do not change the custom domain in `CNAME`.
- Do not add tracking scripts, analytics, or third-party embeds without approval.
- Do not commit unless the user explicitly asks.
