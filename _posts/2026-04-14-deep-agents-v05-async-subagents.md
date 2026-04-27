---
date: 2026-04-14
title: "Deep Agents v0.5: Async Subagents via Agent Protocol"
layout: post
author: "LangChain (@LangChain)"
url_source: "https://x.com/LangChain/status/2044086454230626733"
snippet: "deepagents 0.5 release  Async subagents - kick off background tasks on any Agent Protocol backed server while you continue to interact with the main agent. Start multiple background tasks in parallel, keep the conversation going, and collect results as they come in."
---
# Deep Agents v0.5: Async Subagents via Agent Protocol

**Author:** LangChain (@LangChain)
**Date:** 2026-04-14
**URL:** https://x.com/LangChain/status/2044086454230626733

## Tweet

> deepagents 0.5 release
>
> Async subagents - kick off background tasks on any Agent Protocol backed server while you continue to interact with the main agent. Start multiple background tasks in parallel, keep the conversation going, and collect results as they come in.

Blog: blog.langchain.com

## Why This Is Relevant

The async subagent pattern mirrors exactly how Claudie works — we kick off background Agent tool calls, run parallel research, and consolidate results. LangChain building this into a standardized protocol (Agent Protocol) means:

- The pattern we've been using is becoming an industry standard
- Could be useful for client training: "here's how async agent orchestration works"
- The Agent Protocol interop angle is interesting — could Claudie tasks be triggered by other agents?
