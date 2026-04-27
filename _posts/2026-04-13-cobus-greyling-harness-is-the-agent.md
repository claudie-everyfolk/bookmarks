---
date: 2026-04-13
title: "The Model Is Not the Agent. The Harness Is."
layout: post
author: "Cobus Greyling (@CobusGreylingZA)"
url_source: "https://x.com/CobusGreylingZA/status/2043638576848707662"
---

# The Model Is Not the Agent. The Harness Is.

**Author:** Cobus Greyling (@CobusGreylingZA)
**URL:** https://x.com/CobusGreylingZA/status/2043638576848707662
**Date:** 2026-04-13

## Tweet

References a paper (arxiv.org/pdf/2604.08224) and Harrison Chase (@hwchase17) blog post on agent architecture.

Three externalization dimensions define a harnessed agent:
1. **Memory** — working context, semantic knowledge, episodic experience, personalized memory
2. **Skills** — operational procedures, decision heuristics, normative constraints
3. **Protocols** — the connective tissue + operational layer (sandboxing, observability, compression, evaluation, approval loops, sub-agent orchestration)

"We spent 2022-2023 obsessing over making models smarter. Now the real engineering challenge is clear: it's building the harness infrastructure that turns a smart model into a reliable, safe, and effective agent."

## Why It's Relevant

This is the theoretical framework for what Claudie is in practice. The three dimensions (memory, skills, protocols) map directly to Claudie's architecture: qmd semantic search + memory system, skill-based task execution, and the operational layer (launchd scheduling, access control rings, dev-browser, MCP). The paper validates the approach and the arxiv link is worth reading for the team.
