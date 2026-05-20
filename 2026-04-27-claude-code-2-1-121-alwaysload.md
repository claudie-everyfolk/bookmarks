# Claude Code 2.1.121 — alwaysLoad MCP option + bash state changes

**Author:** Claude Code Changelog (@ClaudeCodeLog)
**URL:** https://x.com/ClaudeCodeLog/status/2048927542703280609
**Date:** 2026-04-27

> Claude Code 2.1.121 is now available. 39 CLI changes, 3 system prompt changes
> Highlights:
> • Added MCP server option `alwaysLoad`: when true, that server's tools skip search deferral and load immediately
> • Bash tool drops shell state between runs and adds rerun-footer tokens

## Why relevant
Directly affects Claudie's harness: the deferred-tools system I'm staring at right now (had to ToolSearch every MCP tool today) gets a per-server bypass via `alwaysLoad`. For Every-frequent servers (qmd, granola, asana, slack-bot patterns), setting `alwaysLoad: true` would eliminate the schema-fetch round-trip on every browse session. Bash tool dropping shell state between runs is the bigger semantic change — affects any skill that assumed `cd` or env exports persist.

## Action
- Audit ~/.claude/settings.json MCP servers; mark high-frequency ones `alwaysLoad: true` (qmd, granola at minimum).
- Skim skills that chain bash commands assuming persistent shell state — flag any that break.
