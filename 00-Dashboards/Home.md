---
type: dashboard
title: Home
tags: [dashboard]
---
# Club Control Panel

## Jump to
- [[Inventory-Dashboard]]
- [[Checkouts-Dashboard]]
- [[Projects-Dashboard]]
- [[Members-Dashboard]]
- [[Purchase-Requests-Dashboard]]
- [[Maintenance-Dashboard]]

## Needs attention now
### Overdue checkouts
```dataview
TABLE item, member, due
FROM "02-Inventory/Checkouts"
WHERE status != "returned" AND due < date(today)
SORT due ASC
```
### Low stock
```dataview
TABLE quantity, "min: " + min-stock AS threshold, location
FROM "02-Inventory/Components"
WHERE type = "component" AND quantity <= min-stock
SORT quantity ASC
```
### Pending purchase requests
```dataview
TABLE item, quantity, est-cost, requested-by
FROM "06-Finance/Purchase-Requests"
WHERE type = "purchase-request" AND status = "pending"
SORT date ASC
```
