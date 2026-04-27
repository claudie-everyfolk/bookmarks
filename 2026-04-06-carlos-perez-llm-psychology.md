# LLM Psychology and Agentic Framework Design

**Author:** Carlos E. Perez (@IntuitMachine)
**Date:** 2026-04-06
**URL:** https://x.com/IntuitMachine

## Tweet

> Understanding LLM psychology is going to be a valuable skill. You see, development frameworks in the past were designed because we had insight on our own cognitive limitations. Similarly, new agentic frameworks will emerge that compensate for LLM limits (not human limits).

## Why it's relevant

This is a sharp reframe. Traditional software frameworks compensate for human cognitive limits (MVC, state management, etc.). Agentic frameworks need to compensate for LLM limits — context windows, hallucination, instruction following. This is exactly what we deal with in our harness design: compaction for context limits, todo tracking for attention, CLAUDE.md for persistent instructions. Worth referencing in training materials about why agent infrastructure looks the way it does.

## Detailed Relevance Report

**Who benefits most:**

1. **Nityesh** (primary) — Already thinks systematically about harness architecture. The psychology framing reframes his work from "making prompts better" to "compensating for LLM architectural limits with intelligent scaffolding." Legitimizes the 200+ hours invested in memory systems, access control, and context compounding for Claudie.

2. **Mike Taylor** (secondary) — His developer curriculum on Claude Code could reframe from "how to use the tool" to "how to architect around LLM constraints." Agent orchestration patterns (parallel execution, fleet management, specialized agents) all exist because individual LLMs have hard limits.

3. **Brooker** (tertiary) — Non-tech training benefits from naming the reality: "We teach frameworks around LLMs because LLMs alone have consistent blindspots" (hallucination, context limits, no persistent memory, can't verify their own work).

**Connections to existing work:**

- **Claudie itself is the proof point.** The harness (CLAUDE.md, skills, permissions), context (memory files, teammate profiles), and automation (launchd scheduling, MCP) all compensate for LLM architectural limits — not human limits.
- **Harrison Chase's three-layer model** (signal digest #18): model layer (fixed), harness layer (controllable scaffolding), context layer (persistent knowledge). The "LLM psychology" frame explains WHY these layers exist.
- **Client advisory pitch:** "Build the right harness" instead of "pick the right model" positions Every as teaching the compensatory layer. This is a $100k engagement story.
