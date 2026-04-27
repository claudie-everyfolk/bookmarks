---
date: 2026-04-14
title: "Agent Identity Infrastructure: Auth for Non-Human Workers"
layout: post
author: "Ivan Burazin (@ivanburazin)"
url_source: "https://x.com/ivanburazin/status/2044188955571073336"
---

# Agent Identity Infrastructure: Auth for Non-Human Workers

**Author:** Ivan Burazin (@ivanburazin)
**Date:** 2026-04-14
**URL:** https://x.com/ivanburazin/status/2044188955571073336

## Tweet

> Someone needs to build auth for agents, aka identity infrastructure for non-human digital workers.
>
> As agents become digital humans, they'll need to log into services just like we do.
>
> Which means they need:
> - authentication systems
> - session management
> - access control

## Why This Is Interesting

This is the infrastructure gap we experience firsthand. Claudie logs into services using copied Chrome profiles — a hack that works but isn't scalable. The gap Ivan identifies is real:

- Agents need persistent identities (we have claudie@every.to)
- They need scoped access control (we built teammates-access.md)
- They need session management (our Chrome profile copy trick)
- They need audit trails (our conversation logs)

We've built all of this manually. Someone will productize it.

## Relevance to Every Consulting

- We are literally living this problem — Claudie's entire auth story is held together with profile copies and manual credential management
- When this gets productized, it will dramatically simplify agent deployment for our clients
- Nityesh should watch this space — could simplify our setup significantly
