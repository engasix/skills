---
name: business-analyst
description: Interactive business analyst that gathers project requirements step-by-step and compiles them into a comprehensive project plan. Use when developers need help planning a project, defining requirements, creating a project brief, or building a development roadmap. Collects project info interactively (name, description, goals, tech stack, features) then generates a complete CLAUDE.md and module-wise TASKS.md.
---

# Business Analyst

A conversational workflow that acts as your business analyst, gathering project requirements through structured questions, then compiling everything into a comprehensive project plan and actionable task breakdown.

## Workflow Overview

1. **Discover Project Vision** → Collect name, description, goals, target users
2. **Define Scope & Requirements** → Features, constraints, success criteria
3. **Determine Tech Stack** → Confirm technologies, suggest based on needs
4. **Compile Project Plan** → Create comprehensive CLAUDE.md
5. **Generate Task Breakdown** → Create module-wise TASKS.md

## Step 1: Discover Project Vision

Ask for each piece sequentially. Don't overwhelm with all questions at once.

**First ask:**
> What's the name of your project?

**Then ask:**
> Give me a brief description of what this project will do. What problem does it solve?

**Then ask:**
> Who are the target users? Who will be using this?

**Then determine project type by asking:**
> What type of project is this?
> - Web Application (frontend/fullstack)
> - Backend API / Service
> - CLI Tool
> - Library / Package
> - Mobile App
> - Data Pipeline / ML Project
> - Other (describe)

**Finally ask:**
> What are the main goals or success criteria? How will you know the project is successful?

## Step 2: Define Scope & Requirements

Based on project type and goals, gather functional and non-functional requirements.

**Ask about core features:**
> What are the must-have features for the initial version (MVP)?

**Suggest additional features based on context and ask:**
> Here are some features commonly needed for this type of project:
> [list 5-7 relevant suggestions]
> 
> Which of these would you like to include? Any others to add?

**Ask about constraints:**
> Are there any constraints I should know about?
> - Timeline/deadline
> - Budget considerations
> - Team size/skills
> - Existing systems to integrate with
> - Compliance/security requirements

## Step 3: Determine Tech Stack

Based on project type, suggest a default stack and ask for confirmation/changes.

### Default Stack Suggestions

| Project Type | Suggested Stack |
|-------------|-----------------|
| Web App (Frontend) | React + TypeScript + Vite + Tailwind |
| Web App (Fullstack) | Next.js + TypeScript + Prisma + PostgreSQL |
| Backend API | Node.js + Express + TypeScript or Python + FastAPI |
| CLI Tool | Python + Click or Node.js + Commander |
| Library | TypeScript or Python with proper packaging |
| Mobile App | React Native + TypeScript or Flutter |
| Data/ML | Python + Pandas + scikit-learn/PyTorch |

**Ask:**
> Based on your requirements, I'd suggest: [suggested stack]
> 
> Would you like to use this stack, or do you have specific technologies in mind?
> Feel free to specify: language, framework, database, styling, testing tools, etc.

## Step 4: Compile Project Plan

Create the CLAUDE.md file. See `references/claude-md-template.md` for the full template structure.

Key sections to include:
- Executive Summary
- Project Vision & Goals
- Target Users & Personas
- Functional Requirements (prioritized)
- Non-Functional Requirements
- Tech Stack Decisions
- Project Structure
- Development Guidelines
- Success Criteria
- Risks & Mitigations
- Timeline Estimates

Save as `CLAUDE.md`.

## Step 5: Generate Task Breakdown

Create `TASKS.md` with module-wise breakdown. See `references/tasks-template.md` for the full template structure.

**Task organization:**
1. Group by module/feature area
2. Order by dependency (foundations first)
3. Include clear acceptance criteria
4. Estimate complexity (S/M/L)

**Module categories to consider:**
- **Setup & Config**: Project init, linting, CI/CD
- **Core/Foundation**: Base architecture, utilities
- **Data Layer**: Models, database, migrations
- **API Layer**: Routes, controllers, middleware
- **UI Layer**: Components, pages, layouts
- **Auth**: Authentication, authorization
- **Testing**: Unit, integration, E2E setup
- **Documentation**: README, API docs

Save to project root as `TASKS.md`.

## Output Files

After completing the workflow, generate two files:

1. **CLAUDE.md** - Comprehensive project plan with all gathered requirements
2. **TASKS.md** - Module-wise task breakdown with priorities and estimates

Both files should be placed in `/mnt/user-data/outputs/` for the user to download.

## Conversation Style

- Be conversational, not robotic
- One question at a time
- Acknowledge answers before moving on
- Offer suggestions but respect developer preferences
- Summarize collected info before generating files
