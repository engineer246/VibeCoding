---
name: feature-planning
description: Use a repeatable, repository-aware workflow to scope a feature and define its implementation and verification steps.
---

# Feature Planning

## When to Use

Use this workflow when a user wants to explore, scope, or plan a feature before implementation.

## Workflow

1. **Clarify the outcome.** Identify who the feature serves, the problem it addresses, and any constraints. Ask only questions whose answers would materially change the plan.
2. **Inspect the project.** Read relevant guidance and trace the existing behavior, architecture, and conventions that the feature may affect. Cite concrete files or components when available.
3. **Set boundaries.** State assumptions, exclusions, and dependencies. Separate observed project facts from proposals.
4. **Plan in increments.** List a small sequence of implementation steps, grouped by the components they affect. Avoid prescribing files or designs without repository evidence.
5. **Define completion.** Write observable acceptance criteria and focused tests or checks. Include compatibility, data migration, accessibility, or security considerations only when relevant.
6. **Present open questions.** Surface unresolved decisions and risks without blocking on details that can be safely assumed.

## Boundaries

- Planning does not authorize implementation; wait for an explicit request before changing code.
- Do not invent repository conventions, product requirements, or technical constraints.
- Keep recommendations proportional to the feature and existing project.

## Expected Result

Provide the feature goal and assumptions, relevant project context, ordered steps, acceptance criteria, verification, and material risks or open questions.

## Example

> Plan a search filter for the existing activity page. Inspect the current UI and API flow, keep the current permissions, and don't implement the change.
