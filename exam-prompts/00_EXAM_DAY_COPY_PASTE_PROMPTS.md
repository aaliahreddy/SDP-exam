# SDP Hackathon — Exact Qoder Messages (Exam Day)

**Purpose:** Open this file on the Wits lab computer and copy **one prompt at a time** into Qoder. Do not paste all prompts at once. Keep `AGENTS.md` at the repository root and the other stage prompts in `exam-prompts/`.

**Authority:** The official exam brief, rubric, submission rules and allowed tooling override these instructions. Confirm the **actual deadline** (the preparation plan assumes 6 hours until the official time is confirmed).

## 0 — First: lab setup and Git connection

**When:** Immediately after opening the *correct exam repository* in Qoder. If the lecturer supplies an assigned repo, use that, not a separate prep repo. Make sure the permitted instruction files are present.

**Paste:**

```text
Before coding, read AGENTS.md and exam-prompts/00_START_HERE.md. Verify that we are in the official exam repository and on the required branch. Check available versions of Node.js, npm and Git; inspect the lab environment for any required database or Docker services. Check git status, git remote -v and authentication. Verify that pushing to the correct remote works using a safe initial instruction/scaffold commit if permitted and there are changes; do not create meaningless commits just to test.

Do not install application dependencies or implement exam features yet. Do not put access tokens in chat, code, commands or remote URLs. Report the exact remote, branch, Node/npm versions, any blockers, and whether the first push succeeded. Follow the commit format in AGENTS.md.
```

**Then:** Attach or place the complete official specification and rubric where Qoder can read them.

## 1 — Read the brief and produce the plan

**When:** Once Git and the specification are accessible.

**Paste:**

```text
Read the ENTIRE official exam specification and marking rubric, AGENTS.md, exam-prompts/00_INITIAL_QODER_MESSAGE.md, and exam-prompts/01_PLAN_PROMPT.md. Follow the planning-stage instructions, with the official brief and submission rules taking priority.

Do not implement application code or install dependencies yet. Identify mandatory/automarked requirements, submission constraints, and optional marks; recommend the simplest suitable Node.js + Vite + React architecture unless the brief requires otherwise; choose the simplest supported persistent database; and rank optional features into small, practical batches by marks, incremental effort, dependencies and regression risk.

Save the complete approved-candidate plan to EXAM_PLAN.md and a concise current status to EXAM_STATUS.md. Present a short requirements checklist, architecture, and ranked batch queue. STOP and wait for my approval.
```

**Your check:** Is every mandatory requirement and automarker rule included? Are the architecture and optional batch rankings sensible? If not, request specific changes before approving.

## 2 — Approve the plan and implement the mandatory working base

**When:** After reviewing Step 1.

**Paste:**

```text
I approve the plan in EXAM_PLAN.md, subject to the official exam brief taking priority. Follow exam-prompts/02_BASE_PROMPT.md.

Build ONLY the mandatory, end-to-end working base with the simplest suitable architecture and minimal dependencies. Include the agreed pastel styling, clear navigation and functional light/dark mode where practical and allowed. Create/update README.md with exact fresh-clone instructions, environment configuration, database setup, run and test commands.

Run relevant build, runtime, API/database and automated checks. Keep the app running if your environment allows. Update EXAM_STATUS.md. Commit and push a verified stable milestone using the exact AGENTS.md commit convention, or a clearly labelled unverified checkpoint if manual approval is still pending. Verify the remote push.

Give me the app URL, a short 2–5 minute manual smoke test with expected results, any unverified items, and the last pushed commit. STOP. Do not start optional features.
```

**Your check:** Actually use the app from beginning to end. Do not approve only because the build passes.

## 3A — Base passed: start first optional feature batch

**When:** Only after completing the manual base test.

**Paste:**

```text
The mandatory base PASSED my manual smoke test. Follow exam-prompts/03_BATCH_PROMPT.md and the approved EXAM_PLAN.md queue.

Implement ONLY the next highest-priority viable feature batch. Preserve all working behaviour and do not add unrelated features or dependencies. Run focused checks plus essential regression checks, update README.md and EXAM_STATUS.md where needed, and commit/push the verified milestone using the AGENTS.md attribution style. Confirm the successful push.

Keep the app running where possible. Give me the URL and exact short manual tests for the new features and the existing main workflow. STOP for my approval before starting another batch.
```

## 3B — Current batch passed: next batch

**When:** After you have manually tested the current batch.

**Paste:**

