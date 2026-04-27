---
date: 2026-04-11
title: "Claude Code Security Hardening — 3-Level Guide"
layout: post
author: "Axel Bitblaze (@Axel_bitblaze69)"
url_source: "https://x.com/Axel_bitblaze69/status/2042704945200402649"
snippet: "By default, Claude Code can read SSH keys, AWS credentials, every .env file, and push code wherever it wants. One bad repo with a hidden instruction and your data is gone."
relevance: "AI Security / Operations. This is a practical hardening guide for Claude Code. We run Claude Code with `--dangerously-skip-permissions` on some scheduled jobs, so understanding the attack surface matters. The Trail of Bits plugin and deny-list patterns are worth evaluating for our own setup — especially the `.env` and credential path blocking. Reference: https://github.com/trailofbits/claude-code-devcontainer"
---
# Claude Code Security Hardening — 3-Level Guide

**Author:** Axel Bitblaze (@Axel_bitblaze69)
**URL:** https://x.com/Axel_bitblaze69/status/2042704945200402649
**Date:** 2026-04-11

## Tweet

By default, Claude Code can read SSH keys, AWS credentials, every .env file, and push code wherever it wants. One bad repo with a hidden instruction and your data is gone.

Three levels to lock it down:

**Level 1 (15 min):** `/sandbox` + `settings.json` deny rules for `~/.ssh/**`, `~/.aws/**`, `.env*`, curl/wget/ssh + disable `enableAllProjectMcpServers` + `claude update`

**Level 2 (30 min):** Trail of Bits plugin — `claude plugin marketplace add trailofbits/skills` — adds security checklists, workflow hooks, forces plan-before-code and verify-before-ship.

**Level 3 (1 hour):** Full container isolation via devcontainers. Claude runs in a container with zero access to your actual machine.

## Why it matters

**AI Security / Operations.** This is a practical hardening guide for Claude Code. We run Claude Code with `--dangerously-skip-permissions` on some scheduled jobs, so understanding the attack surface matters. The Trail of Bits plugin and deny-list patterns are worth evaluating for our own setup — especially the `.env` and credential path blocking.

Reference: https://github.com/trailofbits/claude-code-devcontainer
