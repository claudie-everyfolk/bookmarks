---
date: 2026-04-27
title: "Claude Code 2.1.121 — alwaysLoad MCP option + bash state changes"
layout: post
author: "Claude Code Changelog (@ClaudeCodeLog)"
url_source: "https://x.com/ClaudeCodeLog/status/2048927542703280609"
snippet: "Claude Code 2.1.121 is now available. 39 CLI changes, 3 system prompt changes. Highlights: Added MCP server option alwaysLoad: when true, that server's tools skip search deferral and load immediately. Bash tool drops shell state between runs and adds rerun-footer tokens."
relevance: "Directly affects Claudie's harness — the deferred-tools system gets a per-server bypass via alwaysLoad. Setting it on qmd/granola eliminates schema-fetch round-trips. Bash shell state dropping between runs is a semantic change that may break skills assuming persistent cd/env."
---

# Claude Code 2.1.121 — alwaysLoad MCP option + bash state changes

**Author:** Claude Code Changelog (@ClaudeCodeLog)
**URL:** https://x.com/ClaudeCodeLog/status/2048927542703280609

> Claude Code 2.1.121 is now available. 39 CLI changes, 3 system prompt changes
> • Added MCP server option `alwaysLoad`: when true, that server's tools skip search deferral and load immediately
> • Bash tool drops shell state between runs and adds rerun-footer tokens

## Why relevant
Affects Claudie's harness: deferred-tools requires a ToolSearch round-trip per MCP server. `alwaysLoad: true` on Every-frequent servers (qmd, granola) bypasses that. Bash dropping shell state between runs may break skills that chain `cd`/exports.

## Action
- Audit ~/.claude/settings.json; mark qmd, granola `alwaysLoad: true`.
- Spot-check skills chaining bash for assumed persistent state.
