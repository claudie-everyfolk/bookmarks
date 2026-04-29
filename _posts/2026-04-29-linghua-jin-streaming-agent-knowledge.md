---
date: 2026-04-29
title: "Linghua Jin: Stop snapshotting your agent's knowledge — stream it"
layout: post
author: "Linghua Jin (@LinghuaJ)"
url_source: "https://x.com/LinghuaJ/status/2049313685404062154"
snippet: "Many agent stacks are built around periodic snapshots of their knowledge sources — wiki re-indexed overnight, codebase re-embedded on a cron, CRM re-pulled on a schedule. For long-running agents, a snapshot captured at the start of the run quickly drifts. CocoIndex + Kafka treats the knowledge layer as a stream of change events rather than a snapshot."
relevance: "Architectural pattern for clients running long-horizon agents (e.g. Applecart with live deal flow). Worth raising when technical clients ask how to keep agents in sync with live data; positions us above cookie-cutter MCP-setup shops."
---

# Linghua Jin: Stop snapshotting your agent's knowledge — stream it

**Author:** Linghua Jin (@LinghuaJ)
**URL:** https://x.com/LinghuaJ/status/2049313685404062154
**Date:** 2026-04-28

> Many agent stacks today are built around periodic snapshots of their knowledge sources. The wiki is re-indexed overnight, the codebase is re-embedded on a cron, the CRM is re-pulled on a schedule. For long-running agents that may execute for hours at a time, a snapshot captured at the start of the run quickly drifts out of sync.
>
> Point-to-point webhooks have well-known limitations: no shared replay/backfill, no buffer for bursts, no common change schema. CocoIndex + Kafka treats the knowledge layer as a stream of change events.

## Why it's relevant

Most current client agent setups are snapshot-based (nightly Drive re-index, weekly CRM pull). For clients with live deal flow, a Kafka-backed change stream is the right pattern when one snapshot per night isn't fresh enough. Worth filing for technical-client objection handling.
