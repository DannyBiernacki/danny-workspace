# AI Coding Assistants - Rules \u0026 Best Practices

**Data weryfikacji:** 2026-01-13  
**Źródła:** Oficjalne dokumentacje (cursor.com, code.claude.com, antigravity.google, docs.z.ai)

---

## 🎯 Fundamentalna Zasada

> **ZAWSZE WERYFIKUJ AI KOD PRZED COMMITEM**

**Dane z 2026:**

- AI kod ma **1.7x więcej bugów** niż kod ludzki
- **76% developerów nie ufa** AI kodowi
- **48% nie weryfikuje** przed commitem
- **40-50% AI kodu** ma security flaws

**Źródło:** byteiota.com, addyosmani.com (2026)

---

## 1. Cursor IDE

**Oficjalna dokumentacja:** <https://cursor.com/docs/context/rules>

### Rules (`.cursor/rules/*.mdc`)

**Best Practices (oficjalne):**

- ✅ **Focused rules** - jedna reguła = jeden cel
- ✅ **Under 500 lines** - max długość reguły
- ✅ **Composable** - reużywalne bloki
- ✅ **Concrete names** - opisowe nazwy

**Lokalizacje:**

- `.cursor/rules/` - Project rules (commitowane do Git)
- User Rules - globalne (Settings → Cursor Settings → Rules)
- Team Rules - dla zespołu

**Precedencja:**

1. Local (manual)
2. Auto-attached
3. Agent-requested
4. Always-applied (user rules)

### Bezpieczeństwo

**KRYTYCZNE (backslash.security):**

- ❌ **NIGDY auto-run** bez review
- ✅ Enable file deletion protection
- ✅ Enable dotfile protection
- ✅ Aggressive version control (Git)
- ✅ Sandboxed environments
- ✅ Secrets w vault (nie w plikach)

---

## 2. Claude Code

**Oficjalna dokumentacja:** <https://code.claude.com/docs/en/overview>  
**Best Practices:** <https://www.anthropic.com/engineering/claude-code-best-practices>

### CLAUDE.md Files

**Oficjalne zalecenia:**

- ✅ **Root repo:** `CLAUDE.md` (commituj do Git)
- ✅ **Local:** `CLAUDE.local.md` (.gitignore)
- ✅ **Monorepo:** `root/CLAUDE.md` + `root/foo/CLAUDE.md`
- ✅ **Home:** `~/.claude/CLAUDE.md` (globalne)

**Co umieścić:**

```markdown
# Bash commands
- npm run build: Build the project
- npm run typecheck: Run typechecker

# Code style
- Use ES modules (import/export), not CommonJS
- Destructure imports when possible

# Workflow
- Typecheck when done with code changes
- Run single tests, not whole suite
```

### Workflow (oficjalny)

**Explore → Plan → Code → Commit:**

1. `/init` - generuje CLAUDE.md
2. `#` key - dodaj instrukcję do CLAUDE.md
3. Iteruj z Claude
4. Commit changes

**Multi-Claude (advanced):**

- Claude 1: pisze kod
- Claude 2: weryfikuje kod
- Git worktrees dla izolacji

### Tuning CLAUDE.md

**Oficjalne wskazówki:**

- ✅ Użyj [prompt improver](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/prompt-improver)
- ✅ Dodaj emphasis: "IMPORTANT", "YOU MUST"
- ✅ Iteruj - testuj effectiveness
- ✅ `/clear` - keep context focused

---

## 3. Google Antigravity

**Oficjalna dokumentacja:** <https://codelabs.developers.google.com/getting-started-google-antigravity>  
**Last updated:** 2026-01-13

### Rules \u0026 Workflows

**Lokalizacje:**

- **Global rule:** `~/.gemini/GEMINI.md`
- **Global workflow:** `~/.gemini/antigravity/global_workflows/`
- **Workspace rules:** `your-workspace/.agent/rules/`
- **Workspace workflows:** `your-workspace/.agent/workflows/`

**Rules vs Workflows:**

