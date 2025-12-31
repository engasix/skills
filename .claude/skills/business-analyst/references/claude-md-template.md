# CLAUDE.md Template

Use this template when generating the CLAUDE.md file. Adapt sections based on project type and complexity.

---

```markdown
# {PROJECT_NAME}

## Executive Summary

{2-3 sentence overview of the project, its purpose, and expected outcome.}

**Project Type:** {Web App / API / CLI / Library / Mobile / Data Pipeline}
**Estimated Complexity:** {Small / Medium / Large}
**Target Completion:** {Timeline if provided}

---

## Project Vision

### Problem Statement
{What problem does this project solve? Why does it need to exist?}

### Solution Overview
{How does this project solve the problem? High-level approach.}

### Goals & Success Criteria
1. {Goal 1 - measurable if possible}
2. {Goal 2}
3. {Goal 3}

---

## Target Users

### Primary Users
- **{User Type 1}**: {Description, needs, how they'll use the product}

### Secondary Users
- **{User Type 2}**: {Description}

### User Stories
- As a {user type}, I want to {action} so that {benefit}
- As a {user type}, I want to {action} so that {benefit}
- As a {user type}, I want to {action} so that {benefit}

---

## Requirements

### Functional Requirements (MVP)

| ID | Requirement | Priority | Notes |
|----|-------------|----------|-------|
| FR-1 | {Requirement description} | Must Have | |
| FR-2 | {Requirement description} | Must Have | |
| FR-3 | {Requirement description} | Should Have | |
| FR-4 | {Requirement description} | Nice to Have | |

### Non-Functional Requirements

| Category | Requirement |
|----------|-------------|
| Performance | {e.g., Page load < 2s, API response < 200ms} |
| Scalability | {e.g., Support 1000 concurrent users} |
| Security | {e.g., HTTPS, data encryption, auth requirements} |
| Accessibility | {e.g., WCAG 2.1 AA compliance} |
| Compatibility | {e.g., Modern browsers, mobile responsive} |

### Out of Scope (v1)
- {Feature explicitly not included in initial version}
- {Feature explicitly not included}

---

## Technical Approach

### Tech Stack

| Layer | Technology | Rationale |
|-------|------------|-----------|
| Frontend | {e.g., React + TypeScript} | {Why this choice} |
| Backend | {e.g., Node.js + Express} | {Why this choice} |
| Database | {e.g., PostgreSQL} | {Why this choice} |
| Hosting | {e.g., Vercel / AWS} | {Why this choice} |
| Testing | {e.g., Vitest + Playwright} | {Why this choice} |

### Architecture Overview
{High-level description of system architecture}

```
{Simple ASCII diagram or description of components}
```

### Project Structure
```
{project-name}/
├── src/
│   ├── {folder}/     # {Purpose}
│   └── {folder}/     # {Purpose}
├── tests/
└── {config files}
```

### Development Guidelines
- {Coding standard 1}
- {Pattern to follow}
- {Convention to use}

---

## Constraints & Assumptions

### Constraints
- {Timeline constraint}
- {Budget constraint}
- {Technical constraint}
- {Resource constraint}

### Assumptions
- {Assumption about users}
- {Assumption about environment}
- {Assumption about integrations}

### Dependencies
- {External service or API}
- {Third-party library}
- {Team or resource dependency}

---

## Risks & Mitigations

| Risk | Impact | Likelihood | Mitigation |
|------|--------|------------|------------|
| {Risk description} | High/Med/Low | High/Med/Low | {How to address} |
| {Risk description} | High/Med/Low | High/Med/Low | {How to address} |

---

## Timeline & Milestones

### Phase 1: Foundation ({duration})
- Project setup & configuration
- Core architecture
- Basic infrastructure

### Phase 2: Core Features ({duration})
- {Feature set 1}
- {Feature set 2}

### Phase 3: Polish & Launch ({duration})
- Testing & bug fixes
- Documentation
- Deployment

### Key Milestones
- [ ] {Milestone 1} - {Target date}
- [ ] {Milestone 2} - {Target date}
- [ ] {Milestone 3} - {Target date}

---

## Commands Reference

```bash
# Development
{package-manager} dev          # Start dev server
{package-manager} build        # Production build

# Testing
{package-manager} test         # Run tests

# Code Quality
{package-manager} lint         # Run linter

# Database (if applicable)
{package-manager} db:migrate   # Run migrations
```

---

## Environment Variables

```env
# Required
{VAR_NAME}=        # {Description}

# Optional
{VAR_NAME}=        # {Description}
```

---

## Next Steps

1. Review and approve this project plan
2. Set up development environment
3. Begin Phase 1 tasks (see TASKS.md)
```

---

## Customization by Project Type

**Web Apps**: Add sections for routing, component hierarchy, state management
**APIs**: Add endpoint planning, authentication flow, rate limiting strategy  
**CLI Tools**: Add command structure, config file format, installation instructions
**Libraries**: Add public API design, versioning strategy, publishing plan
**Mobile Apps**: Add platform targets, offline support, app store requirements
**Data/ML**: Add data sources, pipeline stages, model evaluation criteria
