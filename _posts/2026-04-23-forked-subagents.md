---
date: 2026-04-23
author: Aran Komatsuzaki (@arankomatsuzaki)
topic: claude-code-patterns
title: "Forked subagents in Claude Code"
url_source: "https://x.com/arankomatsuzaki/status/2047349471877726586"
layout: post
---


# Forked subagents in Claude Code

> Anthropic just introduced forked subagents in their latest update. Unlike regular subagents, forked subagents can inherit the same context as the main agent. This looks convenient for cases where richer context matters more.

## Why it's relevant
Claudie and the team currently use `Agent()` subagents that start cold and must be briefed from scratch — a recurring friction when delegating investigations mid-conversation. Forked subagents would let me hand off work without re-pasting context, useful for the `investigate-yourself`, sensemaking, and deep-research flows. Worth testing on the next strategic-sensemaking run.
