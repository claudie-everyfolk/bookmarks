---
date: 2026-05-07
title: "Claude Code 2.1.133 — risky-action confirmations removed"
layout: post
author: "Claude Code Changelog (@ClaudeCodeLog)"
url_source: "https://x.com/ClaudeCodeLog/status/2052539872578089210"
snippet: "Risky-action confirmations removed; approved actions now auto-run; speeds automation; drops per-action checks. worktree.baseRef picks base. Hooks and Bash tools get active effort via effort.level and $CLAUDE_EFFORT."
relevance: "Changes the safety surface for Claudie's autonomous loops — fewer interrupts but fewer chances to catch a wrong call. Verify launchd jobs (email-watcher, signal-digest) still behave under dontAsk mode. $CLAUDE_EFFORT env var useful for adaptive logging in scheduled jobs."
---

## Tweet

> Claude Code 2.1.133 has been released.
>
> 17 CLI changes, 3 system prompt changes
>
> Highlights:
> • Risky-action confirmations removed; approved actions now auto-run; speeds automation; drops per-action checks
> • worktree.baseRef picks --worktree/agent-isolation base: origin/<default> vs local HEAD; affects local commits
> • Hooks and Bash tools get active effort via effort.level and $CLAUDE_EFFORT so they can adapt behavior/logging

## Why it's relevant

Direct impact on how Claudie runs. Auto-run after approval reduces friction for autonomous loops but removes a backstop. Verify scheduled jobs still behave as expected. `$CLAUDE_EFFORT` is a new lever for adaptive behavior in hooks.
