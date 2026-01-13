# Danny's Workspace

**Monorepo** dla wszystkich projektów z wspólną bazą wiedzy i konfiguracją AI assistants.

---

## 📁 Struktura

```
Work/
├── .global/          # Wspólna konfiguracja (CONTEXT.md)
├── .cursor/          # Cursor AI rules
├── .claude/          # Claude Code memory & skills
├── .antigravity/     # Antigravity workflows
├── docs/             # Dokumentacja
├── shared/           # Współdzielony kod
├── templates/        # Szablony projektów
├── projects/         # 🎯 WSZYSTKIE PROJEKTY
└── archive/          # Zarchiwizowane
```

---

## 🎯 Tech Stack

- **Languages:** TypeScript, Python
- **Frontend:** React 19, Next.js, Tailwind CSS
- **Tools:** Git, GitHub CLI, Delta, Docker
- **AI:** Cursor, Claude Code, Antigravity

---

## 📋 Konwencje

### Commit Messages

```
feat(scope): description
fix(scope): description
docs: description
```

### Code Style

- TypeScript: Strict mode, no `any`
- Python: Type hints, PEP 8
- Formatting: Prettier (2 spaces)

---

## 🚀 Quick Commands

```bash
# Status
git status

# Nowy projekt
cd projects && mkdir my-project

# Commit
git add .
git commit -m "feat: description"
git push
```

---

## 📚 Dokumentacja

- @.global/CONTEXT.md - Profil użytkownika
- @docs/SETUP.md - Setup guide
- @docs/CONVENTIONS.md - Konwencje
- @docs/GIT_WORKFLOW.md - Git workflow

---

## 🤖 AI Context

**Workspace Type:** Monorepo  
**Owner:** Danny Biernacki  
**Purpose:** Long-term multi-project development  
**AI Tools:** Cursor, Claude Code, Antigravity

---

*Utworzono: 2026-01-13*
