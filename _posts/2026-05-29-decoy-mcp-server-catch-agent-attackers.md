---
date: 2026-05-29
title: "Build a Decoy MCP Server to Catch AI Agent Attackers"
layout: post
author: "Lenny Zeltser (@lennyzeltser)"
url_source: "https://x.com/lennyzeltser/status/2060085225515082226"
snippet: "AI agent MCP configs are plain-text files at known paths, offering an index of high-value services. A decoy entry pointing to a honeypot MCP server alerts you of an intrusion."
relevance: "A cheap defensive tripwire. MCP config files are plain-text maps of an agent's integrations — the first thing an attacker reads on a dev machine. Claudie's always-on Mac mini runs several MCP servers plus Natalia's Workspace MCP; a honeypot entry would fire on the recon stage. Good client security-module material."
---

# Build a Decoy MCP Server to Catch AI Agent Attackers

**Author:** Lenny Zeltser (@lennyzeltser)
**Tweet:** https://x.com/lennyzeltser/status/2060085225515082226
**Source:** https://zeltser.com

## Tweet

> An attacker on a developer's machine often pivots to reconnaissance. AI agent MCP configs are plain-text files at known paths, offering an index of high-value services. A decoy entry pointing to a honeypot MCP server alerts you of an intrusion.

## Why it's relevant

Defensive, not offensive. MCP config files (`.mcp.json`, `~/.claude.json`) are plain-text maps of an agent's high-value integrations — exactly what an attacker reads first. Claudie's always-on Mac mini runs MCP servers (qmd, Granola, Figma, Notion, Every) plus a Workspace MCP on Natalia's account. A decoy MCP entry pointing at a honeypot is a cheap, high-signal intrusion tripwire — and clean material for client security modules, since most teams adopting MCP have zero detection on those files. Flag to Nityesh for host hardening.
