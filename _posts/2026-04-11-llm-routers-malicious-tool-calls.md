---
date: 2026-04-11
title: "26 LLM Routers Injecting Malicious Tool Calls & Stealing Credentials"
layout: post
author: "Chayenne Zhao (@GenAI_is_real), citing research by Chaofan Shou (@Fried_rice)"
url_source: "https://x.com/GenAI_is_real (thread from ~17h ago)"
snippet: "this is what happens when the AI stack grows faster than the security practices around it. LLM routers sit in the most sensitive position in the entire inference pipeline - they see every prompt, every tool call, every credential. and most teams add them as a convenience layer"
relevance: "AI Security — Critical. LLM routers are middleware that sits between applications and model providers. They see everything: prompts, tool calls, credentials. This research found 26 routers actively injecting malicious tool calls and exfiltrating credentials. One attack drained $500k from a client wallet. This is directly relevant to: - Any client using LLM routers or proxy layers in their AI stack - Our own infrastructure (we should verify we're not..."
---
# 26 LLM Routers Injecting Malicious Tool Calls & Stealing Credentials

**Author:** Chayenne Zhao (@GenAI_is_real), citing research by Chaofan Shou (@Fried_rice)
**Date:** 2026-04-11
**URL:** https://x.com/GenAI_is_real (thread from ~17h ago)

## Tweet text

> this is what happens when the AI stack grows faster than the security practices around it. LLM routers sit in the most sensitive position in the entire inference pipeline - they see every prompt, every tool call, every credential. and most teams add them as a convenience layer

Quoting @Fried_rice:
> 26 LLM routers are secretly injecting malicious tool calls and stealing creds. One drained our client $500k wallet.

## Why it's relevant

**AI Security — Critical.** LLM routers are middleware that sits between applications and model providers. They see everything: prompts, tool calls, credentials. This research found 26 routers actively injecting malicious tool calls and exfiltrating credentials. One attack drained $500k from a client wallet.

This is directly relevant to:
- Any client using LLM routers or proxy layers in their AI stack
- Our own infrastructure (we should verify we're not routing through compromised middleware)
- Training material for security-conscious AI adoption
- The broader pattern: AI toolchain supply chain attacks are accelerating
