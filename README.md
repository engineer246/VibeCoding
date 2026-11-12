# VibeCoding

VibeCoding is a curated library of reusable resources for AI-assisted software development. It provides a home for prompts, skills, agents, templates, and supporting documentation that can be adapted to everyday coding workflows.

## Repository structure

```text
VibeCoding/
├── Agents/      # Custom AI agent definitions and role-specific instructions
├── Docs/        # Guides, references, and supporting documentation
├── Prompts/     # Reusable prompts for common development tasks
├── Skills/      # Reusable workflows and task-specific skill definitions
├── Templates/   # Starter files and templates for creating consistent resources
└── README.md    # Repository overview and contribution guidance
```

The directories above are the current top-level structure. Add resources to the appropriate directory as the library grows.

## Getting started

1. Browse the directory that best matches the task:
   - Use **Prompts** for ready-to-adapt instructions to give an AI assistant.
   - Use **Skills** for reusable procedures or specialized workflows.
   - Use **Agents** for role-specific behavior and guidance.
   - Use **Templates** to start a new resource in a consistent format.
   - Use **Docs** for explanations and reference material.
2. Read a resource before using it. Check its purpose, inputs, assumptions, and any tool or platform requirements.
3. Copy or reference the resource in your AI-enabled editor or assistant, then adapt placeholders and context to your project.
4. Keep project-specific details—such as code, file paths, and constraints—accurate when applying a general-purpose resource.

Resources are intended to be portable starting points. Integrate them using the conventions of your chosen AI tool; no particular editor or runtime is required by this repository.

## Naming and contribution conventions

Keep contributions focused, self-explanatory, and easy to discover:

- Use descriptive, lowercase kebab-case filenames, such as `review-pull-request.md` or `python-testing-agent.md`.
- Prefer Markdown (`.md`) for prompts, instructions, and documentation. Use YAML (`.yaml` or `.yml`) when a consuming tool expects structured configuration.
- Start each resource with a clear title and a short description of its purpose. Include relevant metadata where useful, for example:

  ```yaml
  ---
  name: review-pull-request
  description: Review a change for correctness, clarity, and regressions.
  ---
  ```

- Explain expected inputs, assumptions, and outputs when they are not obvious. Mark placeholders clearly, for example `[PROJECT CONTEXT]`.
- Put each resource in the most relevant directory. Use a short README or an index in a directory if its contents later need additional navigation.
- Avoid duplicating an existing resource; extend or clarify it when that better serves the use case.
- Keep examples generic and safe to share. Do not include credentials, private data, or project-specific secrets.
- When adding a resource, check its formatting and links, and verify that its instructions are understandable without relying on undocumented context.

## Contributing

Contributions that make AI-assisted development workflows clearer, safer, or more reusable are welcome. Before submitting a change, confirm that the resource is in the right directory, has a descriptive name and purpose, and follows the conventions above.
