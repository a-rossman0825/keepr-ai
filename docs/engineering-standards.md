
# Keepr Ai Engineering Standards

## AI Workflow Standards
- Prefer incremental scoped changes over large multi-system rewrites.
- Tasks should be implemented one feature at a time.
- AI-generated code must be reviewed before commit.
- Preserve existing architectural patterns unless explicitly refactoring.
- New abstractions require justification.
- Avoid introducing dependencies without approval.
- Prefer extending existing patterns/files before introducing new abstractions or directories.
- Do not rewrite unrelated code during feature implementation.
- New features should include validation steps or testing instructions.

## Rules:

### Core Principles:
- Prefer simplicity over abstraction.
- Prioritize readability over brevity or cleverness.
- Files should have a single primary responsibility.
- Avoid premature optimization.
- Prefer explicitness over magic.
- Commit changes to git early and often. 
- Git commits should follow the "Conventional Commits specification" standard. 



### Frontend Standards:
- Use strict TypeScript at all times on the Frontend.
- Use Vue Composition API only.
- Keep components presentation-focused.
- Move business logic into composables or stores.
- API access belongs in services/
- Components never call axios directly.
- Use primarily Tailwind classes for styling.
- Use BEM naming convention for any SCSS classes.

### Backend Standards:
- Use RESTful API Endpoints
- Controllers should remain thin
- Business Logic belongs in Services
- Repositories handle data access only
- DTOs separate API contracts from models
- Validate all incoming requests
- Use XML comments for all backend methods, classes, fields, and all public members.

---

## Naming Conventions

### Frontend: 
- Vue components: kebab-case filenames
- Composables: useX naming
- Stores: useXStore naming

### Backend: 
- PascalCase C# types
- Interfaces prefixed with I
- Services suffixed with Service

---

## Folder Responsibilities

### Frontend:

#### components/
Reusable UI components only.

#### pages/
Route-level views.

#### composables/
Business Logic & local state management layer. 

#### stores/
Use stores only for shared cross-feature state.
Prefer composables for local feature logic/state.

#### services/
API communication layer.

#### utils/
reusable, stateless functions for specific computations.

#### assets/scss/
all global scss styles, _main.scss for import/export of styles, _variables.scss for theme vars, and style.scss for global classes.

### Backend:

#### Controllers/
Entry point for client requests, Injects Services interfaces.

#### Services/ 
Business Logic & user Authentication layer, Injects Repository interfaces.

#### Repositories/
Database Access Layer (uses Entity Framework), uses DbContext.

#### Models/
Data models 

#### DTOs/
Data Transfer Object models for client requests & responses.

---

## API Standards
- Use REST conventions
- Return consistent error responses
- Use DTOs for all data transfers
- Mutations require authentication
- Controllers should not access DbContext directly

---

 ## Testing Standards
- Critical business logic should be testable
- Prefer integration tests for API behavior
- UI flows will be validated with Playwright

---

## Documentation Standards
- Architecture decisions should be documented in /docs.
- Features should have specifications in /specs before implementation.
- Acceptance criteria should be defined before major feature work begins.