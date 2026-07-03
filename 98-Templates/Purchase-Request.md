---
type: purchase-request
id: PR-<% tp.system.prompt("Next PR number") %>
item: <% tp.system.prompt("Item") %>
quantity: <% tp.system.prompt("Quantity") %>
est-cost: <% tp.system.prompt("Estimated total cost") %>
requested-by: "[[<% tp.system.prompt("Your name") %>]]"
project: 
date: <% tp.date.now("YYYY-MM-DD") %>
status: pending
approved-by: 
tags: [finance, purchase-request]
---
## Justification
## Link / supplier
