# Kevin Kern — Repo Hardening Skill After Supply-Chain Incidents

**Author:** Kevin Kern (@kevinkern)
**URL:** https://x.com/kevinkern/status/2054295740739174627
**Date:** 2026-05-12

> after these supply-chain incidents, I summarized some basic repo hardening checks into a skill.
>
> It checks the repo for:
> - pnpm 11+ package manager policy
> - release-age gates and lockfile hardening
> - risky dependency specs like latest, git, http, file:
> - unreviewed dependency lifecycle scripts
> - unsafe CI install, cache, publish, and secret patterns
> - optional npm supply-chain incident
>
> practical first pass for finding common repo hardening gaps. I ran it with GPT-5.5 High.

## Why it's relevant

Fourth supply-chain signal in ~5 weeks (axios → OpenAI compromise → ClawHub malicious skills → now this). A ready-made hardening skill is exactly the artifact Mike Taylor can ship as a tech-vertical deliverable, and the kind of thing we should run on our own repos (gws, slack-bot, applecart-pptx, openclaw) before pitching to clients.

## Relevance report

**Who cares most:**
- **Mike Taylor** (Tech Vertical Lead) — primary owner. Teaches Cursor/Claude Code/dev-productivity. A pre-built hardening skill is the kind of take-home deliverable that fits his engagements.
- **Nityesh** — runs our own npm/pip surface. Already audited axios exposure in April. Would want this for internal repos.
- **Natalia** — one-liner: "Mike could ship this as a deliverable to tech clients."

**Existing thread this connects to:**
- `bookmarks/2026-04-02-axios-supply-chain-attack.md` — original axios/crypto-js writeup
- `bookmarks/2026-04-10-openai-axios-security-vulnerability.md` — OpenAI disclosed compromise in macOS app
- `bookmarks/2026-04-13-hackinglz-ciso-claude-code-enterprise-controls.md` — CISOs needing dev-workstation supply-chain controls
- `bookmarks/2026-04-14-vercel-skills-prompt-reading.md` — Vercel plugin reading prompts; affected agent-browser
- `bookmarks/2026-04-11-claude-code-security-hardening.md` — Trail of Bits 3-level hardening guide (closest precedent)
- `discoveries/signal-digest/entries/57-clawhub-malicious-skills-supply-chain.md` — 824 malicious ClawHub skills; flagged "supply chain conversation now" for finance clients

Past internal audits: sessions `029b730e`, `4bf4e883`, `1e436cd5` (gws axios check), `decb927c`, `099ac7d8` (security briefing), `ac37a499` (slopsquatting).

**Concrete actions:**
1. Fork/clone the skill into `every-consulting` plugin marketplace alongside `simplify` and `security-review`. Pattern matches `bookmarks/2026-04-25-ksimback-tech-debt-skill.md`.
2. Bundle with Trail of Bits 3-level guide as a tech-vertical add-on for Bloomberg + finance clients (already flagged in discovery #57).
3. Run on our own repos first — gws, slack-bot, applecart-pptx, openclaw, granola-mcp-server, every-consulting.
4. DM Mike with this signal + four prior bookmark links. He's the buyer.
