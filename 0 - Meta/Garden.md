---
title: Garden
tags:
  - meta
  - dashboard
---

# 🌱 The Garden

A living dashboard for the [[About|Zettelkasten]]. Surfaces notes that need attention, celebrates what's mature, and keeps the garden from choking on weeds.

> [!info] Requires the [Dataview](https://github.com/blacksmithgu/obsidian-dataview) community plugin.
> Settings → Community plugins → Browse → "Dataview" → Install & Enable.

---

## 🌱 Seedlings — fresh, unformed thoughts
*Raw captures waiting to be developed. Promote them as ideas mature.*

```dataview
TABLE WITHOUT ID
  file.link AS "Note",
  created AS "Captured",
  file.tags AS "Tags"
FROM "6 - Zettelkasten"
WHERE status = "seedling"
SORT created DESC
```

## 🌿 Budding — ideas in development
*These are taking shape. Refine, link, and promote when stable.*

```dataview
TABLE WITHOUT ID
  file.link AS "Note",
  created AS "Captured",
  length(file.outlinks) AS "Connections"
FROM "6 - Zettelkasten"
WHERE status = "budding"
SORT created DESC
```

## 🌳 Evergreen — stable notes
*Mature thoughts. The trunk of the garden.*

```dataview
LIST
FROM "6 - Zettelkasten"
WHERE status = "evergreen"
SORT file.name ASC
```

## 📉 Stale seedlings — over 30 days old, still unformed
*Either develop, archive, or delete. Don't let the garden choke on weeds.*

```dataview
TABLE WITHOUT ID
  file.link AS "Note",
  (date(today) - date(created)).days AS "Days idle"
FROM "6 - Zettelkasten"
WHERE status = "seedling"
  AND date(today) - date(created) > dur(30 days)
SORT created ASC
```

## 🔗 Orphans — notes with no outgoing links
*A note with no connections is a card lost in the slip box. Link it or let it go.*

```dataview
LIST
FROM "6 - Zettelkasten"
WHERE length(file.outlinks) = 0
  AND file.name != "About"
SORT file.ctime DESC
```

## 📊 Garden census

```dataview
TABLE WITHOUT ID
  status AS "Maturity",
  length(rows) AS "Count"
FROM "6 - Zettelkasten"
WHERE status
GROUP BY status
SORT status ASC
```
