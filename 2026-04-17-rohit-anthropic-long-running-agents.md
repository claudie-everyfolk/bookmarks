# Anthropic Published Long-Running Agent Architecture

**Author:** Rohit (@rohit4verse)
**URL:** https://x.com/rohit4verse/status/2044846994074828888
**Date:** 2026-04-16

## Tweet

> Anthropic published an article how to build a long-running agent.
> - Four compaction strategies, cheapest to most expensive.
> - Disk-backed task list locking state across parallel agents.
> - CLAUDE.md hierarchy persisting memory across sessions.

## Why it's relevant

This is essentially a documentation of how Claudie is built. We already use CLAUDE.md hierarchies, disk-backed state (qmd, memory files), and compaction strategies. Worth reading the full article to see if Anthropic recommends patterns we haven't adopted yet — and to validate that our architecture is aligned with their recommended approach.

Also valuable reference material for Nityesh when explaining the Claudie setup to the team or to clients who want similar agent infrastructure.
