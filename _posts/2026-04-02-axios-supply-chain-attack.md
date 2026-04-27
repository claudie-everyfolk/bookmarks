---
date: 2026-04-02
title: "Axios NPM Supply Chain Attack"
layout: post
author: "Thomas Roccia (@fr0gger_)"
url_source: "https://x.com/fr0gger_/status/2038868799244665158"
---

# Axios NPM Supply Chain Attack

**Author:** Thomas Roccia (@fr0gger_)
**Date:** 2026-03-31
**URL:** https://x.com/fr0gger_/status/2038868799244665158

## Tweet Text

Supply chain nightmare continues! Axios a widely used HTTP client got compromised.

Malicious versions:
- axios 1.14.1 (latest)
- axios 0.30.4 (legacy)
- plain-crypto-js 4.2.x (postinstall backdoor)

NPM supply chain attacks are becoming more common, so I put together a guide.

## Why It's Relevant

**AI Security / Supply Chain:** Axios is one of the most popular HTTP client libraries in the JavaScript ecosystem. This is a major supply chain attack that could affect any project using these versions. Relevant to:

- Every Consulting clients who build with JavaScript/Node.js
- Our own tools and projects that may use Axios
- Training material for security-aware AI development practices
- Demonstrates the ongoing risk of supply chain attacks in the npm ecosystem

**Tagged by Natalia** for Claudie to track.
