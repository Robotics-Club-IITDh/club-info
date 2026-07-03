---
type: dashboard
title: Purchase Requests Dashboard
tags: [dashboard, finance]
---
# Purchase Requests

## Pending
```dataview
TABLE item, quantity, est-cost, requested-by, project, date
FROM "06-Finance/Purchase-Requests"
WHERE type = "purchase-request" AND status = "pending"
SORT date ASC
```

## Pending spend by status
```dataview
TABLE sum(rows.est-cost) AS "estimated total"
FROM "06-Finance/Purchase-Requests"
WHERE type = "purchase-request"
GROUP BY status
```

## All requests
```dataview
TABLE item, status, est-cost, approved-by
FROM "06-Finance/Purchase-Requests"
WHERE type = "purchase-request"
SORT date DESC
```