```text
This batch PASSED my manual smoke test. Implement ONLY the next highest-ranked viable batch from the existing approved EXAM_PLAN.md queue, following exam-prompts/03_BATCH_PROMPT.md and AGENTS.md. Do not re-plan the whole application.

Use focused tests, protect existing functionality, update EXAM_STATUS.md and README.md as needed, commit and push the verified milestone with correct Assisted-by attribution, and confirm the push. Give me the running app URL and a short smoke test with expected results. STOP before the next batch.
```

**Repeat 3B** for later batches. A batch can contain several closely related features. Qoder must stop after **each batch**, not after the entire optional queue.

## 3C — A manual test failed (base or any batch)

**When:** If something visibly fails when you use the app.

**Paste, replacing the bracketed details:**

```text
My manual smoke test FAILED: [what I clicked, the input, what happened, and what I expected].

Stop new feature work. Reproduce the failure, inspect the actual error output, determine the root cause and apply the smallest safe fix. Preserve everything that previously worked. Run focused checks and the relevant regression check, then leave the app running and give me an updated short manual test.

Update EXAM_STATUS.md. Safely checkpoint/push corrected work in accordance with AGENTS.md and confirm the status. Do NOT start another batch until I explicitly confirm that this test passes.
```

## 3D — Feature unexpectedly expensive / credits running low

**When:** If Qoder is stuck, repeatedly reading files, overengineering or spending too many credits.

**Paste:**

```text
Stop unnecessary re-analysis, repeated file scanning, dependency installation and unrelated refactoring. Read EXAM_PLAN.md and EXAM_STATUS.md, then inspect only the files relevant to the current task. State what is working, what is failing, and the smallest next change.

Briefly compare the remaining marks for this batch against implementation effort, credit usage, and regression risk. If poor value, recommend skipping it in favour of the next viable batch or the final audit. Do not discard uncommitted changes destructively. Preserve the last verified and pushed version.
```

## 3E — Git checkpoint / push reminder

**When:** Set your **own 45–50 minute alarm**. Use this whenever work has changed or a push hasn't been verified. AI cannot reliably track the passing of an hour unaided.

**Paste:**

```text
Git safety checkpoint now. Check git status, the current branch, remote and last successfully pushed commit. Review changes for secrets and generated files. If there are safe changes, run appropriate quick verification and commit/push the stable work using the AGENTS.md style; if human testing is pending, label any checkpoint as unverified rather than claiming it passed. Report the commit hash, branch, push outcome and any unpushed files. Do not start new feature work during this checkpoint.
```

## 4 — Final audit and submission

**When:** With adequate time remaining (for an 8-hour exam, aim to reserve roughly the final 45–60 minutes; adjust if the official deadline is 6 hours).

**Paste:**

```text
Stop implementing optional features immediately. Follow exam-prompts/04_FINAL_AUDIT_PROMPT.md.

Read the ENTIRE original exam specification and audit the current application against every mandatory, automarked, optional and submission requirement. Mark each PASS, FAIL, MISSING or NOT VERIFIED. Run the relevant builds, tests and actual end-to-end checks. Verify environment configuration, database persistence, README.md and fresh-clone reproducibility where possible.

Fix ONLY submission-critical problems and regressions. If a fix affects user-visible behaviour, provide a short smoke test and wait for my confirmation before treating it as fully verified. Update EXAM_STATUS.md and README.md as needed. Commit and push all safe final changes using the required Assisted-by trailer. Confirm that the correct remote branch contains the latest commit and that git status is clean or explain any remaining files.

Report a concise final audit, what remains unverified, the final remote/branch/commit hash, and the exact final submission action if the lecturer requires one. Do not start new features.
```

## 5 — Last-minute submission emergency

**When:** Time is almost up. Don't let a new feature jeopardise the current submission.

**Paste:**

```text
SUBMISSION PRIORITY NOW. Stop new coding except for a critical blocker. Verify the correct repository and branch, check git status for uncommitted work or secrets, run the shortest essential verification, safely commit/push the latest viable version with the required Assisted-by trailer, and confirm the exact remote commit hash. Report any manual submission step immediately. Do not redesign, refactor or install packages.
```

---

## The five rules to remember

1. **One stage at a time:** first setup, then plan, then base, then one optional batch at a time, then final audit.
2. **Your approval matters:** Qoder pauses for your manual smoke-test approval **before beginning the next major batch**.
3. **Git is independent of approval:** it may commit/push a clearly labelled checkpoint before you approve, but must never mislabel untested work as verified.
4. **Every 45–50 minutes:** independently check the last successful Git push and your Qoder credit balance.
5. **The official brief wins:** if it requires specific frameworks, database, tooling, filenames, or repo structure, those requirements override preferences in `AGENTS.md`.
