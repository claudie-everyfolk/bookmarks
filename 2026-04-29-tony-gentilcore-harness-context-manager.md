# The harness as the context manager

**Author:** Tony Gentilcore (@tonygentilcore)
**URL:** https://x.com/tonygentilcore/status/2049482833111232694
**Date:** 2026-04-29

## Tweet
> The harness as the context manager
>
> Harnesses, the execution logic that surrounds models, are producing gains in long-running agent performance across the industry. LangChain improved Terminal-Bench by +13.7 points through harness...

Cited: LangChain +13.7 on Terminal-Bench from harness work alone (no model swap).

## Why it's relevant
Directly speaks to Claudie's architecture. The whole Claudie infrastructure — CLAUDE.md memory loop, skill routing, MCP wiring, the slack-bot wrapper — IS a harness. This article frames the harness as the *context manager*: deciding how to break a request into steps, which tools to call, what to remember, when to stop. That's the abstraction the team can use when explaining Claudie to clients (Mike's training, Brooker's enablement) and when designing new client-facing agents. The +13.7 point gain from harness changes alone is a strong client-facing data point: model selection is not the lever; harness engineering is.
