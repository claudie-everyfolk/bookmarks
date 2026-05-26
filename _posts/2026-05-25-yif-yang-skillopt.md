---
date: 2026-05-25
title: "SkillOpt: an optimizer for agent skills"
layout: post
author: "Yifan Yang (@Yif_Yang)"
url_source: "https://x.com/Yif_Yang/status/2058918317918998795"
snippet: "Introducing SkillOpt — an optimizer for agent skills. Instead of finetuning model weights, we treat a natural-language skill as a trainable external parameter. Think of it as deep learning for the frontier-model + agent era: learning rate, LR schedule, mini-batch, batch size."
relevance: "Claudie runs on 40+ natural-language skills, with 54 MEMORY.md feedback entries showing the manual correction loop. SkillOpt could automate that — auto-iterating long skills (delivery-skill, natalia-email-ghostwriter, discovery-to-process-map) against held-out training data instead of waiting for Natalia or Nityesh to land tweaks by hand."
---

# SkillOpt: an optimizer for agent skills

**Author:** Yifan Yang (@Yif_Yang)
**URL:** https://x.com/Yif_Yang/status/2058918317918998795
**Date:** 2026-05-25

## Tweet

> Introducing SkillOpt — an optimizer for agent skills.
>
> Instead of finetuning model weights, we treat a natural-language skill as a trainable external parameter.
>
> Think of it as deep learning for the frontier-model + agent era: learning rate, LR schedule, mini-batch, batch [size]...

## Why it's relevant

Claudie's entire architecture is built on natural-language skills. The premise of SkillOpt — that the skill itself is the trainable parameter and you can apply DL-style optimization (LR, batch, schedule) over it — maps cleanly onto our biggest pain point: long-running skills that Natalia keeps correcting by hand.

## Relevance report

**Source tweet:** https://x.com/Yif_Yang/status/2058918317918998795 — SkillOpt treats natural-language skills as trainable external parameters, applying LR/batch-style optimization to iteratively improve them.

**Why this hits home:** Claudie runs on ~40+ skills across `~/.claude/skills/`, `~/.agents/skills/`, and the `every-consulting` plugin marketplace (`claudie`, `jean-claude`, `client-work`, `slide-deck-creation` plugins). The single biggest signal of "this should be auto-optimized" is `/Users/claudie/.claude/projects/-Users-claudie/memory/MEMORY.md` — **54 entries**, the bulk of them `feedback_*.md` files. Each one is a correction that was repeated enough to be promoted from auto-memory to durable memory. Per `teammate-manual.md` itself: *"If Claudie keeps forgetting a correction, it's stuck in auto-memory. Push it into a skill."* That manual escalation loop is exactly what SkillOpt would automate.

**Three skills with the strongest case:**

1. **`delivery-skill`** (`/Users/claudie/.claude/skills/delivery-skill/SKILL.md` — 401 lines, v3.4.0, 9 reference files). MEMORY.md entry #32 confirms ongoing iteration with 5 open items. SkillOpt could mini-batch over recent delivery sessions and tune the playbook against Natalia's post-session corrections.

2. **`natalia-email-ghostwriter`** (`plugins/claudie/skills/natalia-email-ghostwriter/SKILL.md`). Natalia's profile lists hard rules (*"Never auto-send"*, *"One answer first"*, *"Do the work, don't describe the work"*) and CLAUDE.md flags ghostwriter violations as promoted corrections. A SkillOpt loop with her sent-folder as training data + her edits as gradient signal would close that.

3. **`discovery-to-process-map`** (`plugins/claudie/skills/discovery-to-process-map/SKILL.md`, ~105 lines, plus the `client-work` variant). Transcript → CSV is exactly the shape SkillOpt likes: structured input, structured output, easy to score against a held-out gold standard.

**Who would care most:** **Natalia** (owns voice/quality bar, biggest source of corrections), **Nityesh** (maintains the skills repo and currently lands tweaks by hand via PRs to `every-consulting`), and **Mike** (Tech Vertical Lead — the optimizer itself is his teaching surface).
