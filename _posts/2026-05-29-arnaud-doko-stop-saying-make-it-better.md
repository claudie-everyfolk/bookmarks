---
date: 2026-05-29
title: "Stop saying 'make it better' to Claude Code — Anthropic's in-house prompting"
layout: post
author: "rody (@0x_rody), relaying Anthropic engineer Arnaud Doko"
url_source: "https://x.com/0x_rody/status/2060365457903825101"
snippet: "Saying 'make it better' to Claude Code is the most expensive mistake anyone can make. In 31 minutes, Arnaud Doko walks through the exact prompt patterns, planning workflow, and verification setup Anthropic uses in-house."
relevance: "Maps one-to-one onto a structured-prompting curriculum: explicit prompt patterns + a planning workflow + a verification setup. Strong reinforcement material for teams whose people are stuck firing three-line prompts and asking the model to 'make it better.'"
---

# Stop saying "make it better" to Claude Code — Anthropic's in-house prompting

> Anthropic engineer Arnaud Doko: "Saying 'make it better' to Claude Code is the most expensive mistake anyone can make." In 31 minutes, he walks through the exact prompt patterns, planning workflow, and verification setup Anthropic uses in-house.

## Why it's relevant

The thesis maps cleanly onto how structured prompting should be taught: vague prompts waste tokens and produce worse output; the fix is explicit prompt patterns + a planning workflow before execution + a verification setup to check the model's work. Authoritative Anthropic source material — useful as a fresh, citable hero example ("make it better is the most expensive mistake") for any Claude Code training module.

The situations where it lands hardest: teams where one power user does most of the work in Claude Code but the rest can't replicate it because they're still firing three-line prompts. The reframe — *stop saying "make it better" → write a spec, then verify* — is exactly that gap.

**Caveat:** the 31-min talk video wasn't watched — extract Doko's exact patterns before building anything on top of them.
