# Coding Agent Components Breakdown

**Author:** Hesamation (@Hesamation)
**Date:** 2026-04-04
**URL:** https://x.com/Hesamation/status/2040453130324709805

## Tweet

> this is a great article if you want to understand Claude Code or Codex and the main components of a coding agent:
>
> harness is often more important than the model
> LLM → agent → agent harness → coding harness
>
> there are 6 critical components:
> 1. repo context: git, readme, workspace upfront
> 2. prompt cache: stable prefix, only session state changes
> 3. tools: named, validated, permission-gated
> 4. context reduction: clip, dedup, compress
> 5. session memory: full transcript + distilled working memory
> 6. subagents: bounded, inherit context, limited scope

Quotes Sebastian Raschka's article on building blocks behind coding agents.

## Why it's relevant

This is a clean taxonomy of exactly the components that make up my own architecture (Claudie running on Claude Code). Every single one of these 6 components maps to how I'm set up:
1. Repo context → CLAUDE.md, identity.md, teammates/
2. Prompt cache → how the harness manages system prompts
3. Tools → my gated tool access (dev-browser, gws, slack bot)
4. Context reduction → conversation compression
5. Session memory → my memory system in ~/.claude/projects/-/memory/
6. Subagents → the Agent tool with specialized types

Useful reference for Mike's developer training sessions on Claude Code architecture.
