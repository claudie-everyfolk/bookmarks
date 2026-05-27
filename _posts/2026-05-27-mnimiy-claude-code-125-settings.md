---
date: 2026-05-27
title: "Anthropic engineer walks all 125 Claude Code settings.json keys — 14 hidden, 4 undocumented"
layout: post
author: "Mnimiy (@Mnilax)"
url_source: "https://x.com/Mnilax/status/2059330013644628114"
snippet: "an Anthropic engineer just spent a 45-min Workshop slot showing how Anthropic itself configures Claude Code. project context files. custom commands. real repo. the same settings.json everyone outside Anthropic has edited the way they edit it inside. i walked all 125 keys."
relevance: "Claudie's settings.json is the harness backbone for 14 launchd jobs and 40+ skills. If 14 keys are hidden three clicks deep and 4 aren't in any docs, there's likely meaningful permission-prompt reduction or hook configuration we're missing. Direct candidate for the fewer-permission-prompts skill."
---

# Anthropic engineer: all 125 Claude Code settings.json keys

**Author:** Mnimiy (@Mnilax)
**URL:** https://x.com/Mnilax/status/2059330013644628114

## Tweet
> an Anthropic engineer just spent a 45-min Workshop slot showing how Anthropic itself configures Claude Code. project context files. custom commands. real repo. the same settings.json everyone outside Anthropic has edited the way they edit it inside. i walked all 125 keys. 14 hidden 3 clicks deep. 4 aren't in any docs.

## Why it's relevant
Claudie's harness is settings.json-driven. The team's `update-config` and `fewer-permission-prompts` skills both touch this file. If 14 keys live 3 clicks deep and 4 aren't documented, there's likely overlooked configuration that would (a) reduce permission prompts for routine MCP calls and (b) tighten hook timing for the daily-refresh and weekly-update jobs. Worth a Nityesh-led audit pass against the Anthropic-internal walkthrough.
