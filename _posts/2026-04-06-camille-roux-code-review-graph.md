---
date: 2026-04-06
title: "code-review-graph: 6.8x Fewer Tokens in Code Review"
layout: post
author: "Camille Roux (@CamilleRoux)"
url_source: "https://x.com/CamilleRoux (tweet ~2h ago)"
---

# code-review-graph: 6.8x Fewer Tokens in Code Review

**Author:** Camille Roux (@CamilleRoux)
**Date:** 2026-04-06
**URL:** https://x.com/CamilleRoux (tweet ~2h ago)
**GitHub:** github.com/tirth8205/code... (referenced in tweet)

## Tweet Content

"code-review-graph builds a graph of your codebase so Claude only reads the files actually impacted by a change — 6.8x fewer tokens in review, up to 49% on daily code tasks."

Includes a diagram showing "The Token Problem" — without the graph, Claude reads entire codebases; with it, only affected files are loaded.

## Why This Is Relevant

Token efficiency is a real constraint for us on Claude Max. This approach could:
- Reduce costs on our scheduled jobs that touch code repos
- Speed up code review tasks for Mike's tech vertical training
- Apply to how we structure Claudie's own codebase awareness — instead of reading everything, build a dependency graph

The underlying pattern (dependency-aware context loading) is the same idea as "scoped context" from the 12 Agentic Harness Patterns post.
