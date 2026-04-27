# Jerry Liu: Don't Overbuild Your Agent Stack

**Author:** Jerry Liu (@jerryjliu0) — CEO of LlamaIndex
**URL:** https://x.com/jerryjliu0/status/2041947224889077801
**Date:** 2026-04-09

## Tweet text

If you're an AI/agent builder, it's so important that you don't overbuild and overcommit on a specific toolset and infrastructure.

Frontier labs are shipping not just the models, but the harnesses and surrounding tooling such that your existing stack might be obsolete next week.

- e.g. if you had a super complex RAG stack, you may need to rip it out in favor of agents + sandboxes
- e.g. if you spent a lot of time building the sandbox and serving layer, you may not need to anymore if you can just bootstrap the product with Claude Managed Agents.

The tradeoff is completely dependent on how good out-of-the-box these proprietary agent wrappers get. Back when the OpenAI Agent SDK came out, most people did not switch from frameworks because they were simply more powerful. Nowadays tools like the Claude Agent SDK + managed agent services are getting way better.

(Quotes Claude's announcement of Managed Agents)

## Why it's relevant

Directly relevant to our platform risk on Claude Max. Also validates the approach of building on Claude Code's native capabilities rather than complex custom infrastructure. Good awareness for Nityesh — keep the stack lean, don't overbuild what Anthropic might ship natively.
