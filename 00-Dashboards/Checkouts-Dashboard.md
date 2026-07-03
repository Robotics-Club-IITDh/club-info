---
type: dashboard
title: Checkouts Dashboard
tags: [dashboard, inventory]
---
# Checkouts

## Currently out
```dataview
TABLE item, quantity, member, checked-out, due, status
FROM "02-Inventory/Checkouts"
WHERE status != "returned"
SORT due ASC
```

## Overdue
```dataview
TABLE item, member, due
FROM "02-Inventory/Checkouts"
WHERE status != "returned" AND due < date(today)
SORT due ASC
```

## Returned (history)
```dataview
TABLE item, member, returned
FROM "02-Inventory/Checkouts"
WHERE status = "returned"
SORT returned DESC
LIMIT 50
```
