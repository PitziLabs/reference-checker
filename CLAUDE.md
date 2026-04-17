# Claude Code Guidelines

## Implementation Workflow

When assigned to implement an issue:

1. Read the issue body in full before writing any code or editing any files.
2. Create a working branch scoped to the issue (already handled by the pipeline).
3. Make only the changes required by the issue. Do not clean up adjacent code, refactor unrelated sections, or act on observations outside the issue's scope — open a separate issue instead.
4. Commit with a descriptive message that references the issue number.
5. Push the branch.
6. **Open a pull request as the final step.** Do not stop at "pushed the branch" — the PR is part of the deliverable. PR title should match or clearly refine the issue title. PR body must include `Closes #<number>` so merge closes the issue, plus a short summary of what changed and why. Do not merge the PR yourself; auto-merge is configured and will handle it once checks pass.

## Repository Context

This is a prompt-engineering repository. The primary artifacts are markdown files — prompts, documentation, test sets, and reports. There is no build system, test runner, or package manager to invoke.

When editing prompt files, preserve the existing structure, formatting conventions, and technical voice of the file. Changes to prompts should be grounded in observed behavior or explicit requirements, not speculative improvement.
