---
title: Changelog
tags:
  - meta
---

# Changelog

System-level changes to the vault — structural, template, plugin, or convention changes. Not for content changes (those live in their notes' history).

Newest first.

---

## 2026-05-25

- **Initialized git repository** with Obsidian-tuned `.gitignore` (excludes per-user UI state, plugin binaries, sync credentials, Claudian sessions).
- **Added `README.md`** at vault root as the GitHub repo landing page (project name: **Zettelkasten Template**) — folder structure, plugin requirements, "Use this template" workflow, sample-vs-personal-content guide. Initially named `STARTER-README.md`; renamed so GitHub auto-renders it as the repo landing page.
- **Added Apache 2.0 `LICENSE`** for maximum permissiveness on the public starter.
- **Excluded `6 - Zettelkasten/About.md` from git** — personal manifesto stays local; starter users create their own.
- **Created `0 - Meta/` folder** as the home for vault documentation and dashboards.
- **Authored meta documentation**: [[0 - Meta/README|README]], [[0 - Meta/Folder Conventions|Folder Conventions]], [[0 - Meta/Workflows|Workflows]], [[0 - Meta/Plugin Setup|Plugin Setup]], [[0 - Meta/Roadmap|Roadmap]], this Changelog.
- **Moved Garden dashboard** from `6 - Zettelkasten/About.md` to [[0 - Meta/Garden]]. Restored `About.md` to manifesto-only.
- **Added folder README files** to all six top-level content folders ([[1 - Rough Notes/README|1 - Rough Notes]], [[2 - Source Materials/README|2 - Source Materials]], [[3 - Tags/README|3 - Tags]], [[4 - Indexes/README|4 - Indexes]], [[5 - Templates/README|5 - Templates]], [[6 - Zettelkasten/README|6 - Zettelkasten]]) documenting purpose, conventions, and related notes. Each ends with an interlinked "Other Folders" navigation footer.
- **Deleted** empty stray notes `Untitled.md`, `Untitled 1.md`, and `6 - Zettelkasten/Recipe.md`.

## 2026-05-24

- **Installed and configured Dataview** community plugin.
- **Created Garden dashboard** with 6 views: Seedlings, Budding, Evergreen, Stale Seedlings, Orphans, Census.
- **Installed and configured Templater** community plugin.
  - Template folder: `5 - Templates`
  - Trigger on file creation: ON
  - Folder mappings:
    - `2 - Source Materials/Books` → `Book Template.md`
    - `6 - Zettelkasten` → `Main Notes.md`
- **Configured core Templates plugin** to point at `5 - Templates` with `YYYY-MM-DD` / `HH:mm` formats.
- **Rewrote `Book Template`** to use Templater syntax — prompts for author, year written, year published, language, genre on creation; auto-fills title and created timestamp.
- **Rewrote `Main Notes` template** to use Templater syntax — `tp.system.suggester` dropdown for status (seedling/budding/evergreen/archived), tag prompt, auto-fills title and created timestamp.
- **Expanded book note** `2 - Source Materials/Books/De vita propria liber.md` with full frontmatter, historical context, key themes, related works, and reading-notes scaffolding.

---

# Convention

Each entry: date heading + bullet list. Keep entries short — link to the affected files for details.
