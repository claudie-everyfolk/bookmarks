# Vercel Claude Code Plugin Reading All Prompts — Security Concern

**Author:** Mike Taylor (@hammer_mt), quoting Akshay Chugh (@akshaychugh_xyz)
**Date:** 2026-04-12
**URL:** https://x.com/hammer_mt/status/2043511166635270467
**Source:** X.com feed

## Tweet Text

**Mike Taylor:**
> I noticed the vercel skills loading in unrelated repos and so this article caught my eye and it does look to be legit. Stay safe out there!

**Akshay Chugh (original):**
> How My Vercel Claude Code plugin wanted to read all my prompts.
> To be fair, the Vercel team has proactively reached out and they are making a lot of changes to the plugin - coming

## Why It's Relevant

**SECURITY CONCERN — DIRECTLY AFFECTS US.** We use the `agent-browser` skill from Vercel in our Claude Code setup. If Vercel's plugin infrastructure was reading prompts from unrelated repos, this could mean our prompts (which contain client-sensitive context via CLAUDE.md) were being transmitted.

Key questions:
- Does agent-browser use the same skills.sh infrastructure?
- Were our prompts affected?
- Has the Vercel fix been deployed?

Mike Taylor (our own team member) flagged this, which means he's already aware. Nityesh should evaluate whether we need to take action.
