---
date: 2026-04-07
title: "Anthropic - Project Glasswing"
layout: post
author: "Anthropic (@AnthropicAI)"
url_source: "https://x.com/AnthropicAI/status/2041578392852517128"
---

# Anthropic - Project Glasswing

**Author:** Anthropic (@AnthropicAI)
**Date:** 2026-04-07
**URL:** https://x.com/AnthropicAI/status/2041578392852517128

## Tweet

> Introducing Project Glasswing: an urgent initiative to help secure the world's most critical software.
>
> It's powered by our newest frontier model, Claude Mythos Preview, which can find software vulnerabilities better than all but the most skilled humans.

Linked article: anthropic.com (Project Glasswing: Securing critical software for the AI era)

Follow-up tweet links to detailed technical report on vulnerabilities and exploits discovered by Claude Mythos Preview: red.anthropic.com/2026/mythos-pr

## Why it's relevant

- **AI Security:** Anthropic is entering the automated security scanning space with a dedicated model. This is a significant move — not just a feature, but a new model class optimized for vulnerability detection.
- **Consulting implications:** Clients in finance and media (Bloomberg, NYT) should know about this. Automated vulnerability scanning powered by frontier models changes the security posture conversation.
- **Platform signal:** Anthropic continues to expand beyond chat/coding into specialized verticals (security). This is the kind of product diversification that makes the platform more sticky.
- **For Claudie:** If Claude Mythos Preview becomes available via API, it could be used to scan client codebases or our own infrastructure for vulnerabilities.

## Detailed Relevance Report

**Who Cares Most:**

1. **Nityesh** — PRIMARY. Maintains Claudie's infrastructure, already curates security signals (axios NPM compromise, malicious JSON formatter, slopcop bookmarks). Claude Mythos API access would become an infrastructure decision. Could use it to scan our own codebase (especially given the recent file exfiltration vulnerability flagged by Garry Tan).

2. **Natalia** — HIGH. Clients are Bloomberg, NYT, financial institutions where security audits are table-stakes. Glasswing positions Every Consulting as security-aware. Platform risk memo already documents Anthropic tightening third-party access — Mythos signals new product categories we can advise clients on.

3. **Mike** — MODERATE-HIGH. Developer training could include a live demo: "Here's how Claude Mythos catches what humans miss."

**Concrete Actions:**
1. Nityesh: Request Mythos API access when available. Test against Claudie's codebase as a pilot.
2. Natalia: Add "security vulnerability scanning via Claude Mythos" to consulting offerings for tech clients.
3. Mike: Develop a 10-minute module on Mythos for tech training vertical.
