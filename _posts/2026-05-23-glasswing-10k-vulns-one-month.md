---
date: 2026-05-23
title: "Project Glasswing: 10,000+ Critical Vulnerabilities Found in One Month"
layout: post
author: "Anthropic / Andrew Curran (@AndrewCurran_) / NIK (@ns123abc)"
url_source: "https://x.com/ns123abc/status/2057930703258427664"
snippet: "Anthropic just dropped the first Project Glasswing update. Claude Mythos found 10,000+ critical vulnerabilities in ONE month: Cloudflare 2,000 bugs (400 high/critical severity); Mozilla 271 vulnerabilities in Firefox 150 — 10x more than Firefox 148. Government expansion next."
relevance: "Converts prior Glasswing strategy posts (Signal Digest #28/#34/#51) into a citable throughput number. Direct unlock for Mike's Thumbtack/Bloomberg follow-up + Repo Hardening Skill. The 10x Firefox jump is the data point that lands with a CISO. Also the cleanest 'finding ≠ fixing' diagnostic for a security-discovery angle."
---

# Project Glasswing — One-Month Throughput Update

**Authors:** Anthropic (@AnthropicAI); coverage by Andrew Curran (@AndrewCurran_), NIK (@ns123abc)
**Tweets:** https://x.com/AndrewCurran_/status/2057912254490882053 · https://x.com/ns123abc/status/2057930703258427664
**Date:** 2026-05-22

> Anthropic: Last month we launched Project Glasswing, our collaborative AI cybersecurity initiative. Since then, we and our partners have found more than ten thousand high- or critical-severity vulnerabilities in essential software.
>
> NIK: Cloudflare: 2,000 bugs, 400 high/critical severity. Mozilla: 271 vulnerabilities in Firefox 150 — 10x more vulnerabilities found in Firefox 148.
>
> Andrew Curran: Next, we will work with critical partners — including US and allied governments — to expand Project Glasswing to additional partners.

## Why it's relevant

Three things changed with this update:

1. **Capability → throughput.** Signal Digest #28, #34, #51 established Glasswing as a strategic shift. This is the first hard volume number — and it's an order of magnitude beyond conservative estimates.
2. **10x Firefox jump.** Same Mythos, two sequential Firefox releases, 10x more vulnerabilities surfaced. The capability is improving inside the month, not just at the model level.
3. **Government expansion announced.** "US and allied governments" is the tell that classified deployment precedes commercial availability.

## Detailed relevance report

### Who on the team is most relevant

**Mike Taylor (Tech Vertical Lead) — primary owner.** Per `teammates/mike.md`: teaches Cursor/Claude Code/dev productivity. Signal-digest entries #28 and #34 explicitly nominate him: *"Mike Taylor's evals on Claude Mythos — our own team member is testing this model"* and *"Mike's tech vertical should include security tooling. A live demo of Mythos finding real vulnerabilities would be a bootcamp highlight."* Entry #51 reinforces it for his curriculum.

**Brooker (Non-Tech/Finance Vertical Lead) — secondary, pending sign-off.** Entry #51: *"Brooker's non-tech vertical needs a simplified version: 'AI can now find security holes as well as a professional hacker.'"* His finance audience makes Goldman/JPM Glasswing adoption load-bearing — but #51 noted this needs Natalia/Brooker sign-off.

**Nityesh — internal use.** Entry #28 flagged him to run Mythos against Claudie's own codebase given the file-exfiltration risk surface. He already audited axios/supply chain in April.

### Existing work this connects to

- **`projects/every-consulting-reports/claudie-security-briefing.html`** — our own layered framework for an always-on AI employee. Glasswing throughput is the citation that retroactively backs that briefing.
- **Thumbtack engagement** — Mike's trainer, survey flagged "job security concern (2.5)" and "low trust in output accuracy." Glasswing is the natural follow-up artifact for the continuing relationship.
- **Bloomberg + finance clients** named in entries #28/#34/#51 as ready-to-receive audience.
- **Repo Hardening Skill** (`bookmarks/2026-05-12-kevin-kern-repo-hardening-skill.md`) — already proposed bundling with Trail of Bits guide as a tech-vertical add-on. Cloudflare/Mozilla numbers are the credibility data the proposal lacked.

### Concrete actions this could inform

1. **DM Mike** with the tweet + a one-line pitch to ship a "Mythos demo + Repo Hardening" module to Thumbtack / Bloomberg follow-up. Per his teammate profile he prefers channel-based research/architecture work — this is his sweet spot.
2. **One-liner for Natalia's morning brief**: throughput data point for finance-client discovery angles. Don't surface unless it routes to a deal.
3. **Update entries #28, #34, #51** in Signal Digest with the throughput numbers (now done — see entry #92).
4. **Hold on Brooker** — needs Natalia/Brooker sign-off per #51's caveat.

### Prior Signal Digest entries this connects to

- **#28** anthropic-project-glasswing-claude-mythos (Apr 7, KEY SHIFT) — capability launch
- **#34** anthropic-project-glasswing-ai-vuln-discovery (Apr 7, KEY SHIFT) — strategic positioning
- **#51** mythos-first-ai-cyber-range-complete (Apr 13, KEY SHIFT) — 72% Firefox zero-day rate, Goldman + JPM adoption
- **#45** levie-security-jevons-paradox (Apr 12, KEY SHIFT) — the "more findings = more demand for human judgment" framing this operationalizes
- **#78** anthropic-claude-security-launch — productization angle
- **#92** glasswing-throughput-10k-vulns (today) — this update
