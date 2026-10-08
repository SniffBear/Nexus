---
name: git-github-flow
description: Keep Nexus Git and GitHub changes reviewable through small branches, focused commits, clear pull requests, and verification before merge.
---

# Git and GitHub Flow

Use this skill for repository changes and collaboration workflows.

## Default workflow

1. inspect current branch and working tree
2. understand the requested change
3. make the smallest coherent change
4. verify with relevant tests/checks
5. inspect the diff
6. commit with a focused message
7. summarize verification and remaining risks

## Branch discipline

Do not overwrite unrelated work.

Prefer a dedicated branch for substantial changes.

Never force-push or rewrite history unless explicitly requested.

## Commits

A commit should represent one coherent change.

Avoid:
- unrelated formatting churn
- generated artifacts without need
- huge mixed commits
- vague messages

Good messages describe the change and intent.

## Pull requests

PR descriptions should include:
- what changed
- why
- notable implementation decisions
- tests/checks run
- screenshots for meaningful UI changes
- known limitations
- migration or rollout notes when relevant

## Nexus safety

For financial or agent functionality, explicitly call out:
- permission changes
- execution-path changes
- data-source changes
- audit changes
- live/paper behavior

Never merge a consequential financial workflow without appropriate tests and review.

## Diff review

Before completion inspect:
- changed files
- accidental changes
- secrets
- debug code
- TODOs that alter behavior
- dependency changes
- generated artifacts
