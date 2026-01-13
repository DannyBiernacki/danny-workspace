# Workspace Setup Guide

## 🚀 Quick Start

### Prerequisites

- Git 2.52.0+
- Node.js 24.12.0+ (for web projects)
- Python 3.14+ (for Python projects)
- GitHub CLI (optional but recommended)

### Initial Setup

1. **Clone workspace** (if from GitHub):

   ```bash
   git clone git@github.com:DannyBiernacki/danny-workspace.git ~/Desktop/Work
   cd ~/Desktop/Work
   ```

2. **Or initialize locally**:

   ```bash
   cd ~/Desktop/Work
   git init
   git add .
   git commit -m "Initial commit: Workspace structure"
   ```

3. **Configure Git**:

   ```bash
   git config user.name "Danny Biernacki"
   git config user.email "dev@danielbiernacki.pl"
   ```

---

## 📁 Directory Structure

```
Work/
├── .global/          # User-level configuration
│   └── CONTEXT.md    # Your profile and preferences
│
├── .cursor/          # Cursor AI configuration
│   └── rules/        # Coding rules (base.mdc, git.mdc)
│
├── .claude/          # Claude Code configuration
│   ├── CLAUDE.md     # Workspace memory
│   ├── skills/       # Reusable skills
│   └── agents/       # Specialized agents
│
├── .antigravity/     # Antigravity configuration
│   ├── rules.md      # Behavior guidelines
│   └── workflows/    # Saved workflows
│
├── docs/             # Documentation
│   ├── SETUP.md      # This file
│   ├── CONVENTIONS.md
│   └── GIT_WORKFLOW.md
│
├── shared/           # Shared code
│   ├── utils/        # Utilities
│   ├── components/   # UI components
│   └── configs/      # Shared configs
│
├── templates/        # Project templates
│   ├── react-app/
│   └── python-project/
│
├── projects/         # 🎯 All your projects
│   └── .gitkeep
│
└── archive/          # Old projects
```

---

## 🎯 Creating New Project

### From Template

```bash
cd ~/Desktop/Work/projects
cp -r ../templates/react-app ./my-new-project
cd my-new-project
npm install
```

### From Scratch

```bash
cd ~/Desktop/Work/projects
mkdir my-project
cd my-project

# Initialize based on type
npm init -y              # Node.js
python -m venv venv      # Python
```

### Update README

Add your project to main `README.md`:

```markdown
## Active Projects
- **my-project** - Description
```

---

## 🤖 AI Assistants

### Cursor

- Opens workspace: `cursor ~/Desktop/Work`
- Automatically loads rules from `.cursor/rules/`
- Use `@` to reference files

### Claude Code

- Reads `.claude/CLAUDE.md` automatically
- Use skills from `.claude/skills/`
- Import context with `@path/to/file`

### Antigravity

- Follows `.antigravity/rules.md`
- Use workflows from `.antigravity/workflows/`
- Trigger with `/workflow-name`

---

## 🔄 Git Workflow

### Daily Work

```bash
# Start
git pull

# Work on feature
git checkout -b feature/my-feature

# Commit
git add .
git commit -m "feat(project): description"

# Push
git push -u origin feature/my-feature

# Create PR
gh pr create
```

### Commit Message Format

```
type(scope): description

feat(projects/website): add contact form
fix(shared/utils): handle edge case
docs: update setup guide
```

---

## 📚 Documentation

### When to Update

- **README.md** - New project, major changes
- **CHANGELOG.md** - Every significant change
- **docs/CONVENTIONS.md** - New patterns or standards
- **.global/CONTEXT.md** - Personal preferences change

### Documentation Standards

- Use Markdown
- Include code examples
- Keep it concise
- Update dates

---

## 🛠️ Maintenance

### Weekly

- Pull latest changes: `git pull`
- Update dependencies: `npm update` / `pip list --outdated`
- Review open PRs

### Monthly

- Archive completed projects
- Update documentation
- Clean up branches: `git cleanup`

---

## 🆘 Troubleshooting

### Git Issues

```bash
# Reset to clean state
git reset --hard HEAD

# Discard local changes
git checkout .

# Update from remote
git fetch --all
git pull
```

### AI Assistant Issues

- Cursor: Reload window (Cmd+R)
- Claude: Clear cache, restart
- Antigravity: Check `.antigravity/rules.md`

---

*Last updated: 2026-01-13*
