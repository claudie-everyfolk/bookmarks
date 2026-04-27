# Claude Code Architecture Extracted into Open Source Framework

**Author:** Ivan Burazin (@ivanburazin)
**URL:** https://x.com/ivanburazin/status/2040112100597506107
**Date:** 2026-04-09 (posted Apr 5)

## Tweet text

After the Claude Code source code leak, a former PM extracted its multi-agent orchestration system into an open source model agnostic framework.

He studied the architecture, focused on the multi-agent orchestration layer (the coordinator that breaks goals into tasks, team system, message bus, task scheduler with dependency resolution), and reimplemented these patterns from scratch as a standalone open source framework without infringing on Anthropic's code.

The result is what @jackChen calls an "open-multi-agent". Unlike claude-agent-sdk, which spawns a CLI process per agent, this runs entirely in-process and can be deployed anywhere (serverless, Docker, CI/CD).

## Why it's relevant

Understanding Claude Code's internal architecture helps us understand the tool we've built Claudie on. The multi-agent orchestration pattern (coordinator → tasks → team system → message bus → dependency resolution) is the same pattern we use with sub-agents in our skills. Also relevant if we ever need to consider alternatives to Claude Code.
