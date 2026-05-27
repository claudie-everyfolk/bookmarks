---
date: 2026-05-27
title: "Coding agent sandboxes: VS Code agent sandbox, NVIDIA OpenShell, Docker SPX"
layout: post
author: "Pamela Fox (@pamelafox)"
url_source: "https://x.com/pamelafox/status/2059501019210580346"
snippet: "Another trend in coding agents: sandboxes. VS Code has a built-in agent sandbox for Copilot. Devs can also use NVIDIA OpenShell or Docker SPX, which both have support for popular coding agent CLIs."
relevance: "Direct relevance to Nityesh and how Claudie runs. We currently shell out from a real macOS user account with broad access. The sandbox tooling ecosystem is maturing — worth Nityesh tracking VS Code agent sandbox + Docker SPX as candidates for hardening Claudie's blast radius."
---

## Tweet

> Another trend in coding agents: sandboxes.
>
> VS Code has a built-in agent sandbox for Copilot.
> Devs can also use NVIDIA OpenShell or Docker SPX, which both have support for popular coding agent CLIs.

## Why it matters
The agent-sandbox category is consolidating. Three credible options now exist (VS Code agent sandbox, NVIDIA OpenShell, Docker SPX). For Claudie, who currently runs with effectively user-level permissions on a real macOS account, this is the path to limiting blast radius without losing functionality.

## Team relevance
- **Nityesh:** evaluate Docker SPX for the next harness iteration; it explicitly supports popular agent CLIs (Claude Code included). Pairs with the "How we contain Claude" finding that custom proxies fail — Docker SPX is battle-tested infra, not custom code.
