---
name: plan-feature
description: Turn a feature idea into a scoped, repository-aware implementation plan.
---

# Plan a Feature

## Overview

Develop an actionable plan for `[FEATURE IDEA]` that fits the existing project. Inspect relevant repository guidance and code when available. Do not implement the feature unless explicitly asked.

## Inputs

- **Feature idea:** `[FEATURE IDEA]`
- **Desired outcome or user:** `[DESIRED OUTCOME]`
- **Constraints:** `[CONSTRAINTS]`
- **Relevant context:** `[RELEVANT CONTEXT]`

Provide only the context you have; do not make the user fill every field.

## Instructions

1. Restate the intended outcome and identify any material ambiguity. Ask a concise question only if an answer would change the plan; otherwise state reasonable assumptions.
2. Inspect relevant project guidance, architecture, and nearby implementation patterns before proposing changes. Distinguish observed facts from assumptions.
3. Break the work into small, ordered steps. Include likely files or components only when supported by repository evidence.
4. Call out dependencies, data or API changes, compatibility concerns, risks, and out-of-scope work when relevant.
5. Define observable acceptance criteria and focused tests or validation for the feature.
6. Keep the plan proportionate to the request. Avoid speculative architecture, unnecessary dependencies, and implementation details unsupported by the codebase.

## Output

Return:

1. **Goal and assumptions**
2. **Current project context** (if inspected)
3. **Implementation steps**, in order
4. **Acceptance criteria and verification**
5. **Risks or open questions**

If repository access is unavailable, state that limitation and make the plan explicitly provisional.

## Example Request

> Plan a way for users to export their saved reports as CSV. Keep existing report permissions, and do not implement it yet.
