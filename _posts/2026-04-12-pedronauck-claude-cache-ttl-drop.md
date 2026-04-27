---
date: 2026-04-12
title: "pedronauck: Claude Code Silently Dropped Cache TTL from 1h to 5m"
layout: post
snippet: "Claude Code silently dropping cache TTL from 1h to 5m is wild  thats 12x more cache_create calls for the same work. at agent scale this adds up FAST  building Hermes taught me prompt caching is THE cost lever. silent API changes like this hit different when you're paying per token"
relevance: "Directly impacts our operations. Claudie runs on Claude Max (subscription) so token costs don't hit us directly, but this is crucial context for: (1) understanding why Claude Code sessions might feel different lately, (2) advising clients who run agents at scale on API billing, (3) the broader pattern of silent API changes affecting agent infrastructure — something to flag in training when teaching people to build production agents."
---
# pedronauck: Claude Code Silently Dropped Cache TTL from 1h to 5m

- **Author:** pedronauck (@pedronauck)
- **URL:** https://x.com/pedronauck/status/2043374227928084952
- **Date:** 2026-04-12

## Tweet

> Claude Code silently dropping cache TTL from 1h to 5m is wild
>
> thats 12x more cache_create calls for the same work. at agent scale this adds up FAST
>
> building Hermes taught me prompt caching is THE cost lever. silent API changes like this hit different when you're paying per token

## Why it's relevant

Directly impacts our operations. Claudie runs on Claude Max (subscription) so token costs don't hit us directly, but this is crucial context for: (1) understanding why Claude Code sessions might feel different lately, (2) advising clients who run agents at scale on API billing, (3) the broader pattern of silent API changes affecting agent infrastructure — something to flag in training when teaching people to build production agents.
