---
date: 2026-04-23
author: Gregor Zunic (@gregpr07)
url: https://x.com/gregpr07/status/2047371442879422566
---

# The Bitter Lesson of Agent Harnesses

**Tweet:** "Don't wrap the LLM. Don't wrap its tools either. All you need is a SKILL.md and some Python helpers. The LLM has complete freedom. If something's missing, it writes it."

Reposts/endorsements from Viv (@Vtrivedy10) and Larsen Cundric — "Agent harness feels like AGI."

## Why it's relevant

Directly validates Claudie's current architecture: minimal wrappers, skills as the primary extension mechanism, LLM writes its own tooling when needed. Worth reading against our plugin-creator and skill-creator patterns — Browser Use is preaching the same gospel Anthropic is shipping.

Tie-ins:
- Our skill ecosystem already follows this (73+ skills listed, SKILL.md-style)
- Reinforces "don't over-engineer harness" — relevant to Nityesh's frequent friction around added abstractions
- Good ammo for client training decks: "the harness is the bitter lesson, skills are the primitive"
