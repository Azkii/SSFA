## Component Structure

This document provides best practices for structuring individual React components.

<div style="background: #B00020; padding: 8px; font-size: 11px; border-radius: 2px; font-weight: bold;">
IMPORTANT: If a component has significant logic beyond rendering (i.e., it's not purely presentational), consider it a feature instead of a component. Place such features in a dedicated `features/` directory, e.g., `/features/awesome-feature/`.
</div>

### Folder Structure

For each component, maintain a cohesive folder structure:

```sh
button/
├── button.tsx           # contains the JSX and logic for the Button component.
└── button.module.css    # css module for scoped styles specific to the Button component.
```

### Component Example

```tsx
// button.tsx
import React, { ButtonHTMLAttributes, ReactNode } from "react";
import clsx, { ClassArray } from "clsx";
import style from "./button.module.scss";

type Size = "small" | "medium" | "large";
type ButtonVariant = "solid" | "bordered";
type ButtonColor = "primary" | "secondary";

interface Props extends ButtonHTMLAttributes<HTMLButtonElement> {
  children: ReactNode;
  color?: ButtonColor;
  variant?: ButtonVariant;
  size?: Size;
  classNames?: ClassArray;
}

export const Button = ({
  children,
  color = "primary",
  variant = "solid",
  size = "medium",
  classNames = [],
  ...props
}: Props) => {
  return (
    <button
      className={clsx(
        style.button,
        style[`button-${size}`],
        style[`button-${variant}`],
        style[`button-${color}`],
        ...classNames
      )}
      {...props}
    >
      {children}
    </button>
  );
};
```
