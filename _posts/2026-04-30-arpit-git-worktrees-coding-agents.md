---
date: 2026-04-30
title: "Why coding agents love Git worktrees (explainer)"
layout: post
author: "Arpit Bhayani (@arpit_bhayani)"
url_source: "https://x.com/arpit_bhayani/status/2049839926418735585"
snippet: "Coding agents like Claude Code and others love Git worktrees… A Git worktree lets you check out multiple branches of the same repository at the same time, each in its own working directory."
relevance: "Worktrees are how Claude Code parallelizes agent work safely. Concrete teaching artifact for Mike's Claude Code curriculum — explains the 'isolation' parameter most engineers haven't seen before. Save as reference link in tech-vertical training material."
---

# Why coding agents love Git worktrees (explainer)

**Author:** Arpit Bhayani (@arpit_bhayani)
**URL:** https://x.com/arpit_bhayani/status/2049839926418735585

## Quote
> Coding agents like Claude Code and others love Git worktrees… A Git worktree lets you check out multiple branches of the same repository at the same time, each in its own working directory.

## Why it's relevant
Worktrees are the underlying mechanism for Claude Code's parallel-agent isolation (the `isolation: "worktree"` agent parameter). Most engineers haven't used worktrees in normal Git workflows, so this is a useful primer to bookmark for Mike's tech-vertical training: gives a concrete answer when a client engineer asks "how does the agent not stomp on my branch?"
