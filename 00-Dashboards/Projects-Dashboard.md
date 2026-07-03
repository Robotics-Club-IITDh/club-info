---
type: dashboard
title: Projects Dashboard
tags: [dashboard, projects]
---
# Projects

## Active
```dataview
TABLE lead, deadline, budget-allocated AS budget, length(members) AS team
FROM "03-Projects"
WHERE type = "project" AND status = "active"
SORT deadline ASC
```

## All by status
```dataview
TABLE status, lead, deadline
FROM "03-Projects"
WHERE type = "project"
SORT status ASC, deadline ASC
```
