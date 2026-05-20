# Linghua Jin: Stop snapshotting your agent's knowledge — stream it

**Author:** Linghua Jin (@LinghuaJ)
**URL:** https://x.com/LinghuaJ/status/2049313685404062154
**Date:** 2026-04-28

> Many agent stacks today are built around periodic snapshots of their knowledge sources. The wiki is re-indexed overnight, the codebase is re-embedded on a cron, the CRM is re-pulled on a schedule. For long-running agents that may execute for hours at a time, a snapshot captured at the start of the run quickly drifts out of sync.
>
> Point-to-point webhooks have well-known limitations once more than one consumer is involved: no shared replay/backfill, no buffer for bursts, no common change schema.
>
> CocoIndex + Kafka takes a different approach: treats the knowledge layer as a stream of change events rather than a snapshot.

## Why it's relevant

Architectural pattern worth filing. Most of our client agent setups today are snapshot-based (nightly Drive re-index, weekly CRM pull). For larger clients running long-horizon agents — especially Applecart-style firms with live deal flow — a Kafka-backed change stream is the right pattern when one snapshot per night isn't fresh enough.

Not urgent for current engagements but worth raising with technical clients who ask "how do we keep our agents in sync with live data?" It's also a good positioning move: knowing the streaming pattern exists distinguishes us from cookie-cutter MCP-setup shops.
