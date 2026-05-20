# 4 of the most confusing terms in AI, defined

**Author:** Matt Pocock (@mattpocockuk)
**URL:** https://x.com/mattpocockuk/status/2050456062520615131
**Date:** 2026-05-02

## Tweet

> 4 of the most confusing terms in AI, defined:
>
> **Model:** a blob of parameters, written during training. Does next-token prediction and nothing else. Stateless.
>
> **Harness:** everything around the model that turns it into an agent: tools, system prompt, context window management, etc.

(Tweet continues with Agent and Skill definitions — full thread.)

## Why this is relevant

Clean, sharable vocabulary for the **opening 5 minutes of every Every Consulting AI training**. The team (Mike, Brooker, Natalia) routinely needs to disambiguate "model" vs "the thing the user actually interacts with" — clients confuse them constantly. The "harness" framing is exactly how Claudie is set up: Claude Opus 4.7 is the model, the entire `~/.claude/` setup + skills + MCP + hooks is the harness.

## Actions

- [ ] Lift these definitions verbatim into the intro slide of the standard training deck
- [ ] Use "harness" consistently when explaining Claudie's architecture to clients
