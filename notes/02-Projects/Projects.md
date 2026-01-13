# 📊 Projects

Active and archived projects.

---

## Active Projects

```dataview
TABLE status, created
FROM "02-Projects"
WHERE status != "archived" AND file.name != "Projects"
SORT created DESC
```

---

## Archived Projects

```dataview
TABLE status, created
FROM "02-Projects"
WHERE status = "archived"
SORT created DESC
```
