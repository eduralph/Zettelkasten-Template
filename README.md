# Zettelkasten Template — An Obsidian Starter Vault

An opinionated [Obsidian](https://obsidian.md) vault for personal knowledge management, Zettelkasten-style note-taking, and long-form writing projects.

A complete starter system: numbered folder hierarchy, Templater-driven note scaffolding, Dataview dashboards for the "garden," interlinked folder READMEs, and a maturity ladder for permanent notes. Use it as the substrate for a "book of insights," a research project, a digital garden, or any reflective writing practice.

## What's Inside

```
your-vault/
├── 0 - Meta/             ← Vault documentation, dashboards, conventions
│   ├── README.md             Vault overview & control panel
│   ├── Folder Conventions.md Naming rules
│   ├── Workflows.md          Capture → process → review rituals
│   ├── Plugin Setup.md       Installed plugins and why
│   ├── Garden.md             Zettelkasten dashboard (Dataview)
│   ├── Reading List.md       Books dashboard (Dataview)
│   ├── Roadmap.md            What's coming next
│   └── Changelog.md          System-change log
├── 1 - Rough Notes/      ← Inbox / fleeting capture
├── 2 - Source Materials/ ← Books, articles, podcasts
│   └── Books/                Auto-templated via Templater
├── 3 - Tags/             ← Tag glossary
├── 4 - Indexes/          ← Hand-curated maps of content
├── 5 - Templates/        ← Templater templates
│   ├── Book Template.md
│   └── Main Notes.md
└── 6 - Zettelkasten/     ← Permanent notes (atomic, linked)
    └── About.md              Project manifesto
```

Every folder has its own `README.md` explaining its purpose, conventions, and links to sibling folders. Start at [0 - Meta/README.md](0%20-%20Meta/README.md).

## Required Plugins

The vault depends on two community plugins. Install them on first use:

1. **[Templater](https://github.com/SilentVoid13/Templater)** — powers auto-populated new notes
2. **[Dataview](https://github.com/blacksmithgu/obsidian-dataview)** — powers the Garden and Reading List dashboards

Configurations for both ship in `.obsidian/plugins/*/data.json` — they'll activate as soon as you install the plugins.

## Using This as a Starter

### Option A — Use this template (recommended if hosted on GitHub)

1. Click **"Use this template"** on the GitHub repo page.
2. Clone the new repo locally.
3. Open the cloned folder in Obsidian: *Open folder as vault*.
4. Install Templater and Dataview from Community Plugins.
5. Reload Obsidian. Templates and dashboards activate automatically.
6. Strip personal content (see below) and start writing.

### Option B — Clone and strip

```bash
git clone <this-repo> my-new-vault
cd my-new-vault
rm -rf .git
git init
```

Then follow steps 3–6 above.

### What's Included as Samples

The starter ships with two sample book notes you can use as references for how to fill out the [[5 - Templates/Book Template|Book Template]]:

- `2 - Source Materials/Books/De vita propria liber.md` (Cardano)
- `2 - Source Materials/Books/Denial of Death.md` (Becker)

Keep, edit, or delete them — they're just examples.

### What's NOT Included

- **`6 - Zettelkasten/About.md`** — the project manifesto is intentionally absent. It's where you state *why* this vault exists for **you**. Create it as your first permanent note:
  ```
  Open Obsidian → click any [[About]] link in the existing READMEs → write your own.
  ```
- All personal content notes from the original vault.

### After Cloning

1. Update `0 - Meta/Changelog.md` — strike a clean line and start your own history.
2. Update `0 - Meta/Roadmap.md` — replace with your goals.
3. Adjust folder READMEs to match how you actually work (treat them as scaffolding, not stone).
4. Write your `About.md`.

The folder READMEs, templates, dashboards, and conventions are all generic and stay as-is.

## Conventions at a Glance

- **Numbered folders** (Johnny-Decimal-ish) — sort order is intentional.
- **Maturity ladder** for Zettelkasten notes: 🌱 seedling → 🌿 budding → 🌳 evergreen → 🗃️ archived.
- **Templates fire automatically** when you create a note in a mapped folder (Templater "folder templates").
- **READMEs are interlinked** — every folder README links to every other.

Full details in [0 - Meta/Folder Conventions.md](0%20-%20Meta/Folder%20Conventions.md) and [0 - Meta/Workflows.md](0%20-%20Meta/Workflows.md).

## What's NOT in the Repo

- Per-user UI state (`workspace.json`, hotkeys, graph layout) — set these to your preference.
- Plugin binaries (`main.js`, etc.) — install fresh from Community Plugins.
- Sync credentials (e.g., LiveSync `data.json`) — configure on your own machine.
- Personal cache, trash, file recovery.

See [`.gitignore`](.gitignore) for the full list.

## License

Licensed under the [Apache License, Version 2.0](LICENSE). Maximally permissive: use it, fork it, adapt it, ship it commercially. The only requirements are attribution and preserving the license notice in derivative works.
