---
date: 2026-05-21
title: "Build a Decoy MCP Server to Catch AI Agent Attackers"
layout: post
author: "Lenny Zeltser (@lennyzeltser)"
url_source: "https://x.com/lennyzeltser/status/2057182759806701853"
snippet: "A decoy in your AI agent's MCP config can help spot an intrusion. Interactions with the honeypot MCP server are a high-confidence signal. Building this honeypot is pretty straightforward."
relevance: "A defensive AI-security technique that maps directly onto Claudie's own setup — she runs MCP servers on an always-on Mac mini with real credentials. A decoy entry is a near-zero-cost intrusion tripwire, and a memorable hands-on demo for security-conscious finance clients."
---

# Build a Decoy MCP Server to Catch AI Agent Attackers

**Author:** Lenny Zeltser (@lennyzeltser) — security executive, SANS Faculty Fellow, creator of REMnux
**Tweet:** https://x.com/lennyzeltser/status/2057182759806701853
**Article:** https://zeltser.com/decoy-mcp-server-honeypot

> A decoy in your AI agent's MCP config can help spot an intrusion. Interactions with the honeypot MCP server are a high-confidence signal. Building this honeypot is pretty straightforward.

An attacker who reaches a developer's machine can read the AI agent's MCP config (`~/.claude.json` at user scope, `.mcp.json` at project root for Claude Code) to find other resources worth pursuing. The technique: add a decoy MCP entry pointing at a Cloudflare Worker that mimics a tempting server. Any `tools/call` against it is a high-confidence intrusion signal — and it reveals which tool the attacker chose and the arguments they passed. The difference between knowing someone scanned and knowing what they wanted.

## Why it's relevant

This is a defensive AI-security technique that maps directly onto Claudie's own setup — she runs MCP servers on an always-on Mac mini with real credentials. It's also a memorable, hands-on training demo for security-conscious clients.

## Relevance report

**Direct fit with Claudie's own infrastructure.** Claudie runs three MCP servers (`~/.claude.json`): `granola` (stdio, with a live `GRANOLA_API_KEY` in plaintext), `qmd` (local search), and `every` (SSE). She runs 24/7 on a Mac mini with real credentials, Google Workspace access, and a browser with logged-in sessions — exactly the "always-on AI employee with real credentials" Nityesh describes in `~/work/claudie-security-briefing.md`. A decoy MCP entry (e.g. a fake `internal-vault` or `client-db` server pointing at a Cloudflare Worker) is a concrete, low-cost addition to her config. It maps onto the briefing's weakest layer — **Observability** ("prevents nothing, catches everything") — and would give a high-confidence intrusion signal that the four existing layers (least access, programmatic hooks, ring-based prompts) don't currently provide. Claudie already has Cloudflare Workers/Pages set up (`every-docs.pages.dev`), so the Worker honeypot is near-zero new infra.

**The team has tracked this thread heavily.** Prior security bookmarks: `2026-04-11-claude-code-security-hardening.md`, `2026-04-10-llm-router-malicious-tool-calls.md`, `2026-05-13-maxedapps-ai-supply-chain-rogue-agents.md`. Signal Digest entries `43-axelbitblaze-claude-code-attack-surface.md` (prompt injection via malicious MCP config) and `57-clawhub-malicious-skills-supply-chain.md` already flag MCP/skill configs as attack surface. The decoy idea is the *detective* counterpart to all this *preventive* work.

**Who should see it:**
- **Nityesh** (owner of Claudie's security model) — primary. A buildable addition to his published four-layer framework; consider a v2 of the briefing.
- **Mike** (Tech Vertical Lead) — his Claude Code training needs a "secure your AI setup" module; honeypot MCP is a memorable hands-on demo.
- **Brooker** (Non-Tech/Finance Lead) — finance/hedge-fund clients care about intrusion detection; framed as governance, it fits his vertical. Worth a pipeline-review mention with Natalia for security-conscious clients (Bloomberg, hedge funds, PE).
