---
name: readme-generator
description: Create or improve a repository README using verified project details and audience needs.
---

# Generate or Improve a README

## Overview

Create or update a README for `[REPOSITORY OR PROJECT]` that helps `[TARGET AUDIENCE]` understand and use the project. Support both new repositories and existing ones. Base all project-specific details on inspected files or information supplied by the user.

## Inputs

- **Repository or project:** `[REPOSITORY OR PROJECT]`
- **Target audience:** `[TARGET AUDIENCE]`
- **README location, if known:** `[README PATH]`
- **Goals or required sections:** `[GOALS OR REQUIRED SECTIONS]`
- **Style, length, or other constraints:** `[CONSTRAINTS]`

Infer reasonable defaults when inputs are missing. Ask a focused question only when the answer would materially change the README.

## Instructions

1. **Find the right scope.** Inspect the repository structure and relevant guidance. Identify whether the README is for the repository root, a package, or a subproject. Use the specified path when provided; otherwise, use the root `README.md` unless the project structure clearly calls for a more specific location.
2. **Inspect before writing.** Check relevant source files, manifests, scripts, configuration, tests, and existing documentation. Use them to verify the project name, purpose, capabilities, prerequisites, setup steps, commands, examples, and links.
3. **Handle existing content carefully.** If the target README exists, read it first. Preserve accurate, useful material and make the smallest changes that satisfy the request. Do not replace or remove content wholesale unless the user asks for a rewrite.
4. **Choose sections for the project.** Include only sections that help the audience. Depending on the project, useful sections may include:
   - Project purpose and key capabilities
   - Prerequisites and installation or setup
   - Quick start and common usage
   - Configuration and environment variables
   - Development, tests, and build commands
   - Examples, API usage, or screenshots
   - Deployment, contributing, licensing, or support
5. **Keep instructions trustworthy.** Do not invent features, commands, versions, URLs, environment variables, licensing terms, badges, or guarantees. Prefer exact commands verified in repository files. If a necessary fact cannot be confirmed, ask the user or mark it clearly as `[NEEDS CONFIRMATION: ...]`; do not present guesses as fact.
6. **Write for the reader.** Start with a concise explanation of what the project does and who it is for. Put the simplest useful path first, explain non-obvious steps, and keep detail proportional to the project.
7. **Check the result.** Verify that commands and examples agree with the inspected project, relative links point to the right locations, headings and code fences are valid, and placeholders are clear. Avoid including secrets or private information.

## Output

- If asked to edit the repository, create or update the appropriate README and summarize what changed.
- If asked for a draft, return the complete README in one Markdown code block.
- In either case, briefly state the selected path and audience, list any unverified details or placeholders, and report which commands, links, or examples were checked.

## Example Requests

**New repository**

> Create a root README for this small Rust CLI. Inspect the repository for the actual build and run commands. The audience is developers evaluating whether to use it.

**Existing repository**

> Improve the README for the `packages/web` app. Keep the existing deployment notes, verify the local setup instructions, and add a concise development section.
