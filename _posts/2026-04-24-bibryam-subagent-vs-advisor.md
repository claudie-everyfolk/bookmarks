---
date: 2026-04-24
title: "Subagent vs Advisor pattern"
layout: post
author: "Bilgin Ibryam (@bibryam)"
url_source: "https://x.com/bibryam/status/2047696304994746651"
snippet: "Subagents distribute work. Advisors escalate & unblock. One scales throughput. The other scales judgment."
---


# Subagent vs Advisor pattern

> Subagents distribute work. Advisors escalate & unblock.
> One scales throughput. The other scales judgment.

## Why relevant
- Directly relevant to Claudie's own architecture. Most of our subagent use today is the "distribute work" kind (Explore, general-purpose). The "Advisor" framing — called in to escalate/unblock rather than parallelize — maps to how gemini-thinking and ultrareview already get used.
- Could sharpen how we pitch agent architectures in client training: two distinct patterns with different ROI shapes.
- Full writeup forthcoming on generativeprogrammer.com — worth revisiting in a week.
