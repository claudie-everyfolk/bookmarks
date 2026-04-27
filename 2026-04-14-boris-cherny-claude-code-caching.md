# Boris Cherny Responds to Claude Code Caching Complaints

**Author:** Om Patel (@om_patel5), quoting Boris Cherny (Claude Code creator)
**Date:** 2026-04-14
**URL:** https://x.com/om_patel5 (recent)
**Source:** X.com feed

## Tweet Text

> The creator of Claude Code just responded to the caching complaints.
> Here's what Boris Cherny said:
> "leaving an agent session open too long causes a full cache miss which inf..."

Also related — Arvid Kahl: "Claude Code silently dropping cache TTL from 1h to 5m is wild" (quoting @pedronauck)

## Why It's Relevant

Directly affects our Claude Max setup. Claudie runs long sessions via `claude -p` for scheduled jobs. If long sessions cause full cache misses, this explains potential token waste and performance degradation. The cache TTL reduction (1h → 5m) means our scheduled jobs that run for extended periods may be hitting cache misses more frequently.

**Action item:** Nityesh should evaluate whether our scheduled jobs are affected and whether we need to restructure session durations.
