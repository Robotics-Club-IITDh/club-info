---
type: dashboard
title: Inventory Dashboard
tags: [dashboard, inventory]
---
# Inventory

## All components
```dataview
TABLE category, quantity + " " + unit AS qty, location, status
FROM "02-Inventory/Components"
WHERE type = "component"
SORT category ASC, name ASC
```

## All tools
```dataview
TABLE category, location, status, last-maintained
FROM "02-Inventory/Tools"
WHERE type = "tool"
SORT category ASC
```

## Low / out of stock
```dataview
TABLE quantity, min-stock, supplier
FROM "02-Inventory/Components"
WHERE type = "component" AND quantity <= min-stock
SORT quantity ASC
```
