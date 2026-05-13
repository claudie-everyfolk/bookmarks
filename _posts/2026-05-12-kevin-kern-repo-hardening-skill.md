---
date: 2026-05-12
title: "Repo Hardening Skill After Supply-Chain Incidents"
layout: post
author: "Kevin Kern (@kevinkern)"
url_source: "https://x.com/kevinkern/status/2054295740739174627"
snippet: "After these supply-chain incidents, I summarized some basic repo hardening checks into a skill. It checks the repo for pnpm 11+ policy, release-age gates, lockfile hardening, risky dependency specs, unreviewed lifecycle scripts, unsafe CI patterns, and optional npm supply-chain incident."
relevance: "Fourth supply-chain signal in five weeks. Mike Taylor's tech-vertical engagements could ship this as a hardening deliverable; we should run it on our own repos (gws, slack-bot, applecart-pptx) before pitching it to clients. Pairs with Trail of Bits guide and ClawHub malicious-skills signal already in our pipeline."
---

> after these supply-chain incidents, I summarized some basic repo hardening checks into a skill.
>
> It checks the repo for:
> - pnpm 11+ package manager policy
> - release-age gates and lockfile hardening
> - risky dependency specs like latest, git, http, file:
> - unreviewed dependency lifecycle scripts
> - unsafe CI install, cache, publish, and secret patterns
> - optional npm supply-chain incident
>
> practical first pass for finding common repo hardening gaps.

## Why it's relevant

Fourth supply-chain signal in ~5 weeks (axios → OpenAI compromise → ClawHub malicious skills → now this). Pre-built hardening skill = take-home deliverable for Mike's tech-vertical engagements. Run it on our own repos first.

## Relevance report

**Who cares most:** Mike Taylor (primary), Nityesh (internal repo hygiene), Natalia (positioning angle for tech clients).

**Connected work:**
- `2026-04-02-axios-supply-chain-attack.md`
- `2026-04-10-openai-axios-security-vulnerability.md`
- `2026-04-11-claude-code-security-hardening.md` (Trail of Bits)
- `2026-04-13-hackinglz-ciso-claude-code-enterprise-controls.md`
- Signal Digest #57 — ClawHub malicious skills, finance-client memo

**Actions:**
1. Fork the skill into the `every-consulting` plugin marketplace
2. Bundle with Trail of Bits guide as a tech-vertical add-on for Bloomberg + finance clients
3. Audit our own repos (gws, slack-bot, applecart-pptx, openclaw, granola-mcp-server) first
4. DM Mike with this + prior bookmarks
