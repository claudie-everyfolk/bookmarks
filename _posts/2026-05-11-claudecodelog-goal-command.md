---
date: 2026-05-11
title: "Claude Code 2.1.139: /goal command for multi-turn task completion"
layout: post
author: "Claude Code Changelog (@ClaudeCodeLog)"
url_source: "https://x.com/ClaudeCodeLog/status/2053913625983692979"
snippet: "Claude Code 2.1.139: Added /goal command to run tasks across turns until a set completion condition, with live elapsed/turns/tokens. System prompt compaction is now silent."
relevance: "Native multi-turn-until-done primitive may replace Claudie's /loop skill for many jobs. Codex shipped the same primitive simultaneously — vendor convergence."
---

# Claude Code 2.1.139: /goal command for multi-turn task completion

**Author:** Claude Code Changelog (@ClaudeCodeLog)
**Date:** 2026-05-11
**URL:** https://x.com/ClaudeCodeLog/status/2053913625983692979

## Tweet text
"50 CLI changes, 1 system prompt change. Highlights: /goal command to run tasks across turns until a set completion condition, with live elapsed/turns/tokens. System prompt compaction is now silent."

Codex shipped /goal at the same time (Chris Hayduk's "Using Codex Goals Effectively"). Anthropic + OpenAI converged on the same primitive.

## Why it's relevant
Today Claudie's /loop polls on an interval; /goal runs continuously with a completion predicate. Nityesh can evaluate /goal as a drop-in for daily pipeline refresh and dashboard updates. The live elapsed/turns/tokens display is exactly what we hand-rolled. Sign of the wider shift: "set a goal, return when done" is the agent primitive vendors are converging on.
