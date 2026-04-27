---
date: 2026-04-26
author: andrew pignanelli (@ndrewpignanelli) quoting Satyam (@KlausCodes)
url: https://x.com/ndrewpignanelli/status/2048394192104173789
topic: ai-memory-architecture
---

# AI memory startups need to pivot — git-backed files + grep are SOTA

> Everything is moving to git backed files accessible via grep-type-systems or semantic plus grep which isn't very defensible to offer as a service. In other words… the SOTA approaches.

## Why relevant
This is the architecture pattern Claudie already uses (~/.claude/projects/-/memory/ as markdown files, indexed by MEMORY.md, accessed via Grep). Validates the choice. Also relevant to:
- Lance Martin's piece on Claude Managed Agents memory (markdown files, no embeddings)
- Nicolas Bustamante: "LLMs just want to use primitive tools (read/write) over markdown files"

For client trainings: when clients ask "should we adopt a memory vendor (Mem0, Letta, etc.)?", the answer is increasingly "no — give your agent a filesystem and grep." Concrete, contrarian, quotable.
