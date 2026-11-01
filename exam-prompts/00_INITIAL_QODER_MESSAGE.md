# First message to paste into Qoder on exam day

Use this **after** opening the official exam repository in Qoder, placing the permitted instruction files in it, and attaching or adding the official exam brief. Do not run this in the preparation repository.

```text
Read AGENTS.md and exam-prompts/01_PLAN_PROMPT.md, then read the ENTIRE official exam specification and marking rubric attached to this task or included in this repository.

The exam specification, submission instructions and marking rubric take priority over my preferences.

First verify that this is the correct exam repository and branch, inspect the existing Git remote, and check whether Git authentication and pushing are available. Do not push to an unverified remote. Never request or print personal access tokens in chat.

Follow the planning-stage instructions. Identify mandatory and automarked requirements, constraints, submission rules, the simplest suitable architecture, database choice, expected dependencies and their justification, and a ranked optional-feature batch plan based on marks, effort, prerequisites and regression risk.

Use the preferences in AGENTS.md: Node.js + Vite + React when suitable, minimal dependencies, a clear pastel UI with light/dark mode when appropriate, an accurate README, regular safe commits and pushes, hands-on smoke tests and economical credit usage.

Save the plan to EXAM_PLAN.md. Do not install dependencies or build the application yet. Give me a concise summary and STOP for my approval.
```

## After approving the plan

Paste: `Follow exam-prompts/02_BASE_PROMPT.md and the approved EXAM_PLAN.md. Build the mandatory working base.`

## After testing and approving the base

Paste: `My manual base smoke test PASSED. Follow exam-prompts/03_BATCH_PROMPT.md for the next approved feature batch.`

For later batches, use the same message with `batch` instead of `base`.

## When the submission deadline approaches

Paste: `Follow exam-prompts/04_FINAL_AUDIT_PROMPT.md. Freeze new features and verify the final submission.`

**Note:** If you store prompt files at the repository root rather than inside `exam-prompts/`, remove the `exam-prompts/` prefix in these messages.
