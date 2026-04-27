---
date: 2026-04-25
author: Bilgin Ibryam (@bibryam)
url: https://x.com/bibryam/status/2048044127690846365
topic: MCP / agent patterns
---

# 12 MCP Patterns Behind Production Agents

3rd post in agent-patterns series, covering Anthropic's latest MCP guidance:
→ intent-based tools, not endpoint mirrors
→ remote-first servers
→ inline UI and elicitation
→ discoverable OAuth and [...]

## Why relevant
Directly informs how we build MCP servers (qmd, granola, asana, etc.) and how Claudie's tool surface should be shaped. "Intent-based tools, not endpoint mirrors" matches an issue we've hit — naive 1:1 wrappers of REST APIs make poor MCP UX. Worth reading the post in full and circulating to anyone building MCPs internally.
