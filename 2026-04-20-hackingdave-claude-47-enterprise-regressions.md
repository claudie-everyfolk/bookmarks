---
date: 2026-04-20
author: Dave Kennedy (@HackingDave) + Boris Cherny (@bcherny) reply
urls:
  - https://x.com/HackingDave/status/2046312851648987335
  - https://x.com/bcherny/status/2046366854227312896
topic: claude-4.6/4.7 regressions, enterprise risk
---

# Enterprise dev-team reports Claude 4.6/4.7 introducing bugs and security issues, worse than Opus 4.5

Kennedy: entire dev team rolling back. Boris Cherny (Anthropic) replies asking for /feedback IDs, notes recent harness changes — says last known issue fixed in latest.

## Relevance
- We run almost entirely on Opus 4.7 (1M). Worth tracking whether our own generated code quality has degraded — if clients push back, we have receipts that this is an industry-observed issue, not a Claudie-specific bug.
- Connects to the "Claude Max platform risk" memory — we depend on a single vendor, so regressions hit us directly.

## Action
- Monitor thread for specific failure modes
- If a client reports degraded quality, link to this thread as context + upgrade / feedback trail
