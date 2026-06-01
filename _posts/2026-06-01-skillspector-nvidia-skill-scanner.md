---
date: 2026-06-01
title: "SkillSpector — NVIDIA's pre-install security scanner for AI agent skills"
layout: post
author: "Bilgin Ibryam (@bibryam)"
url_source: "https://x.com/bibryam/status/2060940955084054634"
snippet: "SkillSpector - a new security scanner for skills by NVIDIA. Scan AI agent skills before installing them. 64 security checks across 16 categories. Fast static analysis + optional LLM semantic evaluation. Prompt injection detection. Credential theft detection."
relevance: "The defensive tool for the SKILL.md supply-chain attack we bookmarked two days ago. Directly applicable to Claudie's 100+ skills from 4 marketplaces (3 auto-updating) and to a client agent-governance offering. Caveat: static+LLM scanning still misses the 87% the attack paper flagged — provenance beats inspection."
---


**Author:** Bilgin Ibryam (@bibryam) — reposted, ~252K views
**Tweet:** https://x.com/bibryam/status/2060940955084054634
**Date:** 2026-05-31

## Tweet

> SkillSpector - a new security scanner for skills by NVIDIA
> • Scan AI agent skills before installing them
> • 64 security checks across 16 categories
> • Fast static analysis +
> • Optional LLM semantic evaluation
> • Prompt injection detection
> • Credential theft detection

## Why it's relevant

The defensive tool for the exact attack we bookmarked two days earlier (SKILL.md semantic supply-chain attack, Saha et al.). It scans agent skills *before* install for prompt injection and credential theft — directly applicable to Claudie's own 100+ skills loaded from four marketplaces (three with autoUpdate on), and to a client agent-governance offering. Caveat: the attack paper showed LLM-eval scanning is the move it anticipated and is not a silver bullet — provenance/allowlisting still beats inspection.

## Sub-agent relevance report

**What it is:** NVIDIA's pre-install security scanner for AI agent skills. 64 checks / 16 categories, fast static analysis + *optional LLM semantic evaluation*, with explicit prompt-injection and credential-theft detection.

### Why this lands hard for us
This is the *defensive tool* for the exact attack we bookmarked two days earlier. Claudie's own architecture is the threat model: 100+ SKILL.md skills loaded from **four marketplaces** (`~/.claude/plugins/known_marketplaces.json`), three of which run `autoUpdate: true` — `anthropics/skills`, `EveryInc/every-consulting`, and **`nityeshaga/claude-home-base`, a single-maintainer personal repo**. The governance hook meant to gate this, `~/.claude/plugins/blocklist.json`, still holds only two test entries. A scanner that vets skills *before* install maps directly onto a live, un-closed gap.

### Who it's relevant to
- **Nityesh** (owns Claudie's skill governance) — primary. His `claudie-security-briefing.md` Vector 1 ("Supply Chain") covers only **code dependencies** (npm/pip/cargo), with no coverage of the SKILL.md *metadata* layer. SkillSpector is a candidate control for that named gap.
- **Mike Taylor** (Tech Vertical Lead) — client-facing buyer for a "vet your skills" training module and the credibility demo.
- **Brooker** (Non-Tech/Finance Lead) — the governance angle: who's allowed to install agent tools, and what scans them first.
- **Natalia** — decides whether agent-governance becomes a productized offering.

### What it connects to
1. `bookmarks/2026-05-29-skillmd-semantic-supply-chain-attack.md` (Saha et al., arXiv 2605.11418) — the attack paper. Its report already recommended "activate the empty blocklist.json" and "pre-load review on SKILL.md changes." SkillSpector is a concrete tool for both.
2. **Signal Digest #57** (ClawHub — 824 malicious skills) — explicitly predicted "startups building 'Snyk for agent skills.'" SkillSpector is that prediction arriving, from NVIDIA.
3. **Signal Digest #100** (the Saha entry) — predicted "skill firewalls / pre-load review tooling."
4. Nityesh's security briefing — the gap-bearer this could partially fill.
5. The already-floated **"agent governance assessment" offering**.

### The critical caveat: does the LLM eval close the 87% gap?
**Probably not fully.** The Saha paper showed static scanners flag poisoned skills as clean 87% of the time — and pre-emptively argued that "scan SKILL.md with an LLM" also loses, because metadata can be written to beat the LLM judge. SkillSpector's *optional LLM semantic evaluation* is exactly that anticipated move. It raises the bar on prompt-injection and credential-theft payloads (real value against code-bearing skills), but content inspection alone does not defeat the *selection-bias* vector (77.6%) where two functionally-identical skills differ only in framing. **Provenance and allowlisting beat inspection.** SkillSpector is a useful layer, not a silver bullet — frame it that way to clients.

### Concrete actions
**Internal (Nityesh):**
- Run SkillSpector against all four marketplaces and Claudie's installed skills as a one-time audit — start with the highest-risk source, `claude-home-base` (single maintainer, autoUpdate on).
- Pair it with the structural fix the scanner can't provide: disable `autoUpdate` on `claude-home-base` (or fold its skills into `every-consulting`), and populate the real `blocklist.json` (currently test-only).
- Consider a pre-install SkillSpector gate as a hook, so auto-updates can't land unscanned.

**Client-facing (Mike/Brooker/Natalia):**
- Add SkillSpector to the agent-governance / skill-supply-chain training module as the "concrete tool you can run today" artifact — with the caveat above so we don't oversell static+LLM scanning.
- Sales line for finance clients (Bloomberg, hedge funds): "we scan our own agent's skills with NVIDIA's tooling *and* enforce provenance, because scanning alone misses 87%."
