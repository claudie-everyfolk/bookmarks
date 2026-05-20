---
date: 2026-05-20
title: "Cowork's sandbox silently ignores managed settings and env vars"
layout: post
author: "Daniel San (@dani_avila7)"
url_source: "https://x.com/dani_avila7/status/2057106024776012231"
snippet: "Cowork is incredible for organizational deployment, but it has a major problem: its sandbox. It silently ignores your managed settings and environment variables. Cowork runs inside a Linux VM, your host settings.json is never mounted, managed settings resolve to a path that doesn't exist, env vars aren't forwarded."
relevance: "A concrete deployment gotcha for any Every client rolling out Cowork org-wide. Managed settings is how enterprise IT enforces permissions and policy — and Cowork's VM sandbox silently bypasses it. A governance hole worth flagging before recommending Cowork to a finance or enterprise client."
---

# Cowork's sandbox silently ignores managed settings and env vars

**Author:** Daniel San (@dani_avila7)
**URL:** https://x.com/dani_avila7/status/2057106024776012231
**Date:** 2026-05-20

> Cowork is incredible for organizational deployment, but it has a major problem: its sandbox.
>
> It silently ignores your managed settings, and environment variables. Cowork runs inside a Linux VM, your host settings.json is never mounted, managed settings resolve to a path that doesn't exist, env vars aren't forwarded.
>
> I've been digging for a workaround and there doesn't seem to be one... How are you all solving this?

## Why it's relevant

A concrete deployment gotcha for any Every client rolling out Cowork at the org level. "Managed settings" is exactly the mechanism an enterprise IT team would use to enforce permissions, allow/deny rules, and policy — and Cowork's VM sandbox silently bypasses it. That's a governance hole worth flagging before recommending Cowork to a finance or enterprise client. Pairs with Aakash Gupta's "start with Cowork" advice: Cowork is the right on-ramp for non-technical learners, but the team should know its sandbox does not honor host config when scoping a managed rollout. Worth tracking whether Anthropic ships a fix.
