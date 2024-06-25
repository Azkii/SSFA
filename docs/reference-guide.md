# Reference Guide

## Best Practices

### Single Export per Component File

Each component file should have only one export. This ensures that each file maintains a single responsibility, aligning with best practices for code organization. If a file contains multiple components, each serving distinct responsibilities, consider separating them into individual files.

### Module Name Matching File Name

Exported module name should match the file name.

### No Default Exports

Use named exports to improve code clarity. [Learn More](https://basarat.gitbook.io/typescript/main-1/defaultisbad).

### Single Responsibility Functions

Ensure functions are small and focused on a single task.

### Guard Clauses

Use guard clauses to handle errors and edge cases early in functions. [Learn More](https://medium.com/@timothydan/javascript-guard-clauses-64b999e3240).

### Avoid Primitive Obsession

Use domain-specific types instead of primitive types to model your data. [Learn More](https://refactoring.guru/smells/primitive-obsession).

### Prefer Data Immutability

Ensure data immutability wherever feasible. [Learn More](https://immutable-js.github.io/immutable-js/).

### No Barrel Files

Avoid using barrel files to re-export modules. [Learn More](https://marvinh.dev/blog/speeding-up-javascript-ecosystem-part-7/).

### Impureim sandwich

Separate side effects from pure logic. [Learn More](https://blog.ploeh.dk/2020/03/02/impureim-sandwich/).

### Avoid Large Components

Avoid large components with nested rendering functions. [Learn More](https://helderberto.com/reactjs-tips-tricks-avoid-nested-render-functions).

## Architecture & Structure

### Screaming Architecture

Code should clearly communicate its intent and structure. [Learn More](https://blog.cleancoder.com/uncle-bob/2011/09/30/Screaming-Architecture.html).

### Component Driven User Interfaces

The development and design practice of building user interfaces with modular components. UIs are built from the “bottom up” starting with basic components then progressively combined to assemble screens. [Learn More](https://www.componentdriven.org/).

### Unidirectional Codebase Architecture

Enforce unidirectional codebase architecture: code should flow in one direction, from shared parts of the code to the application (shared → features → app). [Learn More](https://github.com/alan2207/bulletproof-react/blob/master/docs/project-structure.md).

### Connect with External Services through Adapters

Implement adapters to decouple external service integrations. [Learn More](https://refactoring.guru/design-patterns/adapter).

### OpenAPI for Backend Types

Use OpenAPI codegen to generate TypeScript types automatically. [Learn More](https://heyapi.vercel.app/openapi-ts/get-started.html).

### Keep shared types in `/types` directory

Keep shared types in a central files to promote reuse and consistency.

## Development Tools & Techniques

### Path Aliases in TypeScript

Use `tsconfig` to set up path aliases for cleaner imports. [Learn More](https://dev.to/larswaechter/path-aliases-with-typescript-in-nodejs-4353).

### Document UI Components

Document your UI components using tools like Storybook. [Learn More](https://storybook.js.org/).

### Global Styles from Theme

Use a centralized theme for consistent styling across the application. [Learn More](https://mui.com/material-ui/customization/theming/).

### Minimize Libraries

The fewer libraries used, the better for easier long-term maintenance.

### Never Use numbers for Money

Avoid using numbers for monetary values (IEEE 754). [Learn More](https://en.wikipedia.org/wiki/IEEE_754).
Use libraries like [dinerojs](https://dinerojs.com/) instead.
