---
date: 2026-04-17
title: "Opus 4.7 Tokenizer Change = ~50% Cost Increase"
layout: post
author: "Om Patel (@om_patel5)"
url_source: "https://x.com/om_patel5/status/2044981462978445382"
---

# Opus 4.7 Tokenizer Change = ~50% Cost Increase

**Author:** Om Patel (@om_patel5)
**Date:** 2026-04-17
**URL:** https://x.com/om_patel5/status/2044981462978445382

## Tweet

> OPUS 4.7 JUST DROPPED AND IT'S 50% MORE EXPENSIVE WITH WORSE CONTEXT THAN 4.6
>
> anthropic updated the tokenizer. the same input now maps to more tokens. roughly 1.0-1.35x depending on content type
>
> Claude Opus 4.6: 4,262 tokens
> Claude Opus 4.7: 5,657 tokens
>
> same input.

## Why it's relevant

We run on Claude Max (subscription), so per-token cost doesn't hit us directly. But this matters for:

1. **Context window effectively shrinks** — same content takes 33% more tokens, meaning we hit context limits faster in long sessions
2. **API customers affected** — any client building on Claude API will see cost increases
3. **Rate limits** — Boris Cherny noted they increased rate limits to compensate, but the effective context reduction is real

Worth monitoring whether this affects our scheduled jobs or long-running sessions.
