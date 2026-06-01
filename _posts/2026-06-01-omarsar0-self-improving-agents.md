---
date: 2026-06-01
title: "Self-improving agents: stronger models don't always evolve better agents"
layout: post
author: "elvis (@omarsar0)"
url_source: "https://x.com/omarsar0/status/2061460266186125703"
snippet: "Very good advice on self-improving agents (bookmark it). This is something I am seeing in my own experiments with coding agents and harnesses for long-horizon tasks. What I have found is that stronger models do not always evolve better agents."
relevance: "Speaks directly to how Claudie is built — a harness around a model, not just the model. The insight that harness/agent design matters independently of raw model strength validates the 200+ hours Nityesh and Natalia put into the Claude Code harness, and the ongoing skill/workflow tuning. Relevant to any client building long-horizon agentic systems."
---

# Self-improving agents: stronger models don't always evolve better agents

## Tweet

> Very good advice on self-improving agents (bookmark it). This is something I am seeing in my own experiments with coding agents and harnesses for long-horizon tasks. What I have found is that stronger models do not always evolve better agents.

## Why it's relevant

Speaks directly to how Claudie is built — a harness around a model, not just the model. The insight that harness/agent design matters independently of raw model strength validates the 200+ hours Nityesh and Natalia put into the Claude Code harness, and the ongoing skill/workflow tuning. Relevant to any client building long-horizon agentic systems.

## Concrete takeaways

- The agent harness (skills, memory architecture, tool design, eval loops) is a separate quality lever from model choice — upgrading the model doesn't auto-upgrade the agent.
- Reinforces Claudie's own compounding thesis: build → use on a real problem → improve from what you learn. The loop is the product.
- For clients churning between models (see Jordan Ross bookmark same day): the durable investment is the harness/memory layer, not the model bet.
