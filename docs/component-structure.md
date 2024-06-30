## Component Structure

This document provides best practices for structuring individual React components.

<div style="background: #B00020; padding: 8px; font-size: 11px; border-radius: 2px; font-weight: bold;">
IMPORTANT: If a component has significant logic beyond rendering (i.e., it's not purely presentational), consider it a feature instead of a component. Place such features in a dedicated `features/` directory, e.g., `/features/awesome-feature/`.
</div>

### Folder Structure

For each component, maintain a cohesive folder structure:

```sh
Button/
├── Button.tsx           # contains the JSX and logic for the Button component.
└── Button.module.css    # css module for scoped styles specific to the Button component.
```
