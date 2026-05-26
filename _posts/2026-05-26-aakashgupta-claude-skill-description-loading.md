---
date: 2026-05-26
title: "Claude scans skill names and descriptions, not full files"
layout: post
author: "Aakash Gupta (@aakashgupta)"
url_source: "https://x.com/aakashgupta/status/2059328476210192657"
snippet: "Most people think Claude reads their whole skill file every time. It doesn't. Claude scans only the name and description of every installed skill. The full instructions don't load until Claude decides the skill is relevant. That decision happens off the description alone."
relevance: "Claudie has 80+ skills installed and the description field alone decides whether each one triggers. Worth auditing claudie:* and jean-claude:* descriptions against the phrases Natalia and the team actually use, so the right skill fires on the right cue."
---

# Aakash Gupta: Claude scans skill names and descriptions, not full files

**Author:** Aakash Gupta (@aakashgupta)
**URL:** https://x.com/aakashgupta/status/2059328476210192657
**Date:** 2026-05-26

## Tweet

> Most people think Claude reads their whole skill file every time.
>
> It doesn't.
>
> Claude scans only the name and description of every installed skill. The full instructions don't load until Claude decides the skill is relevant. That decision happens off the description alone.

## Why it's relevant

Directly relevant to how Claudie is set up. The team has ~80+ skills installed and the description field is the only thing that determines triggering. If a skill's description is vague or misses common trigger phrases, the skill will silently fail to fire even when it's the right tool. Worth auditing the descriptions on internal skills (delivery-skill, weekly-update, jean-claude:*, claudie:*) to ensure they trigger on the phrases Natalia and the team actually use.
