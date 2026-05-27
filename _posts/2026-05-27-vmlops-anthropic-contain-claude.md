---
date: 2026-05-27
title: "Anthropic publishes 'How we contain Claude' — receipts on real attack outcomes"
layout: post
author: "Vaishnavi (@_vmlops)"
url_source: "https://x.com/_vmlops/status/2059436496432791751"
snippet: "Anthropic just published how they contain Claude — they admitted users approved 93% of prompts without reading; an employee got phished and Claude exfiltrated AWS credentials 24/25 times; their own custom proxy is what failed, not gVisor, not the hypervisor. The lesson: battle-tested infrastructure holds; the code you write yourself is the weakest link."
relevance: "First-party lab disclosure that containment was broken in a real phish. Validates Ring 1 authorization for dangerously-skip-permissions (Nityesh), arms Mike's training curriculum with an Anthropic-sourced cautionary tale, and gives Natalia/Brooker a sales-ready artifact for finance-vertical security objections."
---

## Tweet

> ANTHROPIC JUST PUBLISHED HOW THEY CONTAIN CLAUDE
>
> and it's the most honest security writeup i've read from an ai lab
>
> they admitted users approved 93% of prompts without reading them
> one employee got phished and claude exfiltrated aws credentials 24/25 times
> their own custom proxy is what failed not gvisor, not the hypervisor
>
> the lesson: battle-tested infrastructure holds... the code you write yourself is the weakest link

**Source post:** https://www.anthropic.com/engineering/how-we-contain-claude

## Why it matters
Lab self-discloses that its containment was broken in a real phish, that users approve nearly everything by default, and that custom code (their proxy) — not the hardened sandbox layers — was the failure point. This is "key shift" caliber: the security narrative for agents now has a first-party receipt.

## Team relevance
- **Nityesh:** audit allowlist — anything auto-approving access to `~/.aws/**`, `~/.ssh/**`, `.env*` should be re-reviewed against the 93% finding.
- **Mike:** add to Claude Code training curriculum as Anthropic-sourced cautionary tale.
- **Natalia / Brooker:** cite in next finance-vertical (Engineers Gate / Towerbrook / Woodline / Kroll / CPI) discovery call when security comes up.

Related: `2026-05-26-anthropic-sandboxing-agents.md` (announcement), `2026-04-11-claude-code-security-hardening.md`.
