# Repository Conventions

## Workspace

- All disposable scripts, logs, debug outputs, and intermediate artifacts must go under `.scratch/<task-slug>/`.
- Do not create ad-hoc temporary directories elsewhere in the repository.
- Promote reusable experiments to `experiments/`, regression tests to `tests/`, and lasting findings to `docs/`.
- Clean up temporary files created by the current task when they are no longer needed. Never delete unrelated or pre-existing files.

## Git Workflow

- Before editing, inspect the current branch, `git status`, and existing changes.
- Use a dedicated `feat/`, `fix/`, or `chore/` branch for each independent task. Preserve unrelated work; use a separate worktree when isolation is needed.
- Commit autonomously after each coherent, verified change. Do not accumulate unrelated changes in one commit.
- Stage only intended files and inspect the staged diff before committing. Never indiscriminately stage unrelated changes.
- Run relevant tests before committing. Report failures and remaining uncommitted changes.
- Never discard user changes, force-push, rewrite shared history, or perform destructive Git operations without explicit authorization.
- Do not push, merge into `main`, or delete branches without authorization.

## Completion

- Report the branch, commits made, verification results, and any remaining worktree changes.
- Prefer leaving the repository clean and the task's temporary workspace free of unnecessary files.