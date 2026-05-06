# Project Purpose
The project is an e-commerce showcase using an Nx monorepo. It consists of:
- `shop`: An Angular e-commerce application.
- `api`: A backend API serving product data.
- `shop-e2e`: Playwright end-to-end tests for the shop.
- Several shared libraries for features, data access, UI components, and models.

# Tech Stack
- Framework: Angular (v21)
- Monorepo Tool: Nx (v22)
- Backend: Node.js / Express
- Testing: Vitest (unit/integration), Playwright (e2e)
- Build Tool: Vite / Esbuild
- Linting/Formatting: ESLint, Prettier
- Infrastructure: Docker (for API)

# Code Style and Conventions
- TypeScript is used throughout.
- Nx Module Boundaries are enforced via ESLint tags:
  - `scope:shared`: Shared by all.
  - `scope:shop`: Shop-specific.
  - `scope:api`: API-specific.
  - `type:feature`, `type:data`, `type:ui`: Architectural layers.
- Standard Angular and TypeScript conventions are followed.

# Development Commands
- Install: `npm install`
- Serve Shop: `npx nx serve shop`
- Serve API: `npx nx serve api`
- Build All: `npx nx run-many -t build`
- Test All: `npx nx run-many -t test`
- Lint All: `npx nx run-many -t lint`
- E2E Tests: `npx nx e2e shop-e2e`
- Project Graph: `npx nx graph`
- Docker Build API: `npx nx docker:build api`

# Codebase Structure
- `apps/api`: Backend API.
- `apps/shop`: Angular frontend.
- `apps/shop-e2e`: Playwright tests.
- `libs/api/products`: API product service.
- `libs/shared/models`: Shared data models.
- `libs/shop/data`: Shop data access.
- `libs/shop/feature-products`: Product listing feature.
- `libs/shop/feature-product-detail`: Product detail feature.
- `libs/shop/shared-ui`: Shared UI components.
