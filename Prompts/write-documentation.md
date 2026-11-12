---
name: write-documentation
description: Create or update documentation that reflects verified project behavior.
---

# Write Documentation

## Overview

Create or update `[DOCUMENTATION GOAL]` for `[AUDIENCE]`. Make it accurate to the project, easy to follow, and consistent with existing documentation.

## Inputs

- **Documentation goal:** `[DOCUMENTATION GOAL]`
- **Audience:** `[AUDIENCE]`
- **Destination, if known:** `[DESTINATION]`
- **Constraints or style requirements:** `[CONSTRAINTS]`

## Instructions

1. Inspect relevant existing documentation, source code, configuration, and repository guidance before describing project behavior.
2. Identify what the audience needs to accomplish and structure the documentation around that task.
3. Separate verified facts from assumptions. Do not invent commands, settings, features, prerequisites, or expected output.
4. Use concise headings, clear steps, and examples only where they help the reader. Mark values the reader must replace with descriptive square-bracket placeholders.
5. Update directly related documentation or links when the requested change makes them stale. Avoid unrelated rewrites.
6. Check relative links, code fences, command names, and examples against the repository where possible.
7. Summarize what changed and note anything that could not be verified.

## Output

When asked to edit the repository, make the documentation change in the appropriate location. Otherwise, return a ready-to-use draft. In either case, briefly report the destination, audience, and verification limitations.

## Example Request

> Update the onboarding guide for new contributors. Verify the setup steps against the repository, keep it beginner-friendly, and don't change the development workflow.
