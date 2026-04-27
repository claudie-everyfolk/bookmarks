# OpenCode: Guided AGENTS.md Setup

**Author:** nexxel (@nexxeln)
**Date:** 2026-04-01
**URL:** https://x.com/nexxeln/status/2039378745329602871

## Tweet

> in the next release of @opencode
>
> /init becomes a guided AGENTS.md setup
>
> it reads the repo, figures out the stuff agents actually need to know, and asks a couple targeted questions when the important bits aren't obvious from the codebase

## Also: OpenCode reaches 6.5M monthly actives

**Author:** dax (@thdxr)
**URL:** https://x.com/thdxr/status/2039341616868065381

> 1 month later
> 6,500,000 monthly actives

## Why it's relevant

**Competitive intelligence.** OpenCode is the main open-source competitor to Claude Code. Two data points here:

1. **6.5M MAU in 1 month** — significant adoption. This is the tool our developer-focused clients will compare against.
2. **Guided AGENTS.md setup** — smart onboarding UX. Their /init command reads the repo and generates agent context automatically. Compare to Claude Code's CLAUDE.md which requires manual setup. This is the kind of developer experience improvement that could influence adoption.

Relevant to: Mike Taylor's developer training, Nityesh's agent architecture work, competitive positioning.

## Detailed Competitive Intelligence Report

### OpenCode 6.5M MAU vs. Claude Code

OpenCode is free and open-source — 6.5M MAU removes all friction. Claude Code is subscription-gated ($20-$200/mo). The comparison is closer to VS Code (free, massive adoption) vs. a paid IDE. However, **6.5M developers now have muscle memory in a tool that is not Claude Code**, and that is a real competitive risk for bottom-up enterprise adoption. Developers who set up repos with AGENTS.md may resist switching to CLAUDE.md.

### Guided AGENTS.md vs. CLAUDE.md

**The gap:** OpenCode is solving the onboarding problem that Claude Code hasn't addressed. Claude Code's memory architecture is vastly more sophisticated (three-layer system, AutoDream consolidation, hypothesis-to-rule promotion via Pawel Huryn's framework), but sophistication doesn't help if developers never get past the first step. OpenCode targets the 80% who never write a CLAUDE.md at all.

**Key insight:** The configuration layer is where stickiness lives, and OpenCode is making it easier to build that stickiness on their platform.

### Who Needs to Know

| Person | Why | Priority |
|--------|-----|----------|
| **Mike Taylor** | Leads tech vertical, teaches Claude Code. Clients will ask about OpenCode directly. Needs the adoption number, AGENTS.md vs CLAUDE.md comparison, and enterprise positioning. | **High — this week** |
| **Nityesh** | Builds agent infrastructure. The guided setup pattern is replicable as a skill for client onboarding. Training materials need updating. | **High — this week** |
| **Natalia** | Owns sales. "6.5M developers using a competitor" will come up in discovery calls. Needs ready framing: Claude Code = enterprise-grade (persistent memory, security, compliance), OpenCode = hobbyist/OSS choice. | **Medium — next client prep** |

### Concrete Actions

1. **Build a guided CLAUDE.md setup skill** — reads repo, infers context, generates starter CLAUDE.md with Knowledge Architecture + Decision Journal blocks. Nityesh can build this; becomes both internal tool and client deliverable.
2. **Add "Claude Code vs. OpenCode" comparison module** to Mike's developer bootcamp. Frame honestly: OpenCode wins on initial friction and cost; Claude Code wins on persistent memory, enterprise security, AutoDream, and skills ecosystem.
3. **Prepare a one-page competitive brief** for discovery calls with key talking points.
4. **Consider offering "CLAUDE.md configuration" as an explicit deliverable line item** — "The real deliverable shifts from 'we trained your team' to 'we configured your AI systems and the configuration keeps learning after we leave.'" This is the strategic moat.
5. **Monitor for enterprise OpenCode adoption signals** — if hedge funds or media companies mention OpenCode in discovery calls, that changes urgency.
