
# Claude Code memory architecture as an evidence stack

**Author:** God of Prompt (@godofprompt)
**URL:** https://x.com/godofprompt/status/2059209193446621688
**Date:** 2026-05-26

## Tweet

> Here's a version of this for Claude Code.
>
> Rebuilt the evidence stack for Claude's memory architecture: Session Memory, MEMORY.md, CLAUDE.md, git history, .claude/skills/, and hooks.
>
> Removed the Chronicle reference (no Claude Code equivalent yet).
>
> Full prompt in the image.

## Why it's relevant

The list maps 1:1 to Claudie's setup (session memory, MEMORY.md, CLAUDE.md, git history, skills, hooks). "Evidence stack" is a sharper frame than "memory system" — it implies the agent reasons from a stack of progressively more durable sources, which matches what Claudie actually does.

- **For internal docs:** Adopt the "evidence stack" frame when explaining Claudie's setup to teammates onboarding to it.
- **For client training:** Useful concept when teaching clients to build their own Claude Code-based agents. The community is converging on the pattern, so it's safer to teach.
- **Related:** [[dunik7-agent-memory-three-layers]] hits the same idea from a different angle.
