# 🏠 Danny's Knowledge Base

**Last updated:** 2026-01-13

---

## 🎯 Quick Links

- [[01-Daily/2026-01-13|Today's Note]]
- [[00-Inbox/Inbox|Inbox]]
- [[02-Projects/Projects|Projects]]

---

## 📊 Active Projects

```dataview
TABLE status, created
FROM "02-Projects"
WHERE status != "archived"
SORT created DESC
LIMIT 10
```

---

## ✅ Today's Tasks

```dataview
TASK
WHERE !completed
AND contains(file.folder, "01-Daily")
LIMIT 10
```

---

## 📝 Recent Notes

```dataview
TABLE file.mtime as "Modified"
FROM ""
WHERE file.name != "Home"
SORT file.mtime DESC
LIMIT 10
```

---

## 🏷️ Popular Tags

```dataview
TABLE length(rows) as Count
FROM ""
FLATTEN file.tags as tag
GROUP BY tag
SORT length(rows) DESC
LIMIT 15
```

---

## 📚 Resources

- [[03-Areas/Development/Development|Development]]
- [[03-Areas/AI/AI|AI & Machine Learning]]
- [[03-Areas/Learning/Learning|Learning]]

---

*Vault created: 2026-01-13*
