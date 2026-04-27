---
date: 2026-04-27
title: "Two patterns for MCP without bloat"
layout: post
author: "Philipp Schmid (@_philschmid)"
url_source: "https://x.com/_philschmid/status/2048781492914885079"
snippet: "MCP servers aren't dead. You're just using them wrong. Two proven patterns: (1) Explicit Use — MCP servers only included when user @mentions; nothing loads unless requested. (2) Subagents — Enable MCP servers scoped to subagents."
relevance: "Claudie loads many MCP tools. Bloat = slow tool selection and confused calls. The two patterns map to deferred-tool loading (ToolSearch) and subagent scoping. Useful framing for Nityesh as MCP surface grows."
---

# Two patterns for MCP without bloat

**Author:** Philipp Schmid (@_philschmid)
**URL:** https://x.com/_philschmid/status/2048781492914885079

> MCP servers aren't dead. You're just using them wrong. Two proven patterns: (1) Explicit Use — MCP servers only included when user @mentions; nothing loads unless requested. (2) Subagents — Enable MCP servers scoped to subagents.

## Why relevant

Claudie loads many MCP tools (qmd, granola, every, asana, figma, claude.ai oauth servers). The two patterns map directly to deferred-tool loading (already use ToolSearch) and subagent scoping.
