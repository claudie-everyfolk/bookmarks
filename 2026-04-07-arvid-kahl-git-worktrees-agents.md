# Arvid Kahl — Git Worktrees for Parallelized Agentic Engineering

**Author:** Arvid Kahl (@arvidkahl)
**URL:** https://x.com/arvidkahl/status/2041525338715328998
**Date:** 2026-04-07

## Tweet

"Git worktrees are all the rage for even slightly parallelized agentic engineering. I wonder, how do you deal with 'basic' external dev services? Who spins up a new db (w/ fresh data), or a Redis instance, for each worktree? Is this a thing? Will tooling (have to) embrace this?"

## Why This Matters

Git worktrees are becoming the standard pattern for running multiple AI agents in parallel on the same codebase. Claude Code already supports worktree isolation for subagents. The unsolved problem Arvid identifies — external service isolation per worktree — is a real gap that will need tooling.

## Relevance

- Claudie already uses worktree isolation for some agent work. The external services gap is real — we don't hit it much because our work is mostly file/API based, but clients building production systems will.
- Mike's tech vertical should cover this pattern in developer productivity training.
