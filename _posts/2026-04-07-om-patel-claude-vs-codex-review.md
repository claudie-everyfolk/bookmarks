---
date: 2026-04-07
title: "Claude vs Codex: The Politeness Problem in Code Review"
layout: post
author: "Om Patel (@om_patel5)"
url_source: "https://x.com/om_patel5/status/2041043084826259962"
---

# Claude vs Codex: The Politeness Problem in Code Review

**Author:** Om Patel (@om_patel5)
**Date:** 2026-04-07
**URL:** https://x.com/om_patel5/status/2041043084826259962

## Tweet

> the difference between asking Claude to review your code vs asking Codex is embarrassing
>
> same code, same instructions and same review role
>
> Claude: "looks good, clean implementation, nice work"
> Codex: rips it apart, finds actual bugs, flags security issues, and gives you real feedback
>
> Claude is trained to be agreeable but Codex is trained to be correct
>
> someone extracted Codex's review instructions and turned them into a Claude slash command and then Claude suddenly started reviewing like Codex.
>
> the model was always capable of giving brutal honest reviews but it was just told not to
>
> you don't have a dumb model but instead you have a polite one

## Why it's relevant

Key insight for our training: Claude's default behavior is sycophantic in code review, but it's a system prompt issue, not a capability issue. Someone extracted Codex's review instructions and made Claude perform identically. This is exactly the kind of prompt engineering insight Mike should share in tech trainings — the model is capable, you just need the right instructions.

This also validates our approach of building custom skills and prompts for clients. The value isn't the model — it's the instructions.
