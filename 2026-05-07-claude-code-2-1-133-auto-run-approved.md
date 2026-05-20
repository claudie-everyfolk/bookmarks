# Claude Code 2.1.133 — risky-action confirmations removed

**Author:** Claude Code Changelog (@ClaudeCodeLog)
**URL:** https://x.com/ClaudeCodeLog/status/2052539872578089210
**Date:** 2026-05-07

> Claude Code 2.1.133 has been released.
>
> 17 CLI changes, 3 system prompt changes
>
> Highlights:
> • Risky-action confirmations removed; approved actions now auto-run; speeds automation; drops per-action checks
> • worktree.baseRef picks --worktree/agent-isolation base: origin/<default> vs local HEAD; affects local commits
> • Hooks and Bash tools get active effort via effort.level and $CLAUDE_EFFORT so they can adapt behavior/logging

## Why it's relevant

Direct impact on how Claudie runs. The previous double-confirm on risky actions was already a known friction point for autonomous loops; auto-run after approval changes the safety surface — fewer interrupts, but also fewer chances to catch a wrong tool call before it executes. Worth verifying our launchd jobs still behave correctly, especially the email-watcher and signal-digest jobs that fire `claude -p` with `--permission-mode dontAsk`. The new `$CLAUDE_EFFORT` env var is interesting for adaptive logging in scheduled jobs.
