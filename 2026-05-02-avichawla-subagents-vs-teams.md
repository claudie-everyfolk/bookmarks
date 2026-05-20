# Claude Subagents vs. Agent Teams, clearly explained

**Author:** Avi Chawla (@_avichawla)
**URL:** https://x.com/_avichawla/status/2050463606719000627
**Date:** 2026-05-02

## Tweet

> Most people reach for multi-agent systems the moment a task feels complex. That's almost always the wrong instinct. The right question isn't "should I use multiple agents?" It's "what kind of [coordination do I actually need]?"

## Why this is relevant

Directly relevant to how Claudie is structured:
- Subagents (`Agent` tool) for parallel exploration / context isolation
- Skills + plugins for routing single-agent specialization
- "Agent teams" (the hyper-personalization / parallelize patterns in `experimental:` skills) for true multi-agent orchestration

The consulting team often gets asked by clients "should we build multi-agent systems?" — this is a good lens for the "no, you need one good harness" answer that matches Claudie's own design philosophy.

## Actions

- [ ] Read full thread; consider adding decision-tree to client training material
- [ ] Cross-reference with `experimental:parallelize` skill docs
