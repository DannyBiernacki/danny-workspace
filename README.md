# Danny's Workspace 🚀

**Monorepo workspace** dla wszystkich projektów z wspólną bazą wiedzy i konfiguracją AI.

---

## 📁 Struktura

```
Work/
├── .global/          # Wspólna konfiguracja dla wszystkich projektów
├── .cursor/          # Konfiguracja Cursor AI
├── .claude/          # Konfiguracja Claude Code
├── .antigravity/     # Konfiguracja Antigravity
├── docs/             # Wspólna dokumentacja
├── shared/           # Współdzielony kod i narzędzia
├── templates/        # Szablony nowych projektów
├── projects/         # 🎯 Wszystkie projekty tutaj
└── archive/          # Zarchiwizowane projekty
```

---

## 🎯 Aktywne Projekty

*Lista będzie aktualizowana wraz z dodawaniem projektów*

---

## 🚀 Quick Start

### Nowy Projekt

```bash
# Utwórz nowy projekt z szablonu
cd ~/Desktop/Work/projects
mkdir my-new-project
cd my-new-project

# Lub użyj szablonu
cp -r ../templates/react-app ./my-project
```

### Git Workflow

```bash
# Status
git status

# Commit
git add .
git commit -m "feat: opis zmiany"

# Push
git push
```

---

## 🤖 AI Assistants

### Cursor

- Konfiguracja: `.cursor/rules/`
- Automatycznie ładuje reguły dla workspace

### Claude Code

- Pamięć: `.claude/CLAUDE.md`
- Skills: `.claude/skills/`
- Agents: `.claude/agents/`

### Antigravity

- Workflows: `.antigravity/workflows/`
- Reguły: `.antigravity/rules.md`

---

## 📚 Dokumentacja

- [Setup Guide](docs/SETUP.md) - Jak zacząć
- [Conventions](docs/CONVENTIONS.md) - Konwencje kodowania
- [Git Workflow](docs/GIT_WORKFLOW.md) - Workflow Git
- [AI Guide](docs/AI_GUIDE.md) - Praca z AI

---

## 🛠️ Tech Stack

- **Git:** 2.52.0
- **Node.js:** 24.12.0
- **Python:** 3.14.2
- **GitHub CLI:** 2.83.2

---

**Utworzono:** 13 stycznia 2026  
**Właściciel:** Danny Biernacki (@DannyBiernacki)
