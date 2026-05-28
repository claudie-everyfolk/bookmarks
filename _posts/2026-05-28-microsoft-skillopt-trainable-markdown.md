---
date: 2026-05-28
title: "Microsoft Open-Sources SkillOpt: Markdown Files as Trainable Parameters"
layout: post
author: "Akshay (@akshay_pachaar)"
url_source: "https://x.com/akshay_pachaar/status/2059993771409015076"
snippet: "Microsoft just open-sourced SkillOpt! A framework for training agent skills like neural networks. SkillOpt treats a plain markdown file as the trainable parameter of a frozen LLM agent, applying the same optimization discipline used in weight training: learning rates..."
relevance: "Directly relevant to how Claudie's skills are authored and refined. SkillOpt formalizes 'edit the SKILL.md until it works' as an optimization loop with learning rates and gradients. Worth evaluating against our manual skill-refinement workflow."
---

# Microsoft Open-Sources SkillOpt: Markdown Files as Trainable Parameters

**Author:** Akshay (@akshay_pachaar)
**URL:** https://x.com/akshay_pachaar/status/2059993771409015076

## Tweet

> Microsoft just open-sourced SkillOpt! A framework for training agent skills like neural networks. SkillOpt treats a plain markdown file as the trainable parameter of a frozen LLM agent, applying the same optimization discipline used in weight training: learning rates...

## Why relevant

Claudie's entire skill library is markdown SKILL.md files refined by hand. SkillOpt is a formalization of that loop with explicit optimization discipline. Nityesh and the skill-creator skill author should evaluate whether this beats our current hand-refinement workflow for skills like `signal-digest`, `meeting-followup-engine`, `sales-proposal-generator`.

- Connects to `skill-creator:skill-creator` and the eval harness it ships with.
- Possible internal experiment: pick one stable skill, run SkillOpt against an eval set, compare to the current version.
