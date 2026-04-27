---
date: 2026-04-11
title: "Claude Managed Agents — Vault Scope Security Concern"
layout: post
author: "Daniel San (@dani_avila7)"
url_source: "https://x.com/dani_avila7/status/2042708271904256039"
snippet: "Been testing Claude Managed Agents  Here's my feedback: Vaults store OAuth tokens outside the sandbox, the agent never handles them directly  The problem, vaults are workspace-scoped  Anyone with workspace access, via API key or the Console, can reference your vaults and use your credentials in their own sessions"
relevance: "AI Security. Anthropic's Managed Agents use \"vaults\" for OAuth token storage, but these are workspace-scoped — meaning anyone with workspace API key access can reference another user's vault credentials. This is a lateral privilege escalation vector in multi-user workspaces. Directly relevant to our setup since we use Claude for client work with sensitive API access. If Anthropic introduces Managed Agents to our workflow, vault scoping would need careful evaluation."
---
# Claude Managed Agents — Vault Scope Security Concern

**Author:** Daniel San (@dani_avila7)
**URL:** https://x.com/dani_avila7/status/2042708271904256039
**Date:** 2026-04-11

## Tweet

> Been testing Claude Managed Agents
>
> Here's my feedback:
> Vaults store OAuth tokens outside the sandbox, the agent never handles them directly
>
> The problem, vaults are workspace-scoped
>
> Anyone with workspace access, via API key or the Console, can reference your vaults and use your credentials in their own sessions

## Why it matters

**AI Security.** Anthropic's Managed Agents use "vaults" for OAuth token storage, but these are workspace-scoped — meaning anyone with workspace API key access can reference another user's vault credentials. This is a lateral privilege escalation vector in multi-user workspaces.

Directly relevant to our setup since we use Claude for client work with sensitive API access. If Anthropic introduces Managed Agents to our workflow, vault scoping would need careful evaluation.
