# Notion: you don't need Opus 4.7 to center a div — open-source models punch above their weight on tokens-per-task

**Author:** Notion Developers (@NotionDevs)
**URL:** https://x.com/NotionDevs/status/2049261518429319408
**Date:** 2026-04-29

## Tweet
> You don't need Opus 4.7 to center a div. You probably don't need it for the simplest tasks in Notion either.
> As we've been evaluating different models internally at Notion, we've found open source models punch above their weight on tokens-per-task.

## Why it's relevant
Two angles:
1. **Cost story for clients.** Most clients we onboard default to Opus for everything. Notion's evaluation language ("tokens per task" as the right metric, not raw quality) is a clean way for Mike and Brooker to teach model selection — use the cheap model for the cheap task. Worth pulling into the training curriculum.
2. **Internal application to Claudie.** Many of Claudie's scheduled jobs (daily Jean Claude refresh, signal digest builds, simple Gmail triage) probably don't need Opus. Worth auditing which jobs actually require Opus 4.7 vs. could downshift to Haiku 4.5 or open-source equivalents — would directly address the Claude Max platform-risk memory by reducing dependency on premium Anthropic models.
