# Repository Structure

## Root

```text
/client     → Vue frontend application
/server     → ASP.NET Core backend API
/docs       → Architecture and engineering documentation
/specs      → Product requirements and feature specifications
/scripts    → Utility/setup scripts
```

---

## Frontend Structure

```text
client/src/
├── assets/        → Static assets and global styles
├── components/    → Reusable UI components
├── composables/   → Reusable logic/state hooks
├── pages/         → Route-level views
├── router/        → Vue Router configuration
├── services/      → API communication layer
├── stores/        → Pinia global state stores
├── types/         → Shared TypeScript types/interfaces
└── utils/         → Stateless helper functions
```

---

## Backend Structure

```text
server/
├── Controllers/   → API endpoints
├── Services/      → Business logic layer
├── Repositories/  → Data access layer
├── DTOs/          → API request/response models
├── Models/        → Database entity models
├── Data/          → DbContext and EF configuration
└── Interfaces/    → Shared contracts/interfaces
```