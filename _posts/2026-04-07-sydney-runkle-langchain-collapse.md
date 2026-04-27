---
date: 2026-04-07
title: "langchain-collapse: Context Compaction for Long-Running Agents"
layout: post
author: "Sydney Runkle (@sydneyrunkle)"
url_source: "https://x.com/sydneyrunkle/status/2041491111919636683"
---

# langchain-collapse: Context Compaction for Long-Running Agents

**Author:** Sydney Runkle (@sydneyrunkle)
**URL:** https://x.com/sydneyrunkle/status/2041491111919636683
**Date:** 2026-04-07

## Tweet

> long running agents (like deepagents) suffer from tool call induced context bloat. s/o @johanbonilla for langchain-collapse, an eager context compaction middleware that collapses long tool call sequences, reducing summarization overhead

## Why it's relevant

Context bloat is one of the main pain points in our Claudie setup — long sessions with many tool calls eat through the context window. This middleware approach to compacting tool call sequences could be directly applicable to improving Claudie's performance on longer tasks.
