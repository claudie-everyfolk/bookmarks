---
date: 2026-05-20
title: "Claude Managed Agents: self-hosted sandboxes + MCP tunnels"
layout: post
author: "Claude (@claudeai)"
url_source: "https://x.com/claudeai/status/2056645485696315581"
snippet: "Live from Code with Claude London: we're launching self-hosted sandboxes (public beta) and MCP tunnels (research preview) in Claude Managed Agents. Run agents inside your own perimeter, with your security controls applied by default."
relevance: "The enterprise-security answer to Every's biggest client objection — 'we can't run autonomous agents on our data.' Self-hosted sandboxes run agents inside the client's own perimeter with their controls by default; MCP tunnels expose internal tools without opening the perimeter. Unblocks finance and enterprise adoption conversations."
---

# Claude Managed Agents: self-hosted sandboxes + MCP tunnels

**Author:** Claude (@claudeai), reposted by Boris Cherny
**URL:** https://x.com/claudeai/status/2056645485696315581

> Live from Code with Claude London: we're launching self-hosted sandboxes (public beta) and MCP tunnels (research preview) in Claude Managed Agents. Run agents inside your own perimeter, with your security controls applied by default.

## Why it's relevant

This is the enterprise-security answer to the biggest objection Every hears in client engagements: "we can't run autonomous agents on our data." Self-hosted sandboxes let Claude Managed Agents run inside the client's own network perimeter with their security controls applied by default; MCP tunnels expose internal tools to agents without opening the perimeter.

For Every Consulting this matters two ways:

- **Client advisory** — finance and enterprise clients (hedge funds, PE firms, Bloomberg-tier) cite data-perimeter and compliance constraints as the blocker to agent adoption. "Agents inside your own perimeter, your controls by default" is the line that unblocks those conversations. It pairs directly with the existing Signal Digest thread on Claude Managed Agents (#32, #42, #54, #67, #81).
- **Claudie's own infrastructure** — Claudie already runs a self-hosted agent fleet (20 launchd jobs on a Mac mini). MCP tunnels are the sanctioned pattern for letting cloud-hosted Routines reach local tools — relevant to any future Routines-vs-launchd evaluation Nityesh runs.

Not a vulnerability — this is a defensive/governance capability.
