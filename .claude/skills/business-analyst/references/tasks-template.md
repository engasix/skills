# TASKS.md Template

Use this template when generating the module-wise task list. Adapt modules based on project type.

---

```markdown
# {PROJECT_NAME} - Task List

## Overview

Total modules: {N}
Estimated complexity: {S/M/L}

**Legend:**
- [ ] Not started
- [x] Completed
- Size: S (< 2hrs) | M (2-8hrs) | L (> 8hrs)

---

## Module 1: Project Setup & Configuration

Foundation tasks that everything else depends on.

### Tasks

- [ ] **Initialize project** [S]
  - Run `{init command}`
  - Configure `{package.json/pyproject.toml}`
  - Set up `.gitignore`
  - *Acceptance: Project runs with hello world*

- [ ] **Configure TypeScript/Language** [S]
  - Set up `{config file}`
  - Configure path aliases
  - Set strict mode
  - *Acceptance: Type checking passes*

- [ ] **Set up linting & formatting** [S]
  - Install ESLint/Ruff/Prettier
  - Configure rules in `{config}`
  - Add pre-commit hooks
  - *Acceptance: `lint` and `format` commands work*

- [ ] **Configure testing framework** [M]
  - Install {test framework}
  - Set up test config
  - Add example test
  - *Acceptance: `test` command runs successfully*

- [ ] **Set up CI/CD** [M]
  - Create GitHub Actions workflow
  - Add lint, test, build steps
  - Configure deployment (optional)
  - *Acceptance: CI passes on push*

---

## Module 2: Core/Foundation

Base architecture and shared utilities.

### Tasks

- [ ] **Create project structure** [S]
  - Set up directory layout
  - Create index files
  - *Acceptance: Clean import paths work*

- [ ] **Implement error handling** [M]
  - Create error types/classes
  - Set up error boundaries (if UI)
  - Add logging utility
  - *Acceptance: Errors logged consistently*

- [ ] **Create shared utilities** [S]
  - Add common helper functions
  - Create type definitions
  - *Acceptance: Utils importable and typed*

- [ ] **Configure environment** [S]
  - Set up env validation
  - Create `.env.example`
  - Add env loading logic
  - *Acceptance: App reads env vars correctly*

---

## Module 3: Data Layer

Database, models, and data access.

### Tasks

- [ ] **Set up database connection** [M]
  - Install ORM/driver
  - Configure connection
  - Test connectivity
  - *Acceptance: Can connect to DB*

- [ ] **Create data models** [M]
  - Define schemas/models for: {list entities}
  - Add validations
  - *Acceptance: Models validated and typed*

- [ ] **Implement migrations** [M]
  - Create initial migration
  - Set up migration scripts
  - *Acceptance: Migrations run cleanly*

- [ ] **Add seed data** [S]
  - Create seed script
  - Add development data
  - *Acceptance: DB seeded with test data*

---

## Module 4: {Feature Module}

{Description of this feature area}

### Tasks

- [ ] **{Task 1}** [{Size}]
  - {Subtask 1}
  - {Subtask 2}
  - *Acceptance: {criteria}*

- [ ] **{Task 2}** [{Size}]
  - {Subtask 1}
  - {Subtask 2}
  - *Acceptance: {criteria}*

---

## Module 5: Authentication (if applicable)

User auth and authorization.

### Tasks

- [ ] **Set up auth provider** [M]
  - Install auth library
  - Configure providers
  - *Acceptance: Auth flow works*

- [ ] **Implement login/logout** [M]
  - Create auth pages/endpoints
  - Handle sessions/tokens
  - *Acceptance: Users can sign in/out*

- [ ] **Add protected routes** [S]
  - Create auth middleware
  - Protect relevant routes
  - *Acceptance: Unauthorized access blocked*

- [ ] **Implement authorization** [M]
  - Define roles/permissions
  - Add permission checks
  - *Acceptance: Role-based access working*

---

## Module 6: Testing

Comprehensive test coverage.

### Tasks

- [ ] **Write unit tests** [M]
  - Test utilities
  - Test business logic
  - *Acceptance: >80% coverage on core*

- [ ] **Write integration tests** [M]
  - Test API endpoints
  - Test data flows
  - *Acceptance: Critical paths tested*

- [ ] **Write E2E tests** [L]
  - Set up E2E framework
  - Test user flows
  - *Acceptance: Happy paths covered*

---

## Module 7: Documentation

Project documentation.

### Tasks

- [ ] **Write README** [S]
  - Add project description
  - Include setup instructions
  - Add usage examples
  - *Acceptance: New dev can set up from README*

- [ ] **Document API** [M]
  - Add OpenAPI/JSDoc comments
  - Generate API docs
  - *Acceptance: API endpoints documented*

- [ ] **Add inline documentation** [S]
  - Document complex functions
  - Add type documentation
  - *Acceptance: Code self-documenting*

---

## Dependency Graph

```
Module 1 (Setup)
    ↓
Module 2 (Core) ←→ Module 3 (Data)
    ↓
Module 4 (Features) ← Module 5 (Auth)
    ↓
Module 6 (Testing)
    ↓
Module 7 (Docs)
```

## Suggested Order

1. Complete Module 1 entirely first
2. Module 2 + 3 can be done in parallel
3. Feature modules depend on 2 + 3
4. Auth can be added at any point after core
5. Testing throughout (TDD) or at end
6. Docs last or continuously
```

---

## Module Templates by Project Type

### Additional modules for Web Apps:
- **UI Components**: Design system, reusable components
- **Pages/Routes**: Page components, routing setup
- **State Management**: Global state, data fetching
- **Styling**: Theme, responsive design

### Additional modules for APIs:
- **Middleware**: Request processing, validation
- **Controllers**: Request handlers
- **Services**: Business logic layer
- **Caching**: Response caching, rate limiting

### Additional modules for CLI Tools:
- **Commands**: Individual command implementations
- **Config**: Configuration file handling
- **Output**: Formatters, colors, progress bars

### Additional modules for Libraries:
- **Public API**: Exported functions/classes
- **Build**: Bundle configuration, tree shaking
- **Publishing**: npm/PyPI setup, versioning
- 