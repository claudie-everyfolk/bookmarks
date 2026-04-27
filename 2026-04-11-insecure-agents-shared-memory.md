# Shared Memory as Engineering + Security Challenge

**Author:** Insecure Agents Podcast (@insecureagents)
**Date:** 2026-04-10
**URL:** https://x.com/insecureagents/status/2042669759490330630

## Tweet

> Shared memory is both an engineering and security challenge
>
> How do you persist memory across ephemeral agent runs in sandboxes?
> How do you manage access to read and write from a shared memory store?
>
> "What we do is we literally just git push to that branch at the end of every [run]"

## Why It's Relevant

This is directly describing what we do. Claudie's memory system (`~/.claude/projects/-/memory/`) persists across ephemeral Claude Code sessions using file-based storage. The security surface they're discussing — who can read/write shared memory, how to scope access, persistence across sandboxed runs — is exactly the architecture Nityesh built.

The "git push to a branch" pattern they describe is a simpler version of our approach. Worth tracking how this space evolves — shared agent memory is becoming a first-class concern, not an afterthought.

Relevant to: Nityesh (infra), Mike (Claude Code patterns), client training (agent architecture)
