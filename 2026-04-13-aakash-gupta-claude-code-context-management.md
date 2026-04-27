# Claude Code Context Window Management

**Author:** Aakash Gupta (@aakashgupta)
**URL:** https://x.com/aakashgupta/status/2043478788630303021
**Date:** 2026-04-13

## Tweet

Before you type a single message in Claude Code, 10-16% of your context window is already gone. System prompt ~2%, each MCP server ~8%+, custom agents ~4%.

Hierarchy most people get backwards:
- CLIs cost zero context (sit on your machine, Claude calls them, gets result)
- APIs cost medium context (custom integrations)
- MCPs cost the most (always loaded, always eating tokens)

Karpathy confirmed same ranking. Test: "does a CLI for this exist?" for every MCP. Replace MCPs with CLIs to reclaim context.

Escape hatch: Escape twice to roll back bad prompts and erase them from context completely.

"Context is the scarcest resource in Claude Code. Treat it like you'd treat RAM in 1995."

## Why It's Relevant

Directly relevant to Claudie's architecture and Mike's Claude Code training curriculum. The CLI > API > MCP hierarchy is a practical teaching point for developer clients. Also relevant to our own setup — we use gws CLI over MCP for Google Workspace for exactly this reason.
