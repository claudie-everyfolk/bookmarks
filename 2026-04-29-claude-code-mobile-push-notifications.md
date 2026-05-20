# Claude Code mobile push notifications shipped

**Author:** Wes Roth (@WesRoth) / ClaudeDevs
**URL:** https://x.com/WesRoth/status/2049383179950191075
**Date:** 2026-04-29

## Tweet
> Anthropic shipped mobile push notifications for Claude Code's "Remote Control" feature, allowing the terminal-based AI agent to ping users directly on their smartphones when it completes a task or requires human intervention.

## Why it's relevant
Directly relevant to Claudie's setup. We currently rely on Slack for notifications + the slack-bot wrapper for outbound messages. Native mobile push from Claude Code itself would let Natalia and Nityesh get pings without checking Slack — useful for long-running scheduled jobs (the daily Jean Claude refresh, the weekly kickoff, etc.). Worth Nityesh testing the pairing flow and considering whether it replaces or supplements the existing Slack-based notification path. The PushNotification deferred tool that's already in Claudie's environment may be wired to this.
