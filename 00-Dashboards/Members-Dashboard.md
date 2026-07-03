---
type: dashboard
title: Members Dashboard
tags: [dashboard, members]
---
# Members

## Active roster
```dataview
TABLE role, team, year, join(skills, ", ") AS skills
FROM "04-Members/Roster"
WHERE type = "member" AND active = true
SORT team ASC, name ASC
```

## Headcount by team
```dataview
TABLE length(rows) AS count
FROM "04-Members/Roster"
WHERE type = "member" AND active = true
GROUP BY team
```

## Skill lookup (edit the WHERE to search)
```dataview
LIST
FROM "04-Members/Roster"
WHERE type = "member" AND active = true AND contains(skills, "ros")
```
