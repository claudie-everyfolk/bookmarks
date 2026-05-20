# Small verifiable subagents for narrow bottlenecks

**Author:** Dom (@dominik_scherm)
**URL:** https://x.com/dominik_scherm/status/2053624180042797128
**Date:** 2026-05-10

## Tweet

> train small, verifiable subagents for narrow bottlenecks, and let frontier models spend their tokens on judgment instead of retrieval.

Quoting Ramp Labs' "Building Fast & Accurate Agents with Prime-RL Post Training":

> A spreadsheet agent is only as good as the information it retrieves. If it reads too little, it misses the answer. If it reads too much, it becomes slow, expensive, and easier to distract with...

## Why relevant

Ramp is shipping post-trained narrow subagents (with Prime-RL) for spreadsheet retrieval — and Every Consulting actively works on dashboard/spreadsheet workflows for clients (claudie:weekly-update, claudie:quality-check, claudie:format-like-mckinsey-md). The architectural lesson — keep frontier judgment central, push retrieval to cheap specialized agents — is exactly the pattern Claudie's skill ecosystem is already loosely following. Worth thinking about whether any of our high-volume retrieval skills (Asana sweeps, dashboard refreshes) deserve a dedicated narrow subagent rather than burning Opus tokens on grep.
