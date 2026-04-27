---
date: 2026-04-12
title: "Evo — Open-Source Claude Code Plugin for Autoresearch"
layout: post
author: "Alok Bishoyi (@alokbishoyi97)"
url_source: "https://x.com/alokbishoyi97/status/2043251378374557824"
snippet: "Shipped evo today — an open source Claude Code plugin that optimizes code through experiments. You hand it a codebase. It finds a benchmark, runs the baseline, then fires off parallel agents to try to beat it. Kept if better, discarded if worse. Inspired by @karpathy's autoresearch: - Tree search over greedy hill-climb — multiple forks from any committed node..."
relevance: "A Claude Code plugin that uses parallel agents + git worktrees to iteratively optimize code. The \"shared failure traces\" pattern — agents learning from each other's mistakes — is a concrete implementation of the memory-across-agents idea. The worktree-based isolation is the same pattern Claude Code uses natively for agent isolation. Worth evaluating for our own workflow optimization and as a reference for Mike's tech vertical training on advanced Claude Code..."
---
# Evo — Open-Source Claude Code Plugin for Autoresearch

**Author:** Alok Bishoyi (@alokbishoyi97)
**URL:** https://x.com/alokbishoyi97/status/2043251378374557824
**Date:** 2026-04-12

## Tweet

> Shipped evo today — an open source Claude Code plugin that optimizes code through experiments.
>
> You hand it a codebase. It finds a benchmark, runs the baseline, then fires off parallel agents to try to beat it. Kept if better, discarded if worse.
>
> Inspired by @karpathy's autoresearch:
> - Tree search over greedy hill-climb — multiple forks from any committed node
> - N parallel agents in git worktrees
> - Shared failure traces so agents don't repeat each other's mistakes
> - Regression gates

## Why it's relevant

A Claude Code plugin that uses parallel agents + git worktrees to iteratively optimize code. The "shared failure traces" pattern — agents learning from each other's mistakes — is a concrete implementation of the memory-across-agents idea. The worktree-based isolation is the same pattern Claude Code uses natively for agent isolation.

Worth evaluating for our own workflow optimization and as a reference for Mike's tech vertical training on advanced Claude Code patterns.
