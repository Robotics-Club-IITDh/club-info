---
type: checkout
item: "[[<% tp.system.prompt("Item name (exact note title)") %>]]"
quantity: <% tp.system.prompt("Quantity") %>
member: "[[<% tp.system.prompt("Member name") %>]]"
checked-out: <% tp.date.now("YYYY-MM-DD") %>
due: <% tp.system.prompt("Due date YYYY-MM-DD") %>
returned: 
status: out
tags: [checkout]
---
Purpose / project:
