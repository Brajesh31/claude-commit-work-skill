---
name: commit-work
description: Prepare safe, logically scoped Git commits by reviewing intended changes, staging selected files, and writing Conventional Commit messages. Use when asked to stage, split, or commit work.
---

# Commit Work

Create reviewable commits that contain only intended changes and explain both what changed and why.

## Workflow

1. Inspect the working tree with `git status --short`, `git diff`, `git diff --cached`, and `git diff --stat`. Review untracked files separately.
2. Split unrelated changes by logical responsibility, keeping tightly coupled changes together when separation would make a commit incomplete.
3. Stage deliberately using explicit paths or `git add -p`. Never stage secrets, local configuration, generated output, or unrelated edits.
4. Review the staged diff with `git diff --cached` and `git diff --cached --check`. Confirm it matches the planned commit.
5. Run the smallest meaningful test or check available.
6. Write a Conventional Commit message:

```text
type(scope): short imperative summary

Explain the reason for the change and important context.
```

7. Present the staged file list and message. Obtain confirmation unless the user has already authorized committing.
8. Verify with `git log -1 --oneline` and `git status --short`. Repeat for each logical group.

Use `references/commit-message-template.md` when helpful.

## Safety

Do not commit credentials, tokens, private keys, or sensitive local data. Do not discard user changes. Do not amend, rebase, reset, force-push, or publish without explicit permission. Report skipped checks and remaining uncommitted changes.

## Deliverables

Provide each commit hash and message, included files, checks run, and remaining worktree status.
