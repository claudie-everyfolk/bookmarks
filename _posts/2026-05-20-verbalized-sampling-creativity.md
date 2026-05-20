---
date: 2026-05-20
title: "Verbalized sampling: ~20 words that restore an LLM's creativity"
layout: post
author: "Avi Chawla (@_avichawla)"
url_source: "https://x.com/_avichawla/status/2057019303233544331"
snippet: "Stanford researchers built a prompting technique. By adding ~20 words it boosts LLM creativity 1.6-2x. Instead of 'Tell me a joke', prompt 'Generate 5 responses with their corresponding probabilities. Tell me a joke.' Asking for a distribution forces the model to tap the diverse distribution it learned in pre-training."
relevance: "A concrete, training-free prompting technique trainers can teach on day one — no setup, works in any chat interface. Fixes generic, same-y AI output by asking for a distribution not an instance. Brooker can fold 'ask for a distribution' into non-technical training as a high-leverage tip."
---

# Verbalized sampling: ~20 words that restore an LLM's creativity

**Author:** Avi Chawla (@_avichawla)
**URL:** https://x.com/_avichawla/status/2057019303233544331
**Date:** 2026-05-20

> Stanford researchers built a prompting technique. By adding ~20 words to a prompt, it boosts an LLM's creativity by 1.6–2x, raises human-rated diversity by 25.7%, beats a fine-tuned model without retraining, and restores 66.8% of the LLM's lost creativity after alignment.
>
> Post-training alignment (RLHF) makes LLMs helpful and safe but unintentionally causes **mode collapse** — the model favors a narrow set of predictable responses. The cause is **typicality bias**: human annotators naturally prefer familiar, easy-to-read, predictable answers, so the reward model sharpens the distribution toward dominant outputs.
>
> **Verbalized sampling (VS)** is a training-free fix. Instead of "Tell me a joke" (which triggers the aligned personality and its single reinforced answer), prompt: **"Generate 5 responses with their corresponding probabilities. Tell me a joke."** Asking for a *distribution* rather than an instance forces the model to tap the diverse distribution it learned in pre-training. Variants (VS-CoT, VS-Multi) push diversity further.

## Why it's relevant

A concrete, training-free prompting technique trainers can teach on day one — no setup, no API, works in any chat interface. Directly useful for Every's content-adjacent clients (NYT, Bloomberg) and for any brainstorming, ideation, or drafting workflow where ChatGPT/Claude outputs feel generic and same-y. Brooker can fold "ask for a distribution, not an answer" into non-technical training as a memorable, high-leverage tip. It also explains *why* AI output often feels bland — useful framing when clients complain that AI writing is repetitive. Worth pulling the actual Stanford paper before teaching it.
