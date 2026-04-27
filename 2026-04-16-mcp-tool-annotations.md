# MCP Tool Annotations as Risk Vocabulary — Pamela Fox (@pamelafox)

**Date:** 2026-04-16
**Author:** Pamela Fox
**URL:** https://x.com/pamelafox/status/2044827590066905385

## Tweet

Pamela Fox shares a blog post about MCP tool annotations like `readOnly` and `destructive`:
"Tool Annotations as Risk Vocabulary: What Hints Can and Can't Do"

## Why This Matters

We have multiple MCP servers (Google Workspace, qmd, Granola, etc.) and our access control system (teammates-access.md) already distinguishes between read and write operations. MCP tool annotations could formalize what we currently enforce through prompt-level instructions.

If MCP tools start declaring themselves as `readOnly` or `destructive`, Claude Code could potentially enforce Ring-based access controls at the tool level rather than relying on prompt instructions alone. This would be a more robust security model.

Relevant to: Nityesh (MCP architecture, access control), security considerations for client tool deployments
