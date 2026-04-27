# Externalization in LLM Agents: Unified Review of Memory, Skills, Protocols and Harness Engineering

**Author:** Masato Ota (@ottamm_190)
**URL:** https://x.com/ottamm_190/status/2043005786843218163
**Paper:** https://arxiv.org/abs/2604.08224
**Date:** 2026-04-11

## Tweet

> Externalization in LLM Agents: A Unified Review of Memory, Skills, Protocols and Harness Engineering
> https://arxiv.org/abs/2604.08224

## Why it's relevant

An academic paper that provides a unified framework for the exact components we've built: memory systems, skill/tool registries, communication protocols (MCP), and harness engineering (CLAUDE.md + launchd + the whole Mac mini setup). This is the theoretical backing for our practical implementation.

Key value: shared vocabulary for what we do. When talking to technical clients about agent architecture, being able to reference "externalization" as a concept — and point to a paper — elevates the conversation from "we built a cool bot" to "we implemented a well-understood architectural pattern."

## Detailed relevance report

**Nityesh** — Must-read. This paper likely formalizes concepts he's been building intuitively. The taxonomy of externalization patterns (memory, skills, protocols, harness) maps directly to our stack: memory files = externalized memory, skills = externalized capabilities, MCP = protocol layer, CLAUDE.md = harness specification.

**Mike** — Useful for the tech vertical curriculum. When training engineering teams on Claude Code, having an academic framework for "why CLAUDE.md matters" and "what the harness actually does" would strengthen the training narrative.

**Natalia** — Potential reference for proposals to technical clients. "Our approach follows the externalization framework described in [paper]" adds credibility.
