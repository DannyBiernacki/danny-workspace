# Coding Conventions

## General Principles

- **DRY** (Don't Repeat Yourself) - Reuse code from `shared/`
- **KISS** (Keep It Simple, Stupid) - Simple solutions over complex
- **YAGNI** (You Aren't Gonna Need It) - Don't over-engineer
- **Single Responsibility** - One function, one purpose

---

## TypeScript / JavaScript

### Style

```typescript
// ✅ Good
const getUserName = (user: User): string => {
  return user.name;
};

// ❌ Bad
function get_user_name(user: any) {
  return user.name;
}
```

### Rules

- Use `const` and `let`, never `var`
- Prefer arrow functions
- Use TypeScript strict mode
- No `any` type - use `unknown` or specific types
- Destructure when possible

### Naming

- **Variables:** `camelCase`
- **Functions:** `camelCase`
- **Classes:** `PascalCase`
- **Constants:** `UPPER_SNAKE_CASE`
- **Files:** `kebab-case.ts`

---

## Python

### Style

```python
# ✅ Good
def get_user_name(user: User) -> str:
    """Get user's full name."""
    return user.name

# ❌ Bad
def getUserName(user):
    return user.name
```

### Rules

- Follow PEP 8
- Type hints on all functions
- Google-style docstrings
- Use pathlib for paths
- Prefer f-strings over format()

### Naming

- **Variables:** `snake_case`
- **Functions:** `snake_case`
- **Classes:** `PascalCase`
- **Constants:** `UPPER_SNAKE_CASE`
- **Files:** `snake_case.py`

---

## Git Commits

### Format

```
type(scope): description

[optional body]

[optional footer]
```

### Types

- `feat` - New feature
- `fix` - Bug fix
- `docs` - Documentation
- `style` - Formatting
- `refactor` - Code restructuring
- `test` - Tests
- `chore` - Maintenance

### Examples

```
feat(projects/website): add contact form
fix(shared/utils): handle null in parseDate
docs: update CONVENTIONS.md
refactor(projects/app): extract validation logic
```

---

## File Organization

### Project Structure

```
projects/my-project/
├── src/              # Source code
├── tests/            # Tests (mirror src/)
├── docs/             # Project docs
├── .env.example      # Environment template
└── README.md         # Project overview
```

### Imports

```typescript
// ✅ Good - Absolute imports
import { Button } from '@/components/Button';
import { formatDate } from '@/shared/utils/date';

// ❌ Bad - Relative imports
import { Button } from '../../../components/Button';
```

---

## Testing

### Naming

```typescript
describe('ComponentName', () => {
  it('should render with props', () => {
    // test
  });
  
  it('should handle click event', () => {
    // test
  });
});
```

### Coverage

- Minimum 80% coverage
- Test happy path + edge cases + errors
- Mock external dependencies

---

## Documentation

### Code Comments

```typescript
// ✅ Good - Explain WHY
// Using debounce to prevent excessive API calls
const debouncedSearch = debounce(search, 300);

// ❌ Bad - Explain WHAT (obvious)
// Call the search function
search();
```

### README Structure

```markdown
# Project Name

Brief description

## Features
## Installation
## Usage
## Development
## License
```

---

*Last updated: 2026-01-13*
