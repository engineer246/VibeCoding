---
name: debug-error
description: Diagnose an error or unexpected behavior, identify its likely root cause, and propose a step-by-step fix.
---

# Debug an Error

## Overview

Analyze an error message, stack trace, or report of unexpected behavior. Use the relevant code and environment details to identify the most likely root cause, distinguish confirmed facts from hypotheses, and recommend a practical sequence of steps to verify and fix the issue.

## Inputs/Placeholders

- **Error or unexpected behavior:** `[ERROR_MESSAGE_OR_TRACE]`
- **Relevant code:** `[RELEVANT_CODE]`
- **Environment details:** `[ENVIRONMENT_DETAILS]`

Include reproduction steps, expected behavior, and recent changes when available.

## Instructions

1. Interpret the supplied error or behavior and identify the key diagnostic clues.
2. Trace those clues through `[RELEVANT_CODE]`, taking `[ENVIRONMENT_DETAILS]` into account. Do not assume a cause that is not supported by the evidence.
3. Explain the most likely root cause and indicate your confidence. If multiple causes remain plausible, rank them and describe how to distinguish them.
4. Provide a numbered troubleshooting and fix plan. Start with low-risk checks; include concrete code changes only when the evidence supports them.
5. Suggest a focused verification step or test for the fix. Ask for specific missing information if it is required to proceed.

Structure the response as **Diagnostic clues**, **Likely root cause**, **Step-by-step fix**, and **Verification**. Clearly label any hypotheses.

## Example Usage

```text
Error or unexpected behavior: TypeError: Cannot read properties of undefined (reading 'id')
Relevant code:

const userId = response.user.id;

Environment details: Node.js 20; response comes from an external API; the issue occurs intermittently.
```
