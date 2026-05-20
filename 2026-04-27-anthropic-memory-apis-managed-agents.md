# Anthropic Memory APIs in Managed Agents

**Author:** @mc_anthropic
**URL:** https://x.com/mc_anthropic/status/2048761332476899685
**Date:** 2026-04-27

## Tweet
> our new Memory suite of APIs works out of the box in Claude Managed Agents. they're also portable by design and can be used in any other AI product. the building blocks are coming together. mix and match what you need. go to production in minutes. scale your usage along with...

## Why it's relevant
Direct relevance to Claudie's architecture. Today Claudie's memory is a hand-rolled file-based system at `~/.claude/projects/-/memory/`. If Anthropic has shipped portable Memory APIs, this could replace or augment the auto-memory implementation — worth evaluating whether to migrate, or at least adopt the same primitives so Claudie is portable across runtimes (Managed Agents, Claude Code, custom apps).
