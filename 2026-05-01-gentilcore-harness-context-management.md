# Harness design = scaling context management

**Author:** Tony Gentilcore (@tonygentilcore)
**Date:** 2026-05-01
**URL:** https://x.com/tonygentilcore/status/2050225487931183566

## Tweet

"When Anthropic leaked Claude's system prompt, it reset the playing field for harness design. Good harness design is starting to look a lot like good context management. Figuring out what the agent sees, when it sees it, and how to steer it to complete the task. That is not a coincidence.

In the enterprise, you are not dealing with 6 tools. You are dealing with hundreds of reads and writes across an entire organization. Tools need to be called programmatically. Work needs to be isolated to sub-agents to actually get done. The harness's role has evolved from simple execution to scaling context management."

## Why it's relevant

Yet another reinforcement of the harness theme that's recurring across the past two weeks (Bergum, Vtrivedy, Cursor SDK, elvis/DAIR). The new specific claim: "harness design = context management." That reframes harness work for clients — it's not glue code, it's the discipline of deciding what an agent sees and when. Enterprise scale means hundreds of tools and aggressive sub-agent isolation, not one big context.

For Every Consulting clients (Bloomberg, NYT, hedge funds): the right unit of work is "what does this agent need to see for this task?" — and the answer is almost never "everything in our system." This connects directly to Mike's Claude Code training and Brooker's process-mapping work — process maps ARE context-management designs.
