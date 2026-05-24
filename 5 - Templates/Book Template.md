<%*
const author    = await tp.system.prompt("Author");
const written   = await tp.system.prompt("Year written (optional)", "");
const published = await tp.system.prompt("Year published (optional)", "");
const language  = await tp.system.prompt("Language (optional)", "English");
const genre     = await tp.system.prompt("Genre (optional)", "");
-%>
---
title: <% tp.file.title %>
author: <% author %>
written: <% written %>
published: <% published %>
language: <% language %>
genre: <% genre %>
tags:
  - book
status: to-read
created: <% tp.file.creation_date("YYYY-MM-DD HH:mm") %>
---

Author: <% author %>

# Description

<!-- Brief overview: what the book is about, why it matters, its core thesis or contribution. -->

# Historical Context

<!-- When and where was it written? What was happening in the author's life, field, or world that shaped it? -->

# Structure of the Book

<!-- How is the book organized? Chapters, parts, thematic vs. chronological, etc. -->

# Key Themes

### 1. 

### 2. 

### 3. 

# Why It Matters

<!-- The book's significance — influence, originality, what it changed or anticipated. -->

# Author's Other Major Works

- 

# Related Notes

- 

# Reading Notes

> [!quote] Capture passages, reactions, and thoughts as you read.

## Chapter Notes

<!-- Add notes per chapter or theme as you go -->

## Notable Quotes

<!-- Capture striking passages here -->

## Reflections

<!-- Your own thoughts, connections, questions -->
