---
name: generate-prompt
description: Turn a rough idea into a polished, repository-aligned prompt, skill, or agent definition.
---

# Generate a Prompt, Skill, or Agent

## Overview

Use this meta-prompt when you have a short idea or goal and want to bootstrap a complete, ready-to-adapt prompt, skill, or agent definition for the repository you are currently working in. It guides an AI assistant to inspect the repository's conventions, clarify the request when needed, and produce a self-contained Markdown resource with practical examples.

## Instructions for the AI

Analyze the user's rough idea and create a resource that is specific to the current repository without assuming conventions that have not been verified.

1. **Understand the repository.** Inspect relevant guidance, existing resources, and templates before drafting. Check the target resource directory and follow its naming and content conventions. Prefer an existing template when one applies. Do not copy project-specific or sensitive information into a reusable resource.
2. **Choose the resource type.** Use the user's requested type (prompt, skill, or agent). If none is specified, infer the best fit from the goal and briefly state the choice. A prompt gives task instructions, a skill captures a repeatable workflow, and an agent defines a focused role and its boundaries.
3. **Resolve ambiguity.** Identify the intended user, task, expected result, and important constraints. Ask concise clarifying questions only when missing information would materially change the resource. Otherwise, make reasonable assumptions explicit or use clear placeholders.
4. **Draft for use.** Make the resource actionable, focused, portable, and self-contained. Include concrete steps and quality checks appropriate to its purpose. Avoid vague directions, redundant sections, unnecessary complexity, and unsupported claims about tools or repository behavior.
5. **Follow repository standards.** Use valid YAML frontmatter with a short, descriptive `name` and a concise `description` when the repository expects metadata. Use clean Markdown with a clear title and logical sections. Mark every value the user must supply with a descriptive placeholder in square brackets, such as `[TARGET TASK]` or `[OUTPUT FORMAT]`. Follow the repository's naming, placement, and template conventions.
6. **Make it practical.** Include at least one concise, realistic example showing how to provide inputs or apply the resource. Keep examples generic and safe to share.
7. **Check the result.** Confirm the YAML and Markdown are well formed, placeholders are clear and consistently named, instructions do not conflict, and the result can be used without relying on hidden context. State any assumptions that affect use.

Do not silently invent repository rules. If no applicable template or convention exists, use a simple portable Markdown structure and mention that choice.

## Interactive Workflow

Start from the user's raw idea. Collect or infer these inputs:

- **Target task or goal:** What the resource should help accomplish.
- **Resource type:** Prompt, skill, or agent; optional if the assistant can infer it.
- **Desired output format:** For example, Markdown prompt, skill instructions, or agent definition.
- **Constraints:** Audience, scope, tone, tools, safety boundaries, required checks, or things to avoid.
- **Destination:** Desired directory or filename, if known.

If essential details are missing, ask focused questions and allow the user to answer briefly. Do not make the user fill every field; infer reasonable defaults, clearly mark unknown details with placeholders, and proceed when the goal is sufficiently clear.

## Generated Output

Return the finished resource in a single, clearly labeled Markdown code block so it can be copied directly. Include:

1. YAML frontmatter with `name` and `description`, following repository conventions.
2. A descriptive title and a short purpose or overview.
3. Sections tailored to the resource type. A prompt should explain its task and expected output; a skill should define when and how to apply its workflow; an agent should state its role, responsibilities, and boundaries.
4. Clear square-bracket placeholders for user-supplied values, plus any important inputs, assumptions, and constraints.
5. Actionable instructions, expected output structure, and relevant quality checks.
6. At least one practical, generic example.

After the code block, briefly state the selected resource type, any assumptions, and a suggested filename or destination if the user did not specify one.

## Example Request

> Turn this idea into a skill: help me review database migrations for compatibility and rollback risks. Keep it database-agnostic, include a checklist, and return Markdown.
