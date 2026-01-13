# 📥 Inbox

Quick capture area for ideas, links, and temporary notes.

## Process

1. Capture quickly here
2. Review daily
3. Move to appropriate folder
4. Archive or delete

---

## Recent Captures

```dataview
TABLE file.ctime as "Captured"
FROM "00-Inbox"
WHERE file.name != "Inbox"
SORT file.ctime DESC
```
