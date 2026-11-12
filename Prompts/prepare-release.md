---
name: prepare-release
description: Prepare accurate release notes and a practical release-readiness checklist.
---

# Prepare Release Notes

## Overview

Prepare release notes and a readiness checklist for `[RELEASE OR VERSION]` based on verified changes in `[CHANGE RANGE OR SOURCE]`.

## Inputs

- **Release or version:** `[RELEASE OR VERSION]`
- **Change range or source:** `[CHANGE RANGE OR SOURCE]`
- **Audience:** `[AUDIENCE]`
- **Known constraints or release requirements:** `[CONSTRAINTS]`

## Instructions

1. Inspect the provided change range, merged changes, or release notes source. If repository history is available, use it to verify what changed.
2. Group user-visible changes into clear categories, such as Added, Changed, Fixed, and Removed, only when those categories apply.
3. Describe impact in plain language. Do not claim a fix, compatibility guarantee, security improvement, or completed check without evidence.
4. Flag breaking changes, required migrations, known issues, and upgrade actions when supported by the source.
5. Provide a readiness checklist tailored to the project and distinguish completed checks from recommended or unverified ones.
6. Ask for the change range or other essential context if it is missing; do not fabricate release content.

## Output

Return:

1. **Draft release notes**
2. **Upgrade or compatibility notes**, if applicable
3. **Release-readiness checklist**, marking each item as verified, pending, or not applicable
4. **Unverified details or questions**

## Example Request

> Prepare audience-friendly notes for version 2.4 from the commits since v2.3. Call out any database migration and list tests that still need to run.
