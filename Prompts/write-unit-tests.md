---
name: write-unit-tests
description: Generate focused unit tests for normal behavior, edge cases, and error handling.
---

# Write Unit Tests

## Overview

Create practical unit tests for the supplied function or module. Cover expected behavior, meaningful boundary cases, and error handling using the specified testing framework. Keep tests focused, independent, and consistent with the code's existing public interface.

## Inputs/Placeholders

- **Code to test:** `[CODE_TO_TEST]`
- **Testing framework:** `[TESTING_FRAMEWORK]`
- **Edge cases to include:** `[EDGE_CASES_TO_INCLUDE]`

Provide relevant dependencies, existing test conventions, and expected behavior when available.

## Instructions

1. Identify the public behavior of `[CODE_TO_TEST]` and the test setup required by `[TESTING_FRAMEWORK]`.
2. Write tests for representative happy paths, `[EDGE_CASES_TO_INCLUDE]`, and relevant error handling. Include only cases that apply to the code's behavior.
3. Make assertions specific enough to detect regressions without depending on irrelevant implementation details.
4. Keep each test independent and readable. Avoid unnecessary mocks; when a dependency must be isolated, mock only the relevant boundary.
5. Use the framework's established syntax and conventions. Do not invent expected results when they are not evident; state assumptions or request clarification.
6. Return the test code and briefly summarize the behaviors covered. Mention any setup or execution assumptions.

## Example Usage

```text
Testing framework: Jest
Edge cases to include: empty input, a single item, and negative values
Code to test:

export function total(values: number[]): number {
  return values.reduce((sum, value) => sum + value, 0);
}
```
