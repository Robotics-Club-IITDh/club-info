---
type: event
name: <% tp.system.prompt("Event name") %>
kind: <% tp.system.prompt("Kind (workshop/competition/meeting/outreach/social)") %>
date: <% tp.system.prompt("Date YYYY-MM-DD") %>
location: "<% tp.system.prompt("Location") %>"
lead: "[[<% tp.system.prompt("Lead member") %>]]"
status: planned
tags: [event]
---
# <% tp.frontmatter.name %>
## Plan
## Outcome
