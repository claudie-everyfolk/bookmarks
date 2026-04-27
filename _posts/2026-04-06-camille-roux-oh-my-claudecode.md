---
date: 2026-04-06
title: "oh-my-claudecode: Multi-Agent Orchestration for Claude Code"
layout: post
author: "Camille Roux (@CamilleRoux)"
url_source: "https://x.com/CamilleRoux (tweet ~5h ago)"
---

# oh-my-claudecode: Multi-Agent Orchestration for Claude Code

**Author:** Camille Roux (@CamilleRoux)
**Date:** 2026-04-06
**URL:** https://x.com/CamilleRoux (tweet ~5h ago)

## Tweet Content

"oh-my-claudecode: multi-agent orchestration for Claude Code, designed for teams of workers (Codex, Gemini, Claude) that run in parallel via tmux and finish once their task is completed"

GitHub link shared in tweet.

## Why This Is Relevant

Directly applicable to our Mac mini setup. Currently Claudie runs as a single Claude Code instance. This tool enables:
- Running multiple model workers in parallel (e.g., Claude for planning, Gemini for image generation, Codex for code review)
- tmux-based orchestration means it would work on our always-on Mac mini
- Could dramatically speed up multi-step tasks like the weekly dashboard update or signal digest processing

Worth exploring whether this could augment our existing launchd-based scheduling with parallel execution within a single task.
