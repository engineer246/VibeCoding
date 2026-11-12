---
name: refactor-code
description: Refactor code for maintainability and modularity while preserving its external behavior.
---

# Refactor Code

## Overview

Improve the structure and maintainability of existing code without changing its external behavior. Apply the requested goals while respecting project conventions, dependencies, interfaces, and other constraints.

## Inputs/Placeholders

- **Code to refactor:** `[CODE_TO_REFACTOR]`
- **Refactoring goals:** `[REFACTORING_GOALS]`
- **Constraints:** `[CONSTRAINTS]`

Include relevant surrounding interfaces, tests, or project conventions when available.

## Instructions

1. Understand the code's current behavior and public interfaces before changing its structure.
2. Refactor toward `[REFACTORING_GOALS]` while following the stated `[CONSTRAINTS]`. Prefer small, cohesive changes that make responsibilities and data flow easier to understand.
3. Preserve observable behavior, including return values, side effects, error behavior, and public interfaces, unless a constraint explicitly says otherwise.
4. Avoid unrelated features, unnecessary abstractions, and new dependencies. Do not silently drop behavior that appears redundant or unclear.
5. Return the refactored code and a concise explanation of the structural changes. Call out assumptions or behavior that could not be verified.
6. Recommend focused tests or checks that would demonstrate behavior is preserved.

If essential context is missing, state what is needed rather than guessing at project-specific conventions.

## Example Usage

```text
Refactoring goals: extract validation into a small helper and make the main function easier to read
Constraints: keep the function signature and output unchanged; do not add dependencies
Code to refactor:

function createLabel(name: string, count: number): string {
  if (!name || name.trim().length === 0) {
    throw new Error("Name is required");
  }
  if (count < 0) {
    throw new Error("Count must not be negative");
  }
  return `${name.trim()} (${count})`;
}
```
