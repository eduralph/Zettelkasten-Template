---
title: Workflows
tags:
  - meta
---

# Workflows

How notes flow through the vault.

```
   capture          process            promote
   ─────────►  ──────────────►  ────────────────►
1 - Rough     6 - Zettelkasten   6 - Zettelkasten
   Notes      (status: seedling) (status: evergreen)
```

# 1. Capture (Fleeting Notes)

**Where:** `1 - Rough Notes/`
**When:** Any idea, quote, question, or observation worth keeping. Capture friction must be zero — these aren't supposed to be polished.

**How:**
- Create a note anywhere in `1 - Rough Notes/`.
- Title it something memorable (not perfect — you'll rename later if it survives).
- No template required at this stage.

# 2. Read & Annotate (Source Materials)

**Where:** `2 - Source Materials/Books/` (or other media subfolders)
**Template:** `Book Template` — auto-applied via Templater folder mapping.

**How:**
- Create a new note in the Books folder; Templater prompts for author, year, genre, etc.
- Fill `Description`, `Historical Context`, etc. as you learn about the book.
- During reading, capture passages under **Notable Quotes** and reactions under **Reflections** in the same note.
- When a passage triggers a *new idea of your own*, that's a candidate for a permanent note → see step 3.

# 3. Process to Permanent Notes (Zettelkasten)

**Where:** `6 - Zettelkasten/`
**Template:** `Main Notes` — auto-applied via Templater folder mapping.

**How:**
- Create a new note in the Zettelkasten folder; Templater prompts for status and tags.
- Express **one idea, in your own words**. Atomic.
- Link it to at least one other note in **Connections** — and explain *why* it connects.
- Add the source (book, conversation, etc.) under **Source**.

## Maturity Ladder

Promote notes as they harden:

| Status | Meaning | When to promote |
|---|---|---|
| 🌱 **seedling** | Raw capture, half-formed | When the idea is clearly articulated and connected to at least one other note |
| 🌿 **budding** | In development, taking shape | When it can stand alone — comprehensible without source context |
| 🌳 **evergreen** | Stable, refined | When you'd be comfortable defending it in writing |
| 🗃️ **archived** | Kept for reference, no longer evolving | When the idea is superseded but worth keeping for history |

# 4. Review (Gardening)

**Where:** [[0 - Meta/Garden]]

**Cadence:** Weekly (suggested).

**What to do:**
- **Seedlings**: Develop the most promising. Archive or delete the rest.
- **Stale seedlings (30+ days)**: Force a decision. Promote, archive, or delete.
- **Orphans**: Add at least one connection. If you can't, it might not belong.
- **Budding → Evergreen**: Re-read budding notes — any ready to graduate?

# 5. Index / Map of Content

**Where:** `4 - Indexes/`

**When:** After several evergreen notes cluster around a theme, write a hand-curated index linking them in narrative order. This is the "table of contents" view of your thinking — useful for both writing and finding your way back.
