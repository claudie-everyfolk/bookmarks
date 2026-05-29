---
date: 2026-05-29
title: "Scaling Laws for Agent Harnesses — Effective Feedback Compute"
layout: post
author: "elvis (@omarsar0)"
url_source: "https://x.com/omarsar0/status/2060371848010019001"
snippet: "New research introduces Effective Feedback Compute (EFC), counting only feedback an agent can act on. Raw token/tool counts explain failure at R2 0.33-0.42; EFC pushes that to 0.99. Budgeting by useful feedback lifts success from 0.27 to 0.90 at the same compute."
relevance: "Directly relevant to how Claudie is built — sub-agents, workflows, tool budgets. A concrete tuning lever for Nityesh and a sharp data point for Mike's training on why more tokens does not equal a better agent."
---

# Scaling Laws for Agent Harnesses — Effective Feedback Compute

**Author:** elvis (@omarsar0)
**URL:** https://x.com/omarsar0/status/2060371848010019001
**Paper:** https://arxiv.org/abs/2605.29682

> Most harness tuning treats every token and tool call as if volume is all that counts. New research shows that most of it does not. The work introduces Effective Feedback Compute (EFC), a coordinate that counts only the feedback an agent can actually act on. Raw token and tool-call counts explain agent failure at R2 of 0.33 to 0.42. EFC pushes that to 0.99. Once you budget by useful feedback instead of raw volume, reallocation alone lifts success from 0.27 to 0.90 at the same compute.

## Why it's relevant
Directly relevant to how Claudie herself is built — sub-agents, workflows, tool budgets. The takeaway (budget by *actionable feedback*, not raw token/tool volume) is a concrete lever for Nityesh when tuning Claudie's agent/workflow harness, and a sharp data point for Mike's technical training on why "more tokens" ≠ "better agent." Turns harness design from guesswork into something predictable.
