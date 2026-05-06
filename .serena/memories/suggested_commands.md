# Suggested Commands

## Setup
- `npm install`

## Development
- `npx nx serve shop` - Serve the Angular shop application (and API)
- `npx nx serve api` - Serve the API backend separately
- `npx nx graph` - Visualize the project graph

## Quality Assurance
- `npx nx run-many -t lint` - Lint all projects
- `npx nx run-many -t test` - Run all unit tests
- `npx nx e2e shop-e2e` - Run end-to-end tests

## Build & Deployment
- `npx nx run-many -t build` - Build all projects
- `npx nx docker:build api` - Build Docker image for the API
