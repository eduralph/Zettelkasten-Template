---
title: README
tags:
  - meta
---

# 5 - Templates

**Templater templates.** Scaffolds for new notes. Most fire automatically when a note is created in a mapped folder.

## Templates

| Template | Used by | Trigger |
|---|---|---|
| [[5 - Templates/Book Template]] | Books in `2 - Source Materials/Books/` | Auto (Templater folder mapping) |
| [[5 - Templates/Main Notes]] | Permanent notes in `6 - Zettelkasten/` | Auto (Templater folder mapping) |

## Configuration

Templater is configured to scan this folder. Folder mappings, trigger settings, and other config live in [[0 - Meta/Plugin Setup#Templater Configuration|Plugin Setup]] (source of truth: `.obsidian/plugins/templater-obsidian/data.json`).

## Conventions

- **Templater syntax**: use `<% tp.* %>` for inline expressions and `<%* ... -%>` blocks for setup logic (e.g., prompting for values). The `-%>` suffix suppresses the trailing newline so frontmatter doesn't get a blank line at the top.
- **Filename = template name** as it appears in the Templater picker. Keep them short and unambiguous.
- **Prompt sparingly**: every prompt adds friction at the moment of capture. Only prompt for things that are hard to fill in later or that genuinely vary per note.
- **Provide sensible defaults**: `tp.system.prompt("Language", "English")` accepts Enter for the default.
- **Cursor placement**: use `<% tp.file.cursor() %>` to position the cursor where editing starts after creation.

## Adding a New Template

1. Create the file here.
2. If it should auto-apply to a folder, add a mapping in Templater settings (see [[0 - Meta/Plugin Setup]]).
3. Document it in the table above and update [[0 - Meta/Changelog]].

---

## Other Folders

- [[0 - Meta/README|0 - Meta]] — Vault documentation, dashboards, conventions
- [[1 - Rough Notes/README|1 - Rough Notes]] — Inbox / fleeting capture
- [[2 - Source Materials/README|2 - Source Materials]] — Books, articles, podcasts
- [[3 - Tags/README|3 - Tags]] — Tag glossary
- [[4 - Indexes/README|4 - Indexes]] — Maps of content
- [[6 - Zettelkasten/README|6 - Zettelkasten]] — Permanent notes
