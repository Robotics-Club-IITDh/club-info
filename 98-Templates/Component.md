---
type: component
id: COMP-<% tp.system.prompt("Next component number, e.g. 0001") %>
name: <% tp.system.prompt("Component name") %>
category: <% tp.system.prompt("Category (microcontroller/sensor/motor/passive/...)") %>
quantity: <% tp.system.prompt("Quantity") %>
unit: pcs
location: "<% tp.system.prompt("Storage location") %>"
status: available
min-stock: <% tp.system.prompt("Minimum Stock") %>
unit-cost: 
supplier: 
datasheet: 
tags: [inventory, component]
---
# <% tp.frontmatter.name %>
Notes / specs:
