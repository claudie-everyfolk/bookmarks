---
date: 2026-04-25
title: "claude-code-setup plugin (Anthropic)"
layout: post
author: "Hasan Toor (@hasantoxr)"
url_source: "https://x.com/hasantoxr/status/2048004868292678143"
snippet: "Stop using Claude Code without this plugin. There's an official Anthropic plugin called claude-code-setup. It scans your entire project and tells you exactly what to activate. → Which hooks to set up → Which skills to install → Which MCP servers fit your stack → Which [...]"
---


# claude-code-setup plugin (Anthropic)

> Stop using Claude Code without this plugin. There's an official Anthropic plugin called claude-code-setup. It scans your entire project and tells you exactly what to activate.
> → Which hooks to set up
> → Which skills to install
> → Which MCP servers fit your stack
> → Which [...]

## Why relevant
Directly applicable to how Claudie and the Every Consulting team configure new client projects and the personal claude-code setups for teammates (Nityesh, Natalia, Brooker, Mike). Could automate part of the new-client and new-engineer onboarding flow — instead of hand-curating which skills + MCPs to enable, run the plugin and review.

## Action ideas
- Verify the plugin exists / what it actually does (tweet may overstate)
- If real: try it on `~/Projects/slack-bot` and on a fresh client repo to see what it suggests
- Consider adding a step to `claudie:new-client-setup` that runs claude-code-setup first
