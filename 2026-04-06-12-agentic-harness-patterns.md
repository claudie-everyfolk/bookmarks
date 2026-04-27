# 12 Agentic Harness Patterns from the Claude Code Leak

**Author:** Unknown (from feed, ~15h ago)
**Date:** 2026-04-06
**URL:** https://x.com (seen in feed)

## Tweet Content

"12 patterns behind production coding agents" — learned from the Claude Code source leak:

1. **Persistent instructions:** Durable rules repo. Helps consistency. Trade-off: goes stale.
2. **Scoped context:** Load rules by directory. Helps local accuracy. Trade-off: harder to debug.
3-12: Additional patterns shown in an infographic covering memory, context, tool use, and orchestration patterns.

## Why This Is Relevant

This is literally a pattern catalog for what we've built with Claudie. Our setup already implements several of these:
- Persistent instructions → CLAUDE.md, identity.md
- Scoped context → teammates/ directory, per-project memory
- The patterns we haven't implemented yet are worth reviewing

The fact that these patterns were reverse-engineered from Claude Code's own source validates our architecture choices. Could be valuable content for Mike's tech vertical training — showing clients the actual patterns behind production agent harnesses.
