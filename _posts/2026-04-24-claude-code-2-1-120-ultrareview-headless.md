---
date: 2026-04-24
author: Claude Code Changelog (@ClaudeCodeLog)
topic: claude-code-release
title: "Claude Code 2.1.120: `claude ultrareview` headless mode"
url_source: "https://x.com/ClaudeCodeLog/status/2047835469962965463"
layout: post
---


# Claude Code 2.1.120: `claude ultrareview` headless mode

## Highlights
- `claude ultrareview` runs /ultrareview headless in CI/scripts and prints findings to stdout
- Automated rule reviewer evaluates classifier rules for clarity, catching ambiguous rules

## Why relevant
Headless ultrareview = we can wire it into PR/branch automation for client-facing scripts (dashboard generators, signal-digest build, etc.). Today /ultrareview is interactive-only; headless means a /schedule cron can review changes and Slack the team if anything looks off. Also useful for QC on the slide-deck-creation pipeline.
