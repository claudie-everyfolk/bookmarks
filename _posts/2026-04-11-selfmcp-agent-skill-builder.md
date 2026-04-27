---
date: 2026-04-11
title: "selfMCP — MCP Server That Lets Claude Build Its Own Skills"
layout: post
author: "Yohei Nakajima (@yoheinakajima)"
url_source: "https://x.com/yoheinakajima/status/2042726503809716426"
---

# selfMCP — MCP Server That Lets Claude Build Its Own Skills

**Author:** Yohei Nakajima (@yoheinakajima)
**URL:** https://x.com/yoheinakajima/status/2042726503809716426
**Date:** 2026-04-11

## Tweet

> haha cool, this worked. an MCP server that allows Claude to build its own reusable skills
>
> https://github.com/yoheinakajima/selfMCP (1473 LoC)
>
> basically a server with skills to CRUD skills
>
> in this video, i use claude to create an openai image generation skill and trigger it

## Why it matters

**Agent Infrastructure.** This is an MCP server with CRUD operations for skills — the agent can create, read, update, and delete its own tool definitions at runtime. This is conceptually similar to how we already use the skill-creator skill, but packaged as an MCP server that any agent can connect to.

Worth watching as a pattern — self-modifying tool registries could make agents more adaptive without requiring manual skill authoring.
