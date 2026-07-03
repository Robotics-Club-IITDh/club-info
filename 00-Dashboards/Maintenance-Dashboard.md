---
type: dashboard
title: Maintenance Dashboard
tags: [dashboard, inventory]
---
# Maintenance

## Due within 14 days
```dataview
TABLE item, date AS "last done", next-due, performed-by
FROM "02-Inventory/Maintenance-Logs"
WHERE type = "maintenance" AND next-due <= date(today) + dur(14 days)
SORT next-due ASC
```

## Full log
```dataview
TABLE item, action, date, performed-by
FROM "02-Inventory/Maintenance-Logs"
WHERE type = "maintenance"
SORT date DESC
```
