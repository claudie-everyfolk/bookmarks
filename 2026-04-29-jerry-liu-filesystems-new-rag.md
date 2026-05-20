# Jerry Liu: Filesystems are the new default abstraction for agents (Mesa launch)

**Author:** Jerry Liu (@jerryjliu0), quoting Oliver (@olvrgln) on Mesa
**URL:** https://x.com/jerryjliu0/status/2049661223420223492
**Date:** 2026-04-29

> Filesystems are the new default abstraction for agents to interact with documents (the new RAG stack in 2026). The issue is actually figuring out how to productize this; you can't "productize" Claude Code over a local file system.

Quoting Oliver/Mesa launch: "Mesa: the most powerful filesystem ever built, designed specifically for enterprise AI agents. Every team building agents eventually hits the same wall: where do the files live? Not the chat history, the actual artifacts the agent works on."

## Why it's relevant

Strong shift signal. Last year RAG was the canonical pattern for giving agents context over documents. The 2026 thesis (and Claudie's actual implementation) is: agents read/write a real filesystem, not a vector DB. We already live this — Claudie's `~/work`, `~/projects`, `~/bookmarks` directories ARE the agent's working memory. qmd indexes them.

The productization gap Jerry calls out is exactly Every Consulting's territory: clients can't just give their team Claude Code over the local FS — they need an enterprise filesystem layer with auth, audit, sharing. If Mesa or similar gets traction, it becomes a stack we should know cold for client engagements (especially Bloomberg, NYT, hedge funds — heavy document workflows).
