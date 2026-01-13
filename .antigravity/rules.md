# Antigravity Workspace Rules

## Workspace Context

This is a **monorepo workspace** containing multiple projects with shared:

- Configuration (`.global/`, `.cursor/`, `.claude/`)
- Documentation (`docs/`)
- Code and utilities (`shared/`)
- Templates (`templates/`)

All projects live in `projects/` directory.

---

## Behavior Guidelines

### Understanding Context

- Always check which project you're working in
- Read `@.global/CONTEXT.md` for user preferences
- Check `@README.md` for workspace overview
- Use `@docs/` for detailed documentation

### Code Quality

- Follow conventions in `@docs/CONVENTIONS.md`
- Use shared utilities from `shared/` when applicable
- Write tests for new features
- Keep code modular and reusable

### Communication

- Language: Polish preferred, English when needed
- Be concise but complete
- Explain reasoning, not just solutions
- Ask clarifying questions when ambiguous

### Git Workflow

- Follow Conventional Commits (see `.cursor/rules/git.mdc`)
- Commit often, push daily
- Keep commits atomic
- Write descriptive messages

---

## Project Management

### New Project

1. Create in `projects/[name]/`
2. Use template from `templates/` if applicable
3. Add to README.md project list
4. Initialize with proper .gitignore

### Shared Code

- Add reusable code to `shared/`
- Document in `shared/README.md`
- Import in projects as needed

### Documentation

- Update `docs/` when adding patterns
- Keep README.md current
- Document decisions in CHANGELOG.md

---

## AI Assistant Coordination

### Cursor

- Uses rules from `.cursor/rules/`
- Automatically applies to all projects

### Claude Code

- Memory in `.claude/CLAUDE.md`
- Skills in `.claude/skills/`
- Agents in `.claude/agents/`

### Antigravity (You!)

- Workflows in `.antigravity/workflows/`
- Follow these rules
- Coordinate with other AI tools

---

*Last updated: 2026-01-13*
