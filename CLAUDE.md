# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repository is

`shimizu/shimizu` is a **GitHub special profile repository** — its `README.md` is rendered on
https://github.com/shimizu as the profile page. The repository contains only that README: there is
no source code, no build step, no dependencies, and no test suite. "Deploying" a change means
pushing to `main`; GitHub re-renders the profile immediately.

Because the README *is* the product, edits are content/presentation work, not code changes.

## README structure and conventions

The document is written in Japanese with English section headings, and mixes raw HTML (`<div
align="center">`, `<br>`, `<a id="...">`) with Markdown — GitHub allows this, so keep both.

- **Header/footer banners** come from `capsule-render.vercel.app` query-string APIs. The palette is
  encoded in the `color=` gradient stops (`050816` → `0B4F6C` → `01BAEF`) and reused in the badges
  (`00B4D8` accent, `111827` tech-badge background). Keep new visuals inside that palette.
- **Project tables** are grouped by category — `Geospatial`, `Data & AI`, `Experimental` — each with
  three columns (Project / Description / Stack-or-Category). Descriptions are one short Japanese
  line; Stack values are backtick-wrapped tags. Most entries link to a GitHub Pages demo
  (`https://shimizu.github.io/<repo>/`); use the plain repo URL only when there is no live demo.
- **`Slides`** is a separate section using the same three-column table shape, holding talk decks
  hosted under `https://shimizu.github.io/slides/<deck>/#/`.
- Entries are **bold-linked** (`**[Name](url)**`) for headline projects and plain-linked for the
  rest. There is existing inconsistency here; match the surrounding rows rather than normalizing the
  whole file unless asked.
- **Tech Stack badges** use shields.io `for-the-badge` style with `logo=` slugs from simple-icons.
  Adding a technology means adding a badge under the right sub-heading (Languages & Runtime /
  Visualization & Frontend / Data & Cloud), not editing prose.
- The `Focus` table and the `EXPLORE_MY_WORKS` badge anchor (`#featured-projects`, backed by the
  `<a id="featured-projects">` tag) must stay in sync if headings are renamed.

## Working notes

- All external image/badge URLs are live network calls. After editing, sanity-check any URL you
  constructed (query params, icon slugs) rather than assuming it renders.
- Commit messages in this repo's history are Japanese and terse (e.g. `ポートフォリオ追加`); match
  that style.
