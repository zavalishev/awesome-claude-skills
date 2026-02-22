---
name: git-cleanup
description: "Safely analyzes and cleans up local git branches and worktrees by categorizing them as merged, squash-merged, superseded, or active work."
disable-model-invocation: true
allowed-tools:
  - Bash
  - Read
  - Grep
  - AskUserQuestion
---

# Git Cleanup

Safely clean up accumulated git worktrees and local branches by categorizing them into: safely deletable (merged), potentially related (similar themes), and active work (keep).

## When to Use

- When the user has accumulated many local branches and worktrees
- When branches have been merged but not cleaned up locally
- When remote branches have been deleted but local tracking branches remain

## When NOT to Use

- Do not use for remote branch management (this is local cleanup only)
- Do not use for repository maintenance tasks like gc or prune
- Not designed for headless or non-interactive automation (requires user confirmations at two gates)

## Core Principle: SAFETY FIRST

**Never delete anything without explicit user confirmation.** This skill uses a gated workflow where users must approve each step before any destructive action.

(Полное содержимое см. выше - сокращено для краткости)