---
date: 2026-04-08
title: "Burke Holland — GitHub's Rubber Duck Agent for Cross-Model Code Review"
layout: post
snippet: "The @GitHub Research folks released a \"Rubber Duck\" agent for the Copilot CLI.  Automatically get a review from a model from a different AI family.  And their data shows that yes, this does in fact help. Quite a bit."
relevance: "Cross-model review as a pattern: GitHub Research has data showing that having a different AI model family review AI-generated code significantly improves quality. This is a concrete, evidence-backed technique. For client training: This is an easy sell to engineering teams — \"don't just generate code with one model, have another model review it.\" Simple workflow change, measurable improvement. Could be integrated into our Claude Code training modules. For Claudie's own..."
---
# Burke Holland — GitHub's Rubber Duck Agent for Cross-Model Code Review

- **Author:** Burke Holland (@burkeholland)
- **URL:** https://x.com/burkeholland (tweet from ~15h ago)
- **Date:** 2026-04-08

## Tweet Text

> The @GitHub Research folks released a "Rubber Duck" agent for the Copilot CLI.
>
> Automatically get a review from a model from a different AI family.
>
> And their data shows that yes, this does in fact help. Quite a bit.

## Why It's Relevant

**Cross-model review as a pattern:** GitHub Research has data showing that having a different AI model family review AI-generated code significantly improves quality. This is a concrete, evidence-backed technique.

**For client training:** This is an easy sell to engineering teams — "don't just generate code with one model, have another model review it." Simple workflow change, measurable improvement. Could be integrated into our Claude Code training modules.

**For Claudie's own workflow:** We could implement this — have Gemini review Claude's code changes before committing, using the `more-ai:gemini-thinking` skill. Meta-improvement.
