# Hackathon Exam — Agent Instructions

## Authority and priorities
1. Follow the original exam specification, rubric, automarker, submission rules and permitted tooling above these preferences. If they conflict, flag the conflict.
2. Build a working, reproducible mandatory app first. Then take optional features in approved marks-per-effort batches.
3. Preserve existing functionality, user data, and the last working version. Do not claim a test passed unless it ran.
4. Treat the exam as 6 hours until the official deadline is confirmed; reserve a final submission window.

## Stack and architecture
- Prefer Node.js + Vite + React and simple JavaScript. Use TypeScript only when mandated or it clearly saves effort.
- Choose PostgreSQL only if the brief needs it and the exam environment supports it; otherwise recommend the simplest permitted persistent storage. Never expose database credentials to the browser.
- For persistent server data, use a minimal Node HTTP/Express API as justified. Keep the frontend, API and database wiring simple.
- Prefer standard browser CSS, semantic HTML, accessible labels and straightforward code over unnecessary libraries.
- Before each dependency addition: explain why existing platform features or installed packages are insufficient. No speculative dependencies.
- Use a single package manager, commit its lockfile; never commit node_modules or secrets. Avoid deleting/reinstalling dependencies without cause.
- Set exact scripts, ports, file names and deployment details according to the brief.

## Visual design requirements — apply from the working base
- Build a polished, aesthetically pleasing application with a distinctive **soft pastel** identity, rather than a generic AI-generated dashboard. The official exam specification always overrides these preferences.
- Prefer **sage green, muted teal, warm peach, off-white** and complementary neutrals. Use a consistent palette across navigation, buttons, forms, cards and feedback.
- Suggested **light theme**: canvas `#F7F8F5`, surface `#FFFFFF`, primary text `#25343B`, sage accent `#6C9A91`, peach `#E7C8B5`, border `#DCE5E2`.
- Suggested **dark theme**: canvas `#182327`, surface `#243237`, primary text `#EEF4F2`, accent `#9BC9BC`, secondary text `#BECFC9`. Preserve sufficient contrast in both modes.
- Include a **working light/dark mode toggle** in the initial baseline when allowed and practical. Respect system preference initially and persist the user's choice (e.g. localStorage) when suitable.
- Use a clean, modern, understated editorial/architectural style: structured grids, clear typographic hierarchy, deliberate whitespace, consistent spacing, subtle borders and shadows.
- Avoid heavy glassmorphism, purple gradients, neon, excessive blur, overly rounded components and decorative effects that hurt usability.
- Make the main user journey immediately obvious: consistent navigation, helpful page titles, clear primary actions, semantic and labelled forms, keyboard focus states, and readable error messages.
- Support desktop and smaller screens. Include purposeful empty, loading, success, validation and error states where relevant.
- Use reusable CSS variables/design tokens so styling stays consistent as features are added. Prefer plain CSS and existing dependencies; **do not add a large UI library solely for aesthetics**.
- Incorporate this design in the **first working version** rather than postponing all styling to the end. Functional and marked requirements take priority over decorative polish; avoid repeated redesign during optional batches.

## Workflow and quality gates
- Before coding: read the entire brief, extract mandatory/automarked and optional requirements, choose architecture, and rank optional batches by marks versus incremental effort, dependencies and regression risk. STOP for plan approval.
- Build the smallest complete end-to-end base. Verify installation, startup, main workflow and persistence if relevant. Keep the app running where supported.
- After each milestone: run focused automated checks, give the exact app URL and a 2-5 minute manual smoke test with expected results. STOP for user approval before beginning the next major batch.
- Never treat a successful build as proof the real user workflow works.
- Maintain EXAM_STATUS.md as concise durable state: checked requirements, last verified commit, current batch, commands/URLs, known issues, next action. Update at milestone boundaries, not after every tiny edit.
- Keep README.md accurate for a fresh clone, including setup, environment variables, database and tests.
- As time becomes scarce, freeze optional features and protect achieved marks.

## Git policy
- Initialise and verify Git remote as the first practical task; commit and push the initial scaffold/rules when safe. On lab computers check the exam-assigned repository/branch and Git authentication; never use PATs in model chat, code, commands, Git URLs or committed files.
- At the beginning of each major batch, check the time and commit/hash of the last successful push. Commit and push at each stable, verified milestone and at least once every 60 minutes when changes exist. A model cannot track elapsed real time reliably on its own: prompt the user to set an external 45–50-minute alarm as a backstop. Do not leave all changes unpushed while waiting for a manual test; a clearly labelled checkpoint commit is allowed if automated checks pass but human verification is pending.
- Never knowingly commit broken work as a 'working' milestone. If an unverified checkpoint is needed, label it `chore: checkpoint <scope> (unverified)`.
- Inspect git status and staged changes; exclude secrets, .env, node_modules, build outputs and machine-specific files. Stage targeted files rather than blindly `git add .` when appropriate.
- Commit subject format: `type: concise imperative description`; types: feat, fix, chore, docs, test, style, refactor. No need for refactor when feature work will do.
- Add trailer on separate lines after a blank line: `Assisted-by: Qoder[actual-model-name]`. Use the actual model shown in the interface, not an invented model. List multiple tools if actually used.
- Before beginning the next batch, verify the latest stable milestone is on the correct remote branch. Push and confirm `git status`, remote branch and exit success. On Git failure, alert immediately and fix before doing more large changes.
- Only use force push, destructive clean/reset or history rewrite with explicit approval.

## Credit and time discipline
- Work in one batch at a time; don't repeatedly re-plan the entire repository.
- Read only files needed for the current task after initial orientation. Use concise reports: changed, tested, manual check, blockers, next.
- Prefer focused fixes over rewriting components, and reuse servers/hot reload. Avoid full reinstall, redundant scans and repeated expensive tests.
- Diagnose stuck commands rather than waiting indefinitely. Use local tools for straightforward checks without unnecessary AI dialogue.
- Do not hide failed checks or skip essential verification to conserve credits.
- Do not call additional agents/experts or expensive models unless the task materially needs them.
- Pause for approval at the specified milestones; if the user is absent, secure a verified Git checkpoint and report what remains.
