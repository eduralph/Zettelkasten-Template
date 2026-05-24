---
title: Reading List
tags:
  - meta
  - dashboard
---

# 📚 Reading List

All books in [[2 - Source Materials/Books|Source Materials]], grouped by status.

> [!info] Requires Dataview. Books should use the [[5 - Templates/Book Template]] which sets `status` in frontmatter.

---

## 📖 Currently Reading

```dataview
TABLE WITHOUT ID
  file.link AS "Book",
  author AS "Author",
  genre AS "Genre",
  created AS "Started"
FROM "2 - Source Materials/Books"
WHERE status = "reading"
SORT created DESC
```

## 📚 To Read

```dataview
TABLE WITHOUT ID
  file.link AS "Book",
  author AS "Author",
  genre AS "Genre"
FROM "2 - Source Materials/Books"
WHERE status = "to-read"
SORT file.name ASC
```

## ✅ Finished

```dataview
TABLE WITHOUT ID
  file.link AS "Book",
  author AS "Author",
  genre AS "Genre"
FROM "2 - Source Materials/Books"
WHERE status = "finished" OR status = "read"
SORT file.name ASC
```

## 🌐 By Author

```dataview
TABLE WITHOUT ID
  author AS "Author",
  length(rows) AS "Books"
FROM "2 - Source Materials/Books"
WHERE author
GROUP BY author
SORT length(rows) DESC
```

## 📊 By Genre

```dataview
TABLE WITHOUT ID
  genre AS "Genre",
  length(rows) AS "Books"
FROM "2 - Source Materials/Books"
WHERE genre
GROUP BY genre
SORT length(rows) DESC
```

## 🗂️ All Books

```dataview
TABLE WITHOUT ID
  file.link AS "Book",
  author AS "Author",
  status AS "Status",
  genre AS "Genre"
FROM "2 - Source Materials/Books"
SORT file.name ASC
```
