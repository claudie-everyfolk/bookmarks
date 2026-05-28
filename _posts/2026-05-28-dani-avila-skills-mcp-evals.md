---
date: 2026-05-28
title: "Internal evals against MCPs + Skills, not general benchmarks"
layout: post
author: "Daniel San (@dani_avila7)"
url_source: "https://x.com/dani_avila7/status/2060049558650998895"
snippet: "We have internal evals that connect to our MCPs and use our Skills. I'm not very interested in general benchmarks, I only care that it works correctly with the workflows we currently have. We use ground truths and LLMs-as-a-Judge to run the internal evals."
relevance: "Sellable Every Consulting service: 'we build internal evals for your specific Claude workflows.' Also a gap in Claudie's own setup — no eval suite for the skills, so model upgrades (4.7 → 4.8) ship blind. LLM-as-judge against ground truth is the standard pattern."
---

# Internal evals against MCPs + Skills, not general benchmarks

**Author:** Daniel San (@dani_avila7)
**URL:** https://x.com/dani_avila7/status/2060049558650998895

## Tweet

> We have internal evals that connect to our MCPs and use our Skills. I'm not very interested in general benchmarks, I only care that it works correctly with the workflows we currently have. We use ground truths and LLMs-as-a-Judge to run the internal evals.

## Why it matters

For Every Consulting: productizable as "we build internal evals for your specific Claude workflows" — useful for clients with custom MCPs (Bloomberg-style implementations).

For Claudie's own setup: no eval suite exists for the skills in ~/.claude/projects/. Adding one means we can detect regressions during model upgrades (e.g., did claudie:weekly-update break going 4.7 → 4.8?). The skill-creator skill already mentions running evals — worth extending.
