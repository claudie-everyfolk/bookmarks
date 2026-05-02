---
date: 2026-05-02
title: "The .gitignore That Saves Your Career — .claude/ leak risk"
layout: post
author: "darkzodchi (@zodchiii)"
url_source: "https://x.com/zodchiii/status/2050505359584788850"
snippet: "The .claude/ directory is the newest threat. Claude Code stores your settings.json there, and if you've pre-approved bash commands with API tokens in them, those tokens are now sitting in a file that gets packaged into npm, PyPI, and RubyGems by default."
relevance: "Every client repo Claudie touches likely has .claude/settings.json with pre-approved bash patterns. If clients publish those repos to npm/PyPI without proper .gitignore, embedded tokens leak. One-slide insert for AI hygiene training. Verify the headline Anthropic-leak claim before citing in client materials."
---

# The .gitignore That Saves Your Career — .claude/ leak risk

**Author:** darkzodchi (@zodchiii)
**URL:** https://x.com/zodchiii/status/2050505359584788850
**Date:** 2026-05-01

## Tweet

> Anthropic leaked 512,000 lines of their own source code because someone forgot to add one line to an ignore file. If it happens to them, it's happening to you.
>
> The .claude/ directory is the newest threat. Claude Code stores your settings.json there, and if you've pre-approved bash commands with API tokens in them, those tokens are now sitting in a file that gets packaged into npm, PyPI, and RubyGems by default.
>
> Lakera security researchers confirmed this in April 2026: build tools for Python, Ruby, and JavaScript all package files from your project directory.

Tier 1 (immediate $$ loss): `.env*`, `.claude/settings.json`, `*.pem`, `credentials.json`, `.npmrc`, `.pypirc`
Tier 2 (account takeover): `.aws/credentials`, `.ssh/id_rsa`, `.docker/config.json`, `.kube/config`, `.terraform/terraform.tfstate`
Tier 3 (info leak): `.vscode/settings.json`, `.idea/`

## Why this is relevant

The headline leak claim needs verification before citing in client materials. But the underlying advice is correct and matches a real, recurring failure mode the team should care about.

- Every client repo Claudie touches likely has `.claude/settings.json` with pre-approved bash patterns
- This is a client-training talking point — adding `.claude/`, `.aider*`, `.cursor/` to `.gitignore` belongs in any AI-hygiene handout
- For Mike/Brooker training decks, this is a 1-slide insert: "the new files your `.gitignore` doesn't cover"
