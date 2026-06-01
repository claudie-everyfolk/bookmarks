---
date: 2026-06-01
title: "Opus 4.8 effort levels: high vs xhigh — 4x cost buys 2 quality points"
layout: post
author: "Mnimiy (@Mnilax)"
url_source: "https://x.com/Mnilax/status/2061155693692957142"
snippet: "The official move with Opus 4.8 is hand off the long task and walk away. I tested all 4 effort levels on Opus 4.8. Past high, 4x cost buys two quality points. Opus 4.8 made high the default and added xhigh above it. Long autonomous work is where xhigh earns its cost."
relevance: "Direct guidance on how Claudie should pick effort levels for scheduled/autonomous jobs. xhigh is worth 4x cost only for long-horizon hand-off-and-walk-away work; for most jobs high is the right default. Informs how Nityesh tunes Claudie's launchd jobs and reinforces the 'token-intensive jobs off-peak' guidance in CLAUDE.md."
---

# Opus 4.8 effort levels: high vs xhigh — 4x cost buys 2 quality points

## Tweet

> The official move with Opus 4.8 is hand off the long task and walk away. I tested all 4 effort levels on Opus 4.8. Past high, 4x cost buys two quality points. Opus 4.8 made high the default and added xhigh above it. Long autonomous work is where xhigh earns its cost.

## Why it's relevant

Direct guidance on how Claudie should pick effort levels for scheduled/autonomous jobs. xhigh is worth 4x cost only for long-horizon hand-off-and-walk-away work; for most jobs high is the right default. Informs how Nityesh tunes Claudie's launchd jobs and reinforces the 'token-intensive jobs off-peak' guidance in CLAUDE.md.

## Concrete takeaways

- **Default to high** for routine scheduled jobs (X browsing, digest builds, dashboard refreshes). xhigh's marginal quality gain doesn't justify 4x token cost on bounded tasks.
- **Reserve xhigh** for genuine long-horizon autonomous work where you hand off and walk away — multi-step migrations, deep research, complex builds.
- Maps to Nityesh's recent work converting token-hungry skills to dynamic workflows (5x fewer output tokens). Effort-level selection is the other half of that cost lever.
