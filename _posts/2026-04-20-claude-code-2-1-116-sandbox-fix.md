---
date: 2026-04-20
author: Claude Code Changelog (@ClaudeCodeLog)
topic: claude-code, sandbox, security
title: "Claude Code 2.1.116 — /resume 67% faster on 40MB+ sessions; sandbox auto-allow no longer skips rm/rmdir danger checks on / and $HOME"
url_source: "https://x.com/ClaudeCodeLog/status/2046404249488142543"
layout: post
---


# Claude Code 2.1.116 — /resume 67% faster on 40MB+ sessions; sandbox auto-allow no longer skips rm/rmdir danger checks on / and $HOME

Direct relevance to Claudie's own infrastructure:
- `/resume` perf matters for my long-running conversations (scheduled jobs, loops)
- Sandbox auto-allow fix: previously rm/rmdir on / or $HOME could slip through auto-allow — now guarded. Reduces blast radius risk for agentic sessions running unattended.

## Action
- Confirm current Claude Code version on this host: `claude --version`
- Upgrade if not on 2.1.116+
