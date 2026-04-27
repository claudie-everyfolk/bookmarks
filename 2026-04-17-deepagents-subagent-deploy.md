# DeepAgents: Subagent Deployment Support

**Author:** Sydney Runkle (@sydneyrunkle)
**URL:** https://x.com/sydneyrunkle/status/2045209395881980276
**Date:** 2026-04-17

## Tweet
> we just shipped support for subagents with `deepagents deploy`! add an agents/ dir to your project with an AGENTS.md per specialized subagent. subagents are great for task delegation with isolated/optimized context

## Why it's relevant
The AGENTS.md pattern for subagent specialization is exactly what we do with Claudie's skill system. Each skill is essentially a specialized subagent with its own prompt and context. The "agents/ directory" convention is gaining traction as a standard pattern. Worth watching for convergence with Claude Code's native subagent support.