- **Rules** = System instructions (zawsze aktywne)
- **Workflows** = Saved prompts (trigger: `/`)

**Przykład Rule (PEP 8):**

```markdown
* Make sure all code is styled with PEP 8
* Make sure all code is properly commented
```

**Przykład Rule (Code Generation):**

```markdown
* main.py is entry point
* Generate functionality in separate files (feature_x.py)
* Generate examples in main.py (example_feature_x)
```

### Artifacts System

**Oficjalne typy:**

- ✅ **Task list** - checklist zadań
- ✅ **Implementation plan** - plan zmian
- ✅ **Walkthrough** - podsumowanie + screenshots/recordings
- ✅ **Code changes** - diff view

**Workflow:**

1. Agent generuje kod
2. Review changes (Accept all / Reject all / Review)
3. Komentuj w code review
4. Agent iteruje
5. Walkthrough z weryfikacją (browser recording)

### Security

**Allow/Deny Lists:**

- Configure allowed commands
- Test before production
- Browser security settings

---

## 4. Z.AI Integration

**Oficjalna dokumentacja:** <https://docs.z.ai/devpack/tool/claude>

### Claude Code + GLM Models

**Setup:**

```json
// ~/.claude/settings.json
{
  "env": {
    "ANTHROPIC_AUTH_TOKEN": "your_zai_api_key",
    "ANTHROPIC_BASE_URL": "https://api.z.ai/api/anthropic",
    "API_TIMEOUT_MS": "3000000"
  }
}
```

**Models:**

- GLM-4.7 (default dla użytkowników przed 22.12.2025)
- GLM Coding Plan

**Tools:**

- `npx zai-cli search` - wyszukiwanie w dokumentacjach
- `npx zai-cli read` - czytanie URL
- `npx @z_ai/coding-helper` - automated setup

---

## 🔒 Uniwersalne Zasady Bezpieczeństwa

### Mandatory Verification

**ZAWSZE:**

1. ✅ Review AI code przed commitem
2. ✅ Run tests (minimum 70% coverage)
3. ✅ Static analysis (ESLint, Pylint)
4. ✅ Security scan
5. ✅ Manual code review

### Trust-Verification Gap

**Statystyki 2026:**

- 76% developerów nie ufa AI kodowi
- 48% nie weryfikuje przed commitem
- 1.7x więcej bugów w AI kodzie
- 40-50% incydentów security

**Źródło:** byteiota.com, getpanto.ai

### Workflow Weryfikacji

```bash
# 1. AI generuje kod
cursor/claude/antigravity generate

# 2. Review
git diff

# 3. Test
npm test  # lub pytest

# 4. Lint
npm run lint  # lub pylint

# 5. Security
npm audit  # lub safety check

# 6. Commit
git commit -m "feat: AI-generated feature (verified)"
```

---

## 📊 Best Practices Summary

### DO ✅

- **Cursor:** Use `.mdc` rules, keep under 500 lines
- **Claude:** Create `CLAUDE.md`, use `#` key, iterate
- **Antigravity:** Use Rules + Workflows, review artifacts
- **All:** ALWAYS verify AI code, run tests, security scan

### DON'T ❌

- **NEVER** auto-run AI commands bez review
- **NEVER** commit AI code bez testów
- **NEVER** trust AI kod blindly
- **NEVER** skip security scan
- **NEVER** ignore lint errors

---

## 🔗 Oficjalne Źródła

- **Cursor:** <https://cursor.com/docs/context/rules>
- **Claude Code:** <https://code.claude.com/docs/en/overview>
- **Claude Best Practices:** <https://www.anthropic.com/engineering/claude-code-best-practices>
- **Antigravity:** <https://codelabs.developers.google.com/getting-started-google-antigravity>
- **Z.AI:** <https://docs.z.ai/devpack/tool/claude>

---

**Ostatnia weryfikacja:** 2026-01-13 21:11  
**Metoda:** zai-cli search + official docs read  
**Status:** ✅ ZWERYFIKOWANE U ŹRÓDŁA
