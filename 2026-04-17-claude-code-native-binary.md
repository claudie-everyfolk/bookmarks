# Claude Code 2.1.113 Ships Native Binary

**Author:** ClaudeDevs (@ClaudeDevs)
**URL:** https://x.com/ClaudeDevs/status/2045267790018543736
**Date:** 2026-04-17

## Tweet

> Starting in v2.1.113, the Claude Code npm package ships the native binary instead of the JavaScript build. Same install command, faster startup, and the CLI no longer needs Node.js at runtime. If you need the JS build, pin to an earlier version.

## Why it's relevant

Directly affects how Claudie runs. Faster startup means faster scheduled job execution. No Node.js runtime dependency simplifies our Mac mini setup. Worth monitoring for any breaking changes in how we invoke `claude -p` from launchd scripts.

Also relevant to Mike's training on Claude Code workflows — participants no longer need Node.js installed to use Claude Code, which removes a friction point in workshop setup.
