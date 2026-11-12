---
name: code-review
description: Review code for correctness, edge cases, readability, performance, and security concerns.
---

# Code Review

## Overview

Review a code snippet or proposed change in the specified language or framework. Identify concrete bugs and risks, including edge cases, readability or maintainability concerns, performance problems, and security issues. Prioritize findings by impact and support each finding with evidence from the supplied code.

## Inputs/Placeholders

- **Language or framework:** `[LANGUAGE_OR_FRAMEWORK]`
- **Code or change to review:** `[CODE_TO_REVIEW]`
- **Areas to emphasize:** `[FOCUS_AREAS]`

Provide any relevant surrounding context, expected behavior, or constraints with the code when available.

## Instructions

1. Review the supplied code in the context of `[LANGUAGE_OR_FRAMEWORK]` and the stated `[FOCUS_AREAS]`.
2. Look for functional bugs, boundary conditions, error handling gaps, unintended behavior changes, and relevant security concerns. Also consider readability and performance where supported by the code.
3. Report only actionable findings. For each finding, include a severity, the relevant code or behavior, why it is a problem, and a practical recommendation.
4. Do not invent missing context or report speculative issues as confirmed. State assumptions and ask for essential missing information when needed.
5. If you find no material issues, say so and briefly note the scope and limitations of the review.

Return results in this order:

1. **Findings**, highest severity first. If there are none, state “No material findings.”
2. **Questions or assumptions**, if any.
3. **Summary**, including areas reviewed and any important limitations.

## Example Usage

```text
Language or framework: TypeScript with Node.js
Areas to emphasize: input validation, error handling, and edge cases
Code or change to review:

function average(values: number[]): number {
  return values.reduce((sum, value) => sum + value, 0) / values.length;
}
```
