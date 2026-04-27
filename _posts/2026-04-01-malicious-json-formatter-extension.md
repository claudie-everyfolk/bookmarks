---
date: 2026-04-01
title: "Malicious JSON Formatter Extension Injecting Tracking"
layout: post
author: "Wes Bos (@wesbos)"
url_source: "https://x.com/wesbos/status/2039355472830939319"
snippet: "HEADS UP. Popular JSON formatter extension has started injecting geolocation tracking and donation UI into websites. Reddit thread seems to think they are also swapping tracking IDs for affiliates (a-la honey). Uninstall and switch to another one."
relevance: "Security alert — supply chain attack via browser extension. A popular developer tool (JSON formatter) was compromised to inject tracking, geolocation, and affiliate ID swapping. This is the same pattern as the Honey extension scandal. Relevant to: - Every Consulting's client training: When teaching teams to use AI tools and browser extensions, we need to emphasize supply chain risk. Extensions have broad permissions and can be silently updated to include..."
---
# Malicious JSON Formatter Extension Injecting Tracking

**Author:** Wes Bos (@wesbos)
**URL:** https://x.com/wesbos/status/2039355472830939319
**Date:** 2026-04-01

## Tweet

> HEADS UP. Popular JSON formatter extension has started injecting geolocation tracking and donation UI into websites. Reddit thread seems to think they are also swapping tracking IDs for affiliates (a-la honey). Uninstall and switch to another one.

## Why it's relevant

**Security alert — supply chain attack via browser extension.** A popular developer tool (JSON formatter) was compromised to inject tracking, geolocation, and affiliate ID swapping. This is the same pattern as the Honey extension scandal. Relevant to:

- **Every Consulting's client training:** When teaching teams to use AI tools and browser extensions, we need to emphasize supply chain risk. Extensions have broad permissions and can be silently updated to include malicious code.
- **Our own security posture:** We should audit what extensions are installed on team machines.
- **Broader pattern:** Developer tools are high-value targets because devs have elevated access. JSON formatters, API clients, code formatters — all potential vectors.

Wes Bos built a replacement: [JSON Alexander](https://github.com/wesbos/JSON-Alexander)
