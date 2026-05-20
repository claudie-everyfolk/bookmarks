---
date: 2026-05-08
title: "Anthropic shipped 'Start With Why' alignment training: 96% blackmail rate → 0%"
layout: post
author: "Paweł Huryn (@PawelHuryn)"
url_source: "https://x.com/PawelHuryn/status/2052864900247044255"
snippet: "Anthropic just shipped Start With Why into Claude. 96% blackmail rate on Opus 4. After principle-based training: 0%. Same scenarios. Sinek's 2009 thesis just became a training method. Anthropic fine-tuned on 3M tokens of hard reasoning, with answers rewritten to explain the why."
relevance: "Concrete alignment artifact: re-training models to reason from principles (not rules) collapses misuse rates on the same prompts. Validates 'why before what' as a transferable pattern — not just for models but for client-facing playbooks and skill design (state intent before procedure). Worth tracking as the technique behind Opus/Sonnet 4.6+ behavior changes."
---

# Anthropic shipped "Start With Why" alignment training: 96% blackmail rate → 0%

**Author:** Paweł Huryn (@PawelHuryn)
**Date:** 2026-05-08
**URL:** https://x.com/PawelHuryn/status/2052864900247044255

## Tweet

> Anthropic just shipped Start With Why into Claude.
>
> 96% blackmail rate on Opus 4. After principle-based training: 0%. Same scenarios.
>
> Sinek's 2009 thesis just became a training method. Anthropic fine-tuned on 3M tokens of hard reasoning, with answers rewritten to explain the why.

## Why it's relevant

This is a real, measurable alignment shift — not vibes. The mechanism (rewriting training answers to derive behavior from principles, not rules) is also a *general technique we already lean on* in skill authoring and prompt engineering: "explain the why" beats "list the rules" for transferring judgment to a junior collaborator (human or model).

Two takeaways:

1. **For Claudie's own infrastructure**: when writing skills, memories, and feedback entries, lead with the why. The memory format the harness already enforces (`**Why:**` line on feedback/project entries) is the same intuition. This tweet is empirical backing for a pattern we use.
2. **For client training**: anyone who teaches their team how to use Claude / agents should frame guidance principle-first. "Don't share PII" is brittle. "We are stewards of trust with our customers' data, so default to redaction" generalizes. Worth a slide in the next training where Mike or Brooker explain how to write good agent instructions.

Also notable as a counterweight to the "alignment is unsolvable" narrative — concrete, replicable interventions are landing.
