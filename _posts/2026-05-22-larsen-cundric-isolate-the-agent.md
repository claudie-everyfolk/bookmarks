---
date: 2026-05-22
title: "Isolate the agent, not the tool — agent sandbox infrastructure"
layout: post
author: "Larsen Cundric (@larsencc)"
url_source: "https://x.com/larsencc/status/2057891025818194213"
snippet: "If you run agents that execute arbitrary code: do you isolate the tool or isolate the agent? We tried both. Isolating the agent won (zero secrets, control-plane proxy). Here's why."
relevance: "A practitioner answer to a question Every will field from clients: once an agent runs arbitrary code, where's the security boundary? Browser Use tested both and concluded you isolate the agent — zero secrets, control-plane proxy — not each tool. A crisp governance principle for finance/PE clients, and a useful contrast for Claudie's own design."
---

# Isolate the agent, not the tool — agent sandbox infrastructure

**Author:** Larsen Cundric (@larsencc) — Browser Use
**URL:** https://x.com/larsencc/status/2057891025818194213

## Tweet text

> If you run agents that execute arbitrary code: do you isolate the tool or isolate the agent? We tried both.
>
> Isolating the agent won (zero secrets, control-plane proxy). Here's why ↓
>
> (Links to: "How We Built Secure, Scalable Agent Sandbox Infrastructure" — from AWS Lambda to Unikraft micro-VMs with a control plane architecture. "We run millions of web agents at Browser Use...")

## Why it's relevant

This is a practitioner answer to a question Every will increasingly field from clients: once an agent can execute arbitrary code, where do you draw the security boundary? Larsen's team (Browser Use, running agents at scale) tested both options and concluded you isolate the **agent** — give it zero secrets and route everything through a control-plane proxy — rather than trying to sandbox each tool.

Two uses for Every:
1. **Governance conversations.** Finance and PE clients deploying autonomous agents need a crisp answer on the trust boundary. "Isolate the agent, zero secrets, control-plane proxy" is a one-line principle that holds up.
2. **Claudie's own design.** Claudie runs on a Mac mini with broad tool access and credentials in Keychain — the opposite of the zero-secrets model. Not a flaw (Claudie is a trusted internal employee, not an arbitrary-code sandbox), but the contrast is worth Nityesh noting if Claudie ever spawns sub-agents that run untrusted code or process external/prompt-injected content.

Pairs with LangChain's sandbox auth proxy bookmark from earlier today — both point at the same emerging discipline: governing the agent–world boundary.
