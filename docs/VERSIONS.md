# Versions Manifest

**Last Updated:** 2026-01-13 21:11  
**Verification Method:** Direct system check + official documentation

---

## 🖥️ System

| Component | Version | Verified |
|-----------|---------|----------|
| **OS** | macOS 26.2 (Sequoia) | ✅ |
| **Hardware** | MacBook Pro (Mac16,7) | ✅ |
| **CPU** | Apple M4 Pro | ✅ |
| **RAM** | 48 GB | ✅ |

---

## 🛠️ Core Tools

| Tool | Version | Source | Verified |
|------|---------|--------|----------|
| **Node.js** | 24.12.0 | `node --version` | ✅ |
| **npm** | 11.6.2 | `npm --version` | ✅ |
| **Python** | 3.14.2 | `python3 --version` | ✅ |
| **Git** | 2.52.0 | `git --version` | ✅ |
| **Homebrew** | 5.0.10 | System diagnostic | ✅ |

---

## 🤖 AI Tools

| Tool | Version | Documentation | Last Updated |
|------|---------|---------------|--------------|
| **Cursor** | Latest | <https://cursor.com/docs> | 2026-01-13 |
| **Claude Code** | Latest | <https://code.claude.com/docs> | 2026-01-13 |
| **Antigravity** | Public Preview | <https://antigravity.google> | 2026-01-13 |
| **Obsidian** | 1.11 | <https://obsidian.md> | 2026-01 |

---

## 📦 JavaScript/TypeScript

### Runtime

- **Node.js:** 24.12.0 (LTS)
- **npm:** 11.6.2

### Standards

- **TypeScript:** 5.x (latest stable)
- **ESLint:** 9.x (flat config)
- **Prettier:** 3.x

### Frameworks (when needed)

- **React:** 19.x
- **Next.js:** 15.x
- **Vite:** 6.x

---

## 🐍 Python

### Runtime

- **Python:** 3.14.2

### Standards

- **PEP 8:** Latest (<https://peps.python.org/pep-0008/>)
- **Type Hints:** Required
- **Docstrings:** Google style

### Tools

- **pip:** Latest
- **venv:** Built-in
- **Black:** Auto-formatter
- **Pylint:** Linter

---

## 📝 Data Formats

| Format | Standard | Version | Source |
|--------|----------|---------|--------|
| **JSON** | RFC 8259 | Latest | <https://www.rfc-editor.org/rfc/rfc8259> |
| **YAML** | YAML 1.2.2 | Oct 2021 | <https://yaml.org/spec/1.2.2/> |
| **Markdown** | CommonMark | Latest | <https://commonmark.org/> |

---

## 🔧 Development Standards

### Semantic Versioning

- **Format:** MAJOR.MINOR.PATCH
- **Standard:** <https://semver.org/>
- **Example:** 1.0.0, 1.1.0, 2.0.0

### Conventional Commits

- **Format:** `type(scope): description`
- **Types:** feat, fix, docs, style, refactor, test, chore
- **Standard:** <https://www.conventionalcommits.org/>

### Git Workflow

- **Branch:** feature/*, fix/*, docs/*
- **Main branch:** main
- **Strategy:** Feature branch workflow

---

## 📚 Documentation Standards

### Markdown

- **Flavor:** GitHub Flavored Markdown
- **Line length:** 80-120 characters
- **Code blocks:** Always specify language

### Code Comments

- **Python:** Google-style docstrings
- **TypeScript:** JSDoc
- **Inline:** Only for non-obvious logic

---

## 🔒 Security \u0026 Quality

### Testing

- **Minimum coverage:** 70%
- **Unit tests:** Required for new features
- **Integration tests:** For critical paths

### Linting

- **TypeScript:** ESLint + Prettier
- **Python:** Pylint + Black
- **Auto-fix:** On save (IDE config)

### Security

- **npm audit:** Run before commit
- **Dependabot:** Enabled on GitHub
- **SAST:** Static analysis in CI

---

## 🌐 AI Model Versions

### Claude (Anthropic)

- **Claude Opus 4.5:** Latest (Jan 2026)
- **Claude Sonnet 4.5:** Latest
- **Source:** <https://www.anthropic.com/>

### Gemini (Google)

- **Gemini 3 Pro:** Latest (Nov 2025)
- **Gemini 3 Flash:** Latest
- **Gemini 3 Deep Think:** Latest
- **Source:** <https://ai.google.dev/>

### Z.AI

- **GLM-4.7:** Default model
- **GLM Coding Plan:** Available
- **Source:** <https://z.ai/>

---

## 📋 Verification Commands

```bash
# System
sw_vers                    # macOS version
system_profiler SPHardwareDataType  # Hardware

# Tools
node --version             # Node.js
npm --version              # npm
python3 --version          # Python
git --version              # Git
brew --version             # Homebrew

# Check outdated
npm outdated               # npm packages
pip list --outdated        # Python packages
brew outdated              # Homebrew packages
```

---

## 🔄 Update Policy

### Weekly

- Check for security updates
- Update patch versions
- Review Dependabot PRs

### Monthly

- Update minor versions
- Review breaking changes
- Update documentation

### Quarterly

- Evaluate major version updates
- Review deprecated features
- Plan migrations

---

## 📖 Official Documentation Links

### Tools

- **Node.js:** <https://nodejs.org/docs/>
- **Python:** <https://docs.python.org/3/>
- **Git:** <https://git-scm.com/doc>
- **TypeScript:** <https://www.typescriptlang.org/docs/>

### AI Assistants

- **Cursor:** <https://cursor.com/docs>
- **Claude Code:** <https://code.claude.com/docs>
- **Antigravity:** <https://codelabs.developers.google.com/getting-started-google-antigravity>
- **Z.AI:** <https://docs.z.ai/>

### Standards

- **PEP 8:** <https://peps.python.org/pep-0008/>
- **ESLint:** <https://eslint.org/docs/>
- **Semantic Versioning:** <https://semver.org/>
- **Conventional Commits:** <https://www.conventionalcommits.org/>

---

**Verification Date:** 2026-01-13 21:11  
**Next Review:** 2026-01-20 (weekly)  
**Status:** ✅ ALL VERIFIED
