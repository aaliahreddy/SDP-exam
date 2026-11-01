# Qoder exam kit — quick start

## Tonight
1. Create a **private preparation repository** or keep this ZIP ready for the lecturer-permitted Moodle upload. Do not assume the exam permits prewritten files without checking.
2. Upload AGENTS.md, .gitignore, and the six files in exam-prompts/ (the setup guide, first-message template, and four numbered stage prompts). No code or dependencies are needed in preparation.
3. Confirm you can access GitHub and Qoder accounts from the lab; have a second-factor method available.

## On the lab computer
1. Read the exam's rules and determine whether an assigned repository, template, branch, or Moodle submission is required. Use those rules, not the practice repository, for the real exam.
2. Open the **actual exam repository** in Qoder. If permitted, copy these instructions into its root. Do not put the brief, secret keys, tokens, or restricted content in a public repo.
3. Confirm Node/npm, Git and suitable database are available. Test Git authentication and the right remote immediately.
4. Attach the official brief; paste the first-message template from `exam-prompts/00_INITIAL_QODER_MESSAGE.md`. Approve plan, then use `02_BASE_PROMPT.md`, `03_BATCH_PROMPT.md`, `04_FINAL_AUDIT_PROMPT.md` in sequence.
5. Verify the live app yourself and verify remote pushes regularly.

## GitHub authentication on shared lab PCs
Try `gh auth login` (GitHub.com > HTTPS > browser), if GitHub CLI is installed and allowed. Otherwise HTTPS Git may request a personal access token as password. A fine-grained PAT with only required repository Contents: Read/write is a reasonable fallback, but tokens restricted to your own repositories may not work for an assigned organisation repository. Never paste a PAT into Qoder, code, the shell command line, or the remote URL. Avoid credential persistence on shared devices; revoke an exam-only PAT after the exam, sign out of browser and Qoder, and clear credentials according to lab policy.

## Do not confuse the repositories
Preparation repo = storage for these permitted files. Actual exam repo = the one specified by your lecturer and marked for submission.
