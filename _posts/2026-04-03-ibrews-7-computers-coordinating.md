---
date: 2026-04-03
title: "7 Computers Coordinating via Git with Claude Code"
layout: post
author: "Alex Coulombe (@iBrews)"
url_source: "https://x.com/iBrews/status/2040152159350644947"
snippet: "I gave 7 computers Claude Code and told them to coordinate through git.  They built their own dashboard, dispatch tasks to each other via SSH, and send me Telegram updates when they're done.  No orchestration framework. No central server. Just markdown inboxes and 3 hooks."
relevance: "This is essentially a multi-machine version of how Claudie is set up — a Claude Code agent running on a Mac mini, coordinating through files, using hooks for automation, and messaging the team when work is done. The key insight is that you don't need a complex orchestration framework. Markdown inboxes + git + hooks is sufficient for multi-agent coordination. This validates our architecture and suggests scaling paths. ---"
---
# 7 Computers Coordinating via Git with Claude Code

**Author:** Alex Coulombe (@iBrews)
**URL:** https://x.com/iBrews/status/2040152159350644947
**Date:** 2026-04-03

## Tweet

> I gave 7 computers Claude Code and told them to coordinate through git.
>
> They built their own dashboard, dispatch tasks to each other via SSH, and send me Telegram updates when they're done.
>
> No orchestration framework. No central server. Just markdown inboxes and 3 hooks.

## Why it's relevant

This is essentially a multi-machine version of how Claudie is set up — a Claude Code agent running on a Mac mini, coordinating through files, using hooks for automation, and messaging the team when work is done. The key insight is that you don't need a complex orchestration framework. Markdown inboxes + git + hooks is sufficient for multi-agent coordination. This validates our architecture and suggests scaling paths.

---

## Detailed Relevance Report

### 1. Team Relevance

**Nityesh (highest relevance)** — This tweet describes almost exactly the architecture he built for Claudie, but scaled to 7 machines. Claudie already runs on a dedicated Mac mini, uses git for config sync (repo-watcher pulling `nityeshaga/claude-home-base` every 30 min), coordinates through files (markdown memory, bookmarks, teammate profiles), and uses hooks/launchd for automation. The iBrews pattern is the natural next step: multiple Claudie-class nodes coordinating through the same primitives Nityesh already understands. The "markdown inboxes" concept maps directly to Claudie's `~/bookmarks/`, `~/work/`, and memory file system. The "3 hooks" maps to Claudie's launchd + shell script two-file pattern.

**Mike Taylor (high relevance)** — Mike teaches AI coding workflows and developer productivity. This is a concrete, teachable multi-agent pattern that requires zero proprietary frameworks. The stack is entirely things he already covers: git, SSH, Claude Code, markdown, hooks. Strong candidate for an advanced module in tech bootcamps — "multi-agent coordination without frameworks."

**Natalia (medium relevance)** — Validates the architecture behind Claudie at a higher scale, strengthening the consulting pitch: "We didn't just build one agent — the same patterns work for a fleet." Natalia's own tweet about the 100h-to-7h compression sets up this exact narrative.

### 2. Connections to Existing Work

- Claudie's architecture is a single-node version of this pattern (Mac mini, git sync, markdown state, launchd hooks, Slack notifications)
- Related bookmarks: dennizor tmux multi-agent, imbue mngr parallel sessions, ivan burazin multi-agent OSS, dispatch permission mode, simonw dark factory
- Key differentiator: No orchestration framework, no central server. Peer-to-peer via git + markdown. Closest external validation of Claudie's exact architecture philosophy.

### 3. Concrete Actions

- **Scale Claudie:** Set up a second Mac mini with a specialized role, coordinating through the existing git repo using markdown task files as an inbox
- **Teach in bootcamps:** Create an advanced Claude Code module — "Multi-agent coordination with git + markdown + hooks." No frameworks to install, most teachable multi-agent pattern available
- **Consulting pitch:** "We built a chief of staff agent on a Mac mini using markdown files, git, and hooks. The same pattern scales to 7 machines with zero additional infrastructure."
- **Hook system:** Investigate whether Claude Code's native hooks could replace some launchd jobs for event-driven triggers
