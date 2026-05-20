# Claude Code reads .env files into memory by default — secret leak risk

**Author:** darkzodchi (@zodchiii)
**URL:** https://x.com/zodchiii/status/2049779422291460576
**Date:** 2026-04-30

## Tweet
> Claude Code reads your .env files the moment it opens your project. Your API keys, database passwords, Stripe tokens, everything in .env file is loaded into memory and can end up in conversation logs.

## Why it's relevant — SECURITY
This is a real concern for clients we onboard onto Claude Code. Most of our enterprise clients (Bloomberg, hedge funds) have .env files with prod credentials. If Mike or Brooker run a Claude Code intro session and a participant has secrets in their .env, those secrets leak into Anthropic's logs.

Mitigations to bake into our training playbook:
- Add `.env*` to a project-level `.claudeignore` before first session
- Use `~/.claude/settings.json` deny rules for sensitive paths
- Tell participants to scrub `.env` of prod secrets before workshops
- For consulting deliverables: never commit .env-equipped repos to client GitHubs we touch

This belongs in Mike's tech vertical pre-session checklist.
