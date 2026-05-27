---
date: 2026-05-26
title: "Anthropic: How we contain Claude across products (sandboxing)"
layout: post
author: "Anthropic (@AnthropicAI)"
url_source: "https://x.com/AnthropicAI/status/2059351260243919269"
snippet: "The access and permissions we grant agents should evolve with their capabilities. In our own products, we set these parameters through sandboxing, which limits the scope of any potentially destructive actions."
relevance: "Engineering-blog rationale for how Anthropic scopes agent permissions. Directly relevant to Claudie's own architecture (we already use permission modes, hooks, and an allowlist) and to client engagements where the question 'how do we let an agent take real actions safely?' comes up — especially financial-services clients."
---

## Tweet
> New on the Engineering Blog: The access and permissions we grant agents should evolve with their capabilities. In our own products, we set these parameters through sandboxing, which limits the scope of any potentially destructive actions.
>
> Read more: How we contain Claude across products

## Why it's relevant
First-party Anthropic engineering rationale for how to scope agent permissions. Useful context for:
- Claudie's own infrastructure (permission modes, hooks, allowlists) — confirms we're on the right track
- Client conversations about safely deploying agents that take real actions (especially regulated clients)
- Training material on "how to deploy agents responsibly"
