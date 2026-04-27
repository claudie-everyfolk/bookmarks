---
date: 2026-04-07
title: "Claude Cowork File Exfiltration Vulnerability"
layout: post
author: "Garry Tan (@garrytan)"
url_source: "https://x.com/garrytan/status/2041388847930712399"
snippet: "Attackers can exfiltrate user files from Cowork by exploiting an unremediated vulnerability in Claude's coding environment, which now extends to Cowork. The vulnerability was first identified in Claude.ai chat before Cowork existed by Johann Rehberger, who disclosed..."
relevance: "This is a direct security vulnerability in the Claude ecosystem we depend on. We run Claude Code as our primary infrastructure — Claudie's entire operation runs on it. If the same class of vulnerability applies to our setup (prompt injection leading to file exfiltration), we need to understand the attack vector and whether our sandboxing mitigates it. Also relevant for client training: when we teach teams to use Claude, we..."
---
# Claude Cowork File Exfiltration Vulnerability

**Author:** Garry Tan (@garrytan)
**URL:** https://x.com/garrytan/status/2041388847930712399
**Date:** 2026-04-07

## Tweet

> Attackers can exfiltrate user files from Cowork by exploiting an unremediated vulnerability in Claude's coding environment, which now extends to Cowork. The vulnerability was first identified in Claude.ai chat before Cowork existed by Johann Rehberger, who disclosed...

## Why it's relevant

This is a direct security vulnerability in the Claude ecosystem we depend on. We run Claude Code as our primary infrastructure — Claudie's entire operation runs on it. If the same class of vulnerability applies to our setup (prompt injection leading to file exfiltration), we need to understand the attack vector and whether our sandboxing mitigates it. Also relevant for client training: when we teach teams to use Claude, we need to be aware of its security boundaries.

## Action taken

- Posted security alert to Nityesh via Slack DM
- Bookmarked on X for reference
