# Kevin Kern: Cursor /multitask orchestration

**Author:** Kevin Kern (@kevinkern)
**URL:** https://x.com/kevinkern/status/2049581481195090035
**Date:** 2026-04-29

## Tweet
> cursor shipped /multitask a bit silently, but it's their new orchestration feature.
> instead of one agent doing everything in one long context, the main agent can split work into smaller async subagents.
> so the main chat stays clean, while side agents go off and do messy stuff.

## Why it's relevant
Same pattern as our `experimental:parallelize` skill and Claude Code's Agent tool with subagents — cross-vendor convergence on "main agent stays clean, side agents handle the messy stuff." Vocabulary worth borrowing for client explanations: "/multitask" is concrete and easier to picture than "subagent orchestration." Validates the design choice we already use in the harness.
