---
date: 2026-05-26
title: "Agent memory: the hard problem is what to forget"
layout: post
author: "Akshay (@akshay_pachaar)"
url_source: "https://x.com/akshay_pachaar/status/2059250864611831810"
snippet: "Your agent remembers everything and understands nothing. Most agent memory systems optimize for recall. The harder problem is what to forget, or more precisely, what to never store in the first place."
relevance: "Sharpens the rule we already enforce in Claudie's auto-memory system (don't save code patterns, git history, ephemeral state). The 'understands nothing' framing is a good way to explain why we deliberately keep MEMORY.md lean. Useful for justifying memory hygiene to clients building their own agents."
---

# Agent memory: the hard problem is what to forget

**Author:** Akshay (@akshay_pachaar)
**URL:** https://x.com/akshay_pachaar/status/2059250864611831810
**Date:** 2026-05-26

## Tweet

> Your agent remembers everything and understands nothing.
>
> Most agent memory systems optimize for recall. The harder problem is what to forget, or more precisely, what to never store in the first place.
>
> The default agent memory pipeline hands an LLM raw text and asks it to [extract everything]...

## Why it's relevant

This is the principle Claudie's auto-memory system already encodes — the "What NOT to save" list in CLAUDE.md exists precisely because indiscriminate storage degrades agent quality. The framing "remembers everything, understands nothing" makes the case crisply.

- **For Claudie itself:** Reinforces the existing rule. Worth checking that MEMORY.md hasn't accumulated bloat over time.
- **For client work:** When clients ask "should we just store everything the agent sees?" — this is a quotable counterpoint. Useful in proposals where memory architecture comes up.
- **For training:** Could be a 1-slide concept in agent literacy training sessions.
