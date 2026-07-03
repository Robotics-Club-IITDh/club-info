---
type: maintenance
item: "[[<% tp.system.prompt("Tool/equipment name") %>]]"
date: <% tp.date.now("YYYY-MM-DD") %>
action: "<% tp.system.prompt("What was done") %>"
performed-by: "[[<% tp.system.prompt("Your name") %>]]"
next-due: <% tp.system.prompt("Next check date YYYY-MM-DD") %>
tags: [maintenance]
---
