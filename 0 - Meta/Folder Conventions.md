---
title: Folder Conventions
tags:
  - meta
---

# Folder Conventions

The vault follows a numbered-prefix convention (loosely inspired by [Johnny Decimal](https://johnnydecimal.com/)) to enforce a deliberate sort order and signal each folder's role.

## Numbering Rules

| Prefix | Reserved for |
|---|---|
| **0 -** | Meta — documentation about the vault itself. Sorts first so the control panel is always on top. |
| **1 -** | Inbox / rough capture. The "front door." |
| **2 -** | Source materials being consumed (books, articles, etc.). |
| **3 -** | Reference / glossary (tags, terminology). |
| **4 -** | Maps of content / indexes — hand-curated entry points. |
| **5 -** | Templates. |
| **6 -** | Permanent notes (Zettelkasten). The output of all the work. |

## Naming Rules

- **Folders**: `N - Title Case` (e.g., `2 - Source Materials`). Space-dash-space, title case.
- **Notes**: Free-form, prefer human-readable titles over IDs. Use the filename as the canonical title — the Templater templates pick this up via `tp.file.title`.
- **No leading numbers on notes** (unless they're date-prefixed daily/log notes). Numbering is for folders.
- **Attachments**: stored in the vault root by default. (Revisit if attachment count grows — could move to `0 - Meta/attachments/` or per-folder `_attachments/`.)

## Subfolder Rules

- Subfolders are allowed but should be **flat where possible**. Tags and links scale better than folder hierarchies.
- Current sanctioned subfolders:
  - `2 - Source Materials/Books/`
  - (Add others here as they emerge: `2 - Source Materials/Articles/`, `Podcasts/`, etc.)

## Adding a New Top-Level Folder

Before creating a new top-level folder, ask:
1. Could this be a **tag** instead? (Often yes.)
2. Could it be a **subfolder** of an existing one?
3. If a new top-level folder is genuinely needed, pick the next available number that fits the conceptual ordering. Document it here.
