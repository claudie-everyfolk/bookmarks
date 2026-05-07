---
date: 2026-05-07
title: "Claude Code 2.1.132 — CLAUDE_CODE_SESSION_ID for hooks, alternate-screen disable"
layout: post
author: "Claude Code Changelog (@ClaudeCodeLog)"
url_source: "https://x.com/ClaudeCodeLog/status/2052152053628035088"
snippet: "Bash subprocesses now get CLAUDE_CODE_SESSION_ID matching hook session_id, enabling tool-level session tracing. Added CLAUDE_CODE_DISABLE_ALTERNATE_SCREEN=1 to disable fullscreen."
relevance: "Lets Claudie correlate launchd job runs end-to-end across Bash subprocesses. Useful for email-watcher, signal-digest, qmd-reindex observability. Stamp CLAUDE_CODE_SESSION_ID in log lines next time we touch the wrappers."
---

# Claude Code 2.1.132 — CLAUDE_CODE_SESSION_ID for hooks, alternate-screen disable

**Author:** Claude Code Changelog (@ClaudeCodeLog), automated by @marc_krenn
**Date:** 2026-05-06
**URL:** https://x.com/ClaudeCodeLog/status/2052152053628035088

> Claude Code 2.1.132 has been released. 28 CLI changes, 2 system prompt changes
> Highlights:
> • Bash subprocesses now get CLAUDE_CODE_SESSION_ID matching hook session_id, enabling tool-level session tracing
> • Added CLAUDE_CODE_DISABLE_ALTERNATE_SCREEN=1 to disable fullscreen

## Why it's relevant
Direct ops impact for Claudie's infrastructure:

- **CLAUDE_CODE_SESSION_ID in Bash subprocesses** = we can finally correlate launchd job runs end-to-end. Right now `~/scripts/*.sh` wrappers log start/done timestamps but can't easily tie individual tool calls back to a specific session. With session_id propagating into Bash, we can build cleaner observability — useful for the email-watcher, signal-digest, and qmd-reindex jobs.
- **Disable alternate screen** = small, but useful when running `claude -p` and tee-ing output to a log without ANSI fullscreen artifacts.

Action: when next touching `~/scripts/email-watcher.py` or any wrapper, consider stamping `CLAUDE_CODE_SESSION_ID` into log lines for correlation.
