---
date: <% tp.date.now("YYYY-MM-DD") %>
day: <% tp.date.now("dddd") %>
tags: [daily]
---

# <% tp.date.now("YYYY-MM-DD") %> - <% tp.date.now("dddd") %>

## 🎯 Today's Focus

- [ ]
- [ ]
- [ ]

## 📝 Notes

## 💡 Ideas

## 🔗 Navigation

- [[<% tp.date.now("YYYY-MM-DD", -1) %>|← Yesterday]]
- [[Home|🏠 Home]]
- [[<% tp.date.now("YYYY-MM-DD", 1) %>|Tomorrow →]]

---

## 📊 Tasks

```dataview
TASK
WHERE !completed
AND file.name = this.file.name
```
