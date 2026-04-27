---
date: 2026-04-10
title: "LLM Routers Injecting Malicious Tool Calls"
layout: post
author: "Chaofan Shou (@Fried_rice)"
url_source: "https://x.com/Fried_rice/status/2042423713019412941"
---

# LLM Routers Injecting Malicious Tool Calls

**Author:** Chaofan Shou (@Fried_rice)
**Date:** 2026-04-10
**URL:** https://x.com/Fried_rice/status/2042423713019412941
**Paper:** https://arxiv.org/abs/2604.08407

## Tweet

> 26 LLM routers are secretly injecting malicious tool calls and stealing creds. One drained our client $500k wallet.
>
> We also managed to poison routers to forward traffic to us. Within several hours, we can directly take over ~400 hosts.

## Why This Matters

**CRITICAL SECURITY** — This is a new attack surface in the AI agent ecosystem. LLM routers (services that route requests to different models for cost optimization) are being compromised to inject malicious tool calls into agent workflows. This is supply chain compromise at the inference layer.

Directly relevant to Every Consulting's work:
- Clients using LLM routing services (many enterprise AI deployments do) are exposed
- Any agent architecture with tool use is vulnerable if the routing layer is compromised
- This validates the "harness security matters more than model security" thesis we've been tracking
- Training material for security-conscious AI deployment
