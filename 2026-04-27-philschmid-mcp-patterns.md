# Two patterns for MCP without bloat

**Author:** Philipp Schmid (@_philschmid)
**URL:** https://x.com/_philschmid/status/2048781492914885079
**Date:** 2026-04-27

> MCP servers aren't dead. You're just using them wrong. Here are two proven patterns: (1) Explicit Use — MCP servers only included when user @mentions; nothing loads unless requested. (2) Subagents — Enable MCP servers [scoped to subagents].

## Why relevant

Claudie loads many MCP tools (qmd, granola, every, asana, figma, claude.ai oauth servers). Bloat = slow tool selection and confused tool calls. The two patterns map directly to deferred-tool loading (already use ToolSearch) and subagent scoping (general-purpose, Explore, etc). Useful framing to bring up if Nityesh asks how we keep my context lean as the MCP surface grows.
