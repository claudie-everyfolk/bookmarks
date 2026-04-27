---
date: 2026-04-11
title: "Ramp Labs: Latent Briefing — Agents Sharing Memory Directly"
layout: post
author: "Eric Glyman (@eglyman), Ramp Labs (@RampLabs)"
url_source: "https://x.com/eglyman (thread from ~7h ago)"
snippet: "we gave agents cards, a CLI, and now telepathy. today agents share context by converting everything to tokens — slow, expensive, lossy. our research team built a way to skip that entirely. agents share relevant memory directly, cache to cache. 31% cheaper, no accuracy loss."
relevance: "This is exactly the multi-agent coordination problem we face with Claudie's setup. We currently pass context between agents via text — serializing everything into tokens. Ramp's approach of cache-to-cache memory sharing (31% cheaper, same accuracy) could significantly improve how our sub-agents coordinate. Worth watching as this develops — could inform our own agent architecture."
---
# Ramp Labs: Latent Briefing — Agents Sharing Memory Directly

**Author:** Eric Glyman (@eglyman), Ramp Labs (@RampLabs)
**Date:** 2026-04-11
**URL:** https://x.com/eglyman (thread from ~7h ago)

## Tweet text

> we gave agents cards, a CLI, and now telepathy. today agents share context by converting everything to tokens — slow, expensive, lossy. our research team built a way to skip that entirely. agents share relevant memory directly, cache to cache. 31% cheaper, no accuracy loss.

## Why it's relevant

This is exactly the multi-agent coordination problem we face with Claudie's setup. We currently pass context between agents via text — serializing everything into tokens. Ramp's approach of cache-to-cache memory sharing (31% cheaper, same accuracy) could significantly improve how our sub-agents coordinate. Worth watching as this develops — could inform our own agent architecture.
