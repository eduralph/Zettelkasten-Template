---
title: Plugin Setup
tags:
  - meta
---

# Plugin Setup

What's installed, what it does, and why I keep it. Useful for vault migrations, new devices, or sanity checks.

# Core Plugins (enabled)

| Plugin | Why |
|---|---|
| File Explorer, Switcher, Search, Backlinks, Outgoing Links, Tag Pane, Graph, Outline | Standard navigation. |
| **Templates** | Configured to point at `5 - Templates`. Date `YYYY-MM-DD`, time `HH:mm`. Mostly superseded by Templater but kept enabled as a fallback. |
| **Daily Notes** | Enabled (configure as needed). |
| **Properties** | Frontmatter UI — used heavily by the Book and Main Notes templates. |
| **Canvas** | Enabled for visual brainstorming. |
| **Bases** | Native database views — enabled as an alternative to Dataview if ever needed. |
| **Sync** | Official Obsidian Sync (also using LiveSync below — pick one). |

# Community Plugins

| Plugin | Purpose |
|---|---|
| **[Templater](https://github.com/SilentVoid13/Templater)** | Powers all template auto-population. Folder mappings: `2 - Source Materials/Books` → `Book Template.md`, `6 - Zettelkasten` → `Main Notes.md`. `trigger_on_file_creation: true`. |
| **[Dataview](https://github.com/blacksmithgu/obsidian-dataview)** | Powers all dashboards ([[0 - Meta/Garden\|Garden]], [[0 - Meta/Reading List\|Reading List]]). |
| **[Excalidraw](https://github.com/zsviczian/obsidian-excalidraw-plugin)** | Hand-drawn diagrams for visual notes. |
| **[Editing Toolbar](https://github.com/PKM-er/obsidian-editing-toolbar)** | Floating formatting toolbar for faster Markdown editing. |
| **[Self-hosted LiveSync](https://github.com/vrtmrz/obsidian-livesync)** | Real-time sync via self-hosted CouchDB. (Overlaps with official Sync — decide which is canonical.) |
| **Realclaudian** | Claude AI assistant inside the vault. |

# Decisions to Revisit

- **Sync conflict**: Both official Obsidian Sync and LiveSync are enabled. Running both can cause edit collisions. Pick one as canonical and disable the other.
- **Bases vs Dataview**: Bases is native and GUI-driven; Dataview is more flexible. Currently using Dataview for dashboards — fine to keep both enabled, but choose one as the convention going forward.

# Templater Configuration

- **Template folder:** `5 - Templates`
- **Trigger on file creation:** ON (templates run automatically when a file is created in a mapped folder)
- **Folder Templates:**
  - `2 - Source Materials/Books` → `Book Template.md`
  - `6 - Zettelkasten` → `Main Notes.md`
- **System commands:** disabled (no shell access from templates)

Stored in `.obsidian/plugins/templater-obsidian/data.json`.
