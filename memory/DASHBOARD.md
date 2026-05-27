---
type: dashboard
---
# Earned Media Dashboard

## Outbox — Ready to Review
```dataview
TABLE file.mtime AS "Written", file.name AS "Item"
FROM "walter-code/outbox"
SORT file.mtime DESC
LIMIT 10
```

## Recent Placements
```dataview
TABLE outlet AS "Outlet", angle_name AS "Angle", date AS "Date"
FROM "walter-code"
WHERE type = "placement"
SORT date DESC
LIMIT 8
```

## Reports
```dataview
TABLE file.mtime AS "Date", file.name AS "Report"
FROM "walter-code/reports"
SORT file.mtime DESC
LIMIT 5
```

---
*Earned Media Skills by 701am*
