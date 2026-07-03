---
type: member
name: <% tp.system.prompt("Full name") %>
roll: 
role: member
team: <% tp.system.prompt("Team (mechanical/electronics/software/management)") %>
year: <% tp.system.prompt("Year of study") %>
skills: []
email: 
joined: <% tp.date.now("YYYY-MM-DD") %>
active: true
tags: [member]
---
# <% tp.frontmatter.name %>
