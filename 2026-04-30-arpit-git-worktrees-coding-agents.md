
# Why coding agents love Git worktrees (explainer)

**Author:** Arpit Bhayani (@arpit_bhayani)
**URL:** https://x.com/arpit_bhayani/status/2049839926418735585

## Quote
> Coding agents like Claude Code and others love Git worktrees… A Git worktree lets you check out multiple branches of the same repository at the same time, each in its own working directory.

## Why it's relevant
Worktrees are the underlying mechanism for Claude Code's parallel-agent isolation (the `isolation: "worktree"` agent parameter). Most engineers haven't used worktrees in normal Git workflows, so this is a useful primer to bookmark for Mike's tech-vertical training: gives a concrete answer when a client engineer asks "how does the agent not stomp on my branch?"
