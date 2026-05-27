---
date: 2026-05-27
title: "Anthropic ships first-party security-guidance plugin for Claude Code"
layout: post
author: "Wes Roth (@WesRoth)"
url_source: "https://x.com/WesRoth/status/2059484740588335338"
snippet: "Anthropic released a new security-guidance plugin for Claude Code that helps developers identify and fix vulnerabilities while writing code. The plugin is available to all Claude Code users through the plugin marketplace."
relevance: "Same week as 'How we contain Claude', Anthropic ships the in-flow tool to fix the problem. Direct install for Nityesh on Claudie's own machine, curriculum module for Mike's tech-vertical trainings, and a 'first-party security tooling exists at the agent layer' talking point for Natalia/Brooker on finance discovery calls."
---

## Tweet

> Anthropic released a new security-guidance plugin for Claude Code that helps developers identify and fix vulnerabilities while writing code.
>
> The plugin is available to all Claude Code users through the plugin marketplace.

## Companion: Paweł Huryn's `/security-audit-static`

Paweł noted the Anthropic plugin only guards edits/diffs/commits *going forward* — it doesn't audit the repo you already have. He built `/security-audit-static` to cover that gap.
URL: https://x.com/PawelHuryn/status/2059533995121971605

## Why it matters
First-party security tooling at the developer agent layer, not just the SOC layer (Signal Digest #92 Glasswing). Together with "How we contain Claude," Anthropic shipped the problem statement and the tool to address it in the same week.

## Team relevance
- **Nityesh:** install both. Run Huryn's `/security-audit-static` against `/Users/claudie/Projects/slack-bot` and the `every-consulting` plugin repo — these have never had a static audit. Highest-leverage one-time use.
- **Mike:** add a 20-min "secure-by-default Claude Code" module to the tech curriculum (slots alongside the #96 token-economics module). One slide cites "How we contain Claude" findings; the next demos installing the plugin.
- **Brooker / Natalia:** "Anthropic ships first-party security tooling for the agent layer" is a de-risking point for finance-vertical clients (Engineers Gate, Towerbrook, Woodline, CPI, Kroll).

Related: `2026-05-26-claudedevs-security-guidance-plugin.md`, `2026-04-11-claude-code-security-hardening.md`, Signal Digest #78 / #92.
