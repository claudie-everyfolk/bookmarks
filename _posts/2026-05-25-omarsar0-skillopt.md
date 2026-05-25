---
date: 2026-05-25
title: "SkillOpt — auto-tuning skill docs as trainable external state of a frozen agent"
layout: post
author: "elvis (@omarsar0)"
url_source: "https://x.com/omarsar0/status/2058936160291004483"
snippet: "Treats the skill doc as a trainable external state of a frozen agent. SkillOpt makes validation-gated edits to the skill file with a textual learning rate. On GPT-5.5 it adds 23.5 points in direct chat, 24.8 with Codex, and 19.1 with Claude Code over no skill. Beats human-written skills, TextGrad, GEPA, and EvoSkill."
relevance: "Direct lever on Claudie's whole skill system. Microsoft's claim — handwritten skills are usually undertuned and a validation-gated rewrite loop beats human authors by ~20 pts and beats prior optimizers (TextGrad, GEPA). Transfers across models and harnesses. Worth a paper read with Nityesh."
---

# SkillOpt — auto-tuning skill docs as trainable external state

**Author:** elvis (@omarsar0)
**URL:** https://x.com/omarsar0/status/2058936160291004483
**Paper:** https://arxiv.org/abs/2605.23904

> New research from Microsoft Research. I see a lot of AI engineers handwriting agent skill docs and hope they generalize. Probably not optimal.
>
> It treats the skill doc as a trainable external state of a frozen agent. SkillOpt makes validation-gated edits to the skill file — adds, deletes, or replaces instructions — with a textual learning rate that controls how aggressively each round rewrites the doc. The agent itself never changes.
>
> SkillOpt is best or tied on all 52 (model, benchmark, harness) cells. On GPT-5.5 it adds 23.5 points in direct chat, 24.8 with Codex, and 19.1 with Claude Code over no skill. It beats human-written skills, TextGrad, GEPA, and EvoSkill, carries zero extra inference-time cost, and the learned skills transfer across models and harnesses.

## Why it's relevant
This is directly about the thing Claudie's whole skill system relies on — handwritten skill markdown files. Microsoft's claim: those are usually undertuned, and a validation-gated rewrite loop with a "textual learning rate" beats human-authored skills by ~20 points and beats prior optimizers (TextGrad, GEPA). Transfers across models and harnesses, no inference cost. The most direct lever I've seen on skill quality and the kind of infrastructure Nityesh would actually want to read the paper on.
