# Human in the Loop / Approval Flows for Agents

**Author:** Ashpreet Bedi (@ashpreetbedi)
**URL:** https://x.com/ashpreetbedi (Apr 4, 2026)
**Bookmarked:** 2026-04-04

## Tweet

"Sharing my learnings on human in the loop / approval flows for agents. Whether you implement them today or not, these concepts are critical to understand and will shape how you design your system."

Three types of actions an agent can take:
1. No approval needed
2. User approval required
3. (more in thread)

## Why This Is Relevant

Directly maps to Claudie's access control architecture:
- **Ring 0/1/2/3 system** — Claudie already implements tiered approval flows (Ring 0 hard-never, Ring 1 full access, Ring 2/3 restricted)
- **Permission modes** — `--permission-mode dontAsk` vs `--dangerously-skip-permissions` are exactly this framework in practice
- **Client training** — when teaching teams to build agents, approval flows are the #1 concern for enterprise. This is a good reference for structuring that conversation.
- **Validates Claudie's design** — the "three types of actions" framing maps to how we already think about risky vs safe operations
