---
type: tool
id: TOOL-<% tp.system.prompt("Next tool number") %>
name: <% tp.system.prompt("Tool name") %>
category: <% tp.system.prompt("Category (soldering/power/measurement/...)") %>
location: "<% tp.system.prompt("Storage location") %>"
status: available
last-maintained: <% tp.date.now("YYYY-MM-DD") %>
tags: [inventory, tool]
---
# <% tp.frontmatter.name %>
Usage notes / safety:
