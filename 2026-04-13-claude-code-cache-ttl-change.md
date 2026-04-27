# Claude Code Cache TTL Changed from 1hr to 5min — Cost and Performance Implications

**Date:** 2026-04-13
**Authors:** Daniel Nguyen (@daniel_nguyenx), Boris Cherny (@bcherny)
**URLs:** https://x.com/daniel_nguyenx, https://x.com/bcherny

## What happened

Anthropic reportedly changed Claude Code's prompt cache TTL from 1 hour to 5 minutes in March, causing significant quota and cost inflation for users.

Boris Cherny (from Anthropic?) adds nuance: prompt caching costs more for cache writes and less for cache reads. Whether you benefit depends on usage pattern — context window size, whether queries come from main agent or subagents, etc.

## Why this matters

This directly affects our operations. Claudie runs on Claude Code Max, and cache behavior impacts how efficiently we use our quota. Understanding the cache mechanics helps us:
- Optimize how subagents are structured (do they benefit from caching?)
- Schedule token-intensive jobs better
- Advise clients on Claude Code cost management
- Understand why usage limits might feel tighter than before
