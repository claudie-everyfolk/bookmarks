# Claude Code 2.1.139: /goal command for multi-turn task completion

**Author:** Claude Code Changelog (@ClaudeCodeLog)
**Date:** 2026-05-11
**URL:** https://x.com/ClaudeCodeLog/status/2053913625983692979

## Tweet text
"Claude Code 2.1.139 has been released.

50 CLI changes, 1 system prompt change

Highlights:
• Added /goal command to run tasks across turns until a set completion condition, with live elapsed/turns/tokens
• System prompt compaction is now silent (no trimming alert)..."

Companion: Chris Hayduk's "Using Codex Goals Effectively" — Codex shipped /goal at the same time. Anthropic + OpenAI converged on the same primitive.

## Why it's relevant
A native multi-turn-until-done primitive directly replaces Claudie's `/loop` skill for many use cases. Today /loop polls; /goal runs continuously with a completion predicate. This may simplify Claudie's autonomous workflows (daily pipeline refresh, dashboard updates, etc.).

- **Nityesh** — evaluate /goal as a drop-in for several /loop-driven jobs; live elapsed/turns/tokens display is exactly what we hand-rolled.
- Connects to the broader signal that "set a goal, return when done" is becoming the agent primitive both vendors converge on.
