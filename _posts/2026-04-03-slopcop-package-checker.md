---
date: 2026-04-03
title: "slopcop — Package Legitimacy Checker for AI-Hallucinated Dependencies"
layout: post
author: "Larsen Cundric (@larsencc)"
url_source: "https://x.com/larsencc/status/2040165621628027354"
---

# slopcop — Package Legitimacy Checker for AI-Hallucinated Dependencies

**Author:** Larsen Cundric (@larsencc)
**URL:** https://x.com/larsencc/status/2040165621628027354
**Date:** 2026-04-03

## Tweet

> Built a tool for exactly this.
>
> "slopcop check <package>" tells you if a package is legit before you install it. Checks registry age, download count, postinstall scripts, and name similarity to popular packages.
>
> "slopcop scan" runs through your entire package.json or requirements.txt.
>
> If your AI hallucinated a package name and someone registered it with malware, slopcop catches it.
>
> Pro Tip: Setup a Claude Code hook to run this before every install.

## Why it's relevant

**AI Security** — This addresses a real supply chain attack vector: AI models hallucinate package names, attackers register those names with malicious code. slopcop can be set up as a Claude Code hook to automatically check packages before installation. Directly relevant to the team's security posture and could be recommended to consulting clients who use AI coding tools.

---

## Detailed Relevance Report

### 1. Who This Is Most Relevant To

**Nityesh (primary)** — Builds and maintains Claudie's infrastructure, manages all npm/pip dependencies. He would install slopcop, write the Claude Code hook, and enforce it. The Every Consulting plugin marketplace already has a hooks pattern in `experimental/hooks/hooks.json` — slopcop would slot right in.

**Mike Taylor (high)** — Teaches AI coding workflows to clients. This specific threat — AI-hallucinated package names registered as malware — is directly relevant to his training curriculum. A 5-minute live demo during sessions would be powerful.

**Natalia (moderate)** — Positioning value. Bloomberg, NYT, hedge funds — organizations where supply chain compromise is catastrophic. Articulating this risk and offering slopcop as security hygiene elevates the consulting offering.

### 2. Connection to Existing Practices

- Ring 0 already has a hard-never rule against prompt-injected scripts. slopcop operationalizes a related concern.
- X browsing pipeline already posts security vulnerabilities to Slack.
- Hooks infrastructure exists in the plugin marketplace. No existing package verification tooling was found — this is a gap.

### 3. Concrete Implementation Steps

1. **Install:** `npm install -g slopcop`
2. **Scan existing projects:** Run against `/Users/claudie/Projects/slack-bot/` and plugin marketplace dependencies
3. **Set up Claude Code hook:** Add a `PreToolUse` hook in settings.json that intercepts `npm install` / `pip install` commands, runs `slopcop check`, blocks suspicious packages
4. **Add to plugin marketplace:** Package as a reusable hook for distribution to clients and team members

### 4. Client Training Relevance

- AI supply chain attacks are a new threat class most developers don't know about
- Mike's tech training should include a live demo: Claude suggests a package → run slopcop → show flagged result
- Brooker's non-tech vertical benefits too — non-technical teams using ChatGPT to write scripts lack intuition to question package names
- Differentiates Every Consulting: "We don't just teach people to use AI — we teach them to use it safely"
