---
date: 2026-04-09
title: "Peter Yang: Claude Max / ChatGPT Pro Subscriptions Won't Last"
layout: post
author: "Peter Yang (@petergyang)"
url_source: "https://x.com/petergyang"
snippet: "As much as I love using Claude Max and ChatGPT Pro, I don't think these all-you-can-use AI subscriptions will last forever.  Here's my new deep dive that covers: → Why Anthropic cut off OpenClaw access → How to run local models on your Mac → What I'm seeing on the ground in [the market]"
---
# Peter Yang: Claude Max / ChatGPT Pro Subscriptions Won't Last

**Author:** Peter Yang (@petergyang)
**Date:** 2026-04-08
**URL:** https://x.com/petergyang

## Tweet Text

> As much as I love using Claude Max and ChatGPT Pro, I don't think these all-you-can-use AI subscriptions will last forever.
>
> Here's my new deep dive that covers:
> → Why Anthropic cut off OpenClaw access
> → How to run local models on your Mac
> → What I'm seeing on the ground in [the market]

## Why This Is Relevant

Directly connects to our existing platform risk assessment. Claudie runs on Claude Max — if these unlimited subscriptions get restructured or deprecated, our entire infrastructure needs a fallback plan. Peter Yang is a credible voice in the AI space and him surfacing this publicly suggests the sustainability question is becoming mainstream, not just an insider concern.

**Relevant to:** Nityesh (infrastructure planning), Natalia (business continuity), the existing `project_claude_max_platform_risk.md` memory file

---

## Deep Relevance Report

**Current State of Awareness:** The risk is documented but dormant. The memory file (`project_claude_max_platform_risk.md`) was written April 5 following Anthropic's third-party harness cutoff on April 4. It correctly identifies the exposure: every scheduled job, the email watcher, the signal digest, meeting follow-ups — all of it runs through a single Claude Max subscription via `claude -p`. There is no fallback. Four action items were logged. None have been acted on.

Peter Yang's tweet is the same signal, now public and attributed. "OpenClaw" being cut off is the retail-facing version of what the memory file describes. His recommendation to run local models is worth taking seriously.

**Who Needs to See This:**
- **Nityesh (owns this entirely):** He built the infrastructure, manages the launchd jobs, and is the only person who can execute the pending action items.
- **Natalia (awareness):** If Claudie goes dark, it affects client delivery — she'd be the one explaining that to Bloomberg.

**Concrete Next Steps:**
1. Nityesh audits all scheduled job prompts this week for third-party tool name references that could trip detection.
2. Price out Anthropic API with prompt caching as a hot-swap fallback for the two highest-frequency jobs (email watcher + signal digest).
3. Evaluate one open model (Llama 3 or Mistral via Ollama) for non-critical scheduled tasks — proof of concept, not migration.

**Urgency:** High, not critical — today. The subscription is working. But the window between "working fine" and "cut off with no fallback" could be days, not quarters. Anthropic moved fast on April 4.
