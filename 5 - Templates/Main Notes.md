<%*
const statusChoice = await tp.system.suggester(
  ["🌱 seedling — raw capture, unformed", "🌿 budding — in development", "🌳 evergreen — refined, stable", "🗃️ archived — kept for reference"],
  ["seedling", "budding", "evergreen", "archived"],
  false,
  "Note maturity"
);
const status = statusChoice ?? "seedling";
const tags = await tp.system.prompt("Tags (space-separated, no # needed)", "");
const tagList = tags.split(/\s+/).filter(Boolean).map(t => "  - " + t).join("\n");
-%>
---
title: <% tp.file.title %>
status: <% status %>
created: <% tp.file.creation_date("YYYY-MM-DD HH:mm") %>
tags:
<% tagList %>
---

# <% tp.file.title %>

<!-- One idea, in your own words. Atomic and self-contained — a future reader (or future you) should grasp it without needing the source. -->



# Connections

<!-- Why does this note connect to other notes? Don't just link — explain the relationship. -->

- [[ ]] — 

# Source

<!-- Where did this idea come from? Book, conversation, your own reflection, etc. -->

