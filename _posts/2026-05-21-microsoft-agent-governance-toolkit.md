---
date: 2026-05-21
title: "Microsoft AI Agent Governance Toolkit"
layout: post
author: "Bilgin Ibryam (@bibryam)"
url_source: "https://x.com/bibryam/status/2057126955388993990"
snippet: "AI Agent Governance Toolkit - by Microsoft. Runtime governance for AI agents through deterministic policy enforcement, zero-trust identity, execution sandboxing, and SRE for autonomous agents. Covers all 10 OWASP Agentic risks with 13,000+ tests."
relevance: "Microsoft formalized the patterns Every has been improvising — runtime policy enforcement, zero-trust agent identity, sandboxing, OWASP Agentic risk coverage. A hardening reference for Claudie's own architecture (gaps: no sandboxing, no audit trail) and a credible artifact for advising Woodline and other finance clients deploying agents."
---

# Microsoft AI Agent Governance Toolkit

**Author:** Bilgin Ibryam (@bibryam)
**Tweet:** https://x.com/bibryam/status/2057126955388993990
**Repo:** https://github.com/microsoft/agent-governance-toolkit

> AI Agent Governance Toolkit - by Microsoft. Runtime governance for AI agents through deterministic policy enforcement, zero-trust identity, execution sandboxing, and SRE for autonomous agents. Covers all 10 OWASP Agentic risks with 13,000+ tests.

## Why it's relevant

Microsoft just formalized the exact patterns Every has been improvising — runtime policy enforcement, zero-trust agent identity, sandboxing, OWASP Agentic risk coverage. It's both a hardening reference for Claudie's own architecture and a credible artifact for advising finance clients who deploy agents.

## Relevance report

**The toolkit, in one line:** Microsoft's `agent-governance-toolkit` formalizes exactly the patterns Every Consulting has been improvising — runtime policy enforcement, zero-trust agent identity, sandboxing, and OWASP Agentic risk coverage.

**1. Maps directly onto Claudie's own architecture.** Claudie already runs a partial version of every concept. `teammates/teammates-access.md` is a zero-trust identity + ring-based deny-list model (Ring 0 hard-nevers, supervisor-only edits). `CLAUDE.md` already splits `--permission-mode dontAsk` (least-privilege default) vs. `--dangerously-skip-permissions` (Nityesh/Natalia authorization required) — a deterministic policy split. `claudie-send-email` enforces an @every.to-only hard boundary via hook. **Gaps the toolkit would close:** no execution sandboxing (Claudie runs unsandboxed on the Mac mini with full home-dir, gws, and Keychain access — see Signal Digest entry `43-axelbitblaze-claude-code-attack-surface.md`); no SRE/observability layer for the launchd jobs; no audit trail; access control is enforced in prompt + bot.py code, not at runtime. Ring 0's anti-prompt-injection rule is policy text, not enforcement.

**2. Nityesh has repeatedly worked this exact problem.** Past sessions show him building `RESTRICTED_USERS` → `dontAsk` logic into `bot.py` and a settings.json deny-list "sandbox" for non-Ring-1 users. He is the primary recipient — this toolkit is a reference architecture for hardening Claudie's gaps.

**3. Client engagement: Woodline Partners (hedge fund).** The Woodline technical discovery call is the strongest fit — Woodline runs ~100-110 Copilot Studio agents, requires compliance review before deployment, uses DSPM with prompt-injection detection, and had General Counsel + deputy head of compliance in the room. They are literally building agent governance. The toolkit is a credible reference when Every advises them. Also relevant to Bloomberg and other finance/PE clients.

**4. Who should see it:** **Nityesh** (harden Claudie; map gaps). **Natalia** — positioning: "AI governance consultant," not prompt engineer. **Brooker** — finance-client governance framing for Woodline. **Mike** — a module for dev-productivity training on securing coding agents.
