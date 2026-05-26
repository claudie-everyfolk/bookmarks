---
date: 2026-05-26
title: "/goal — second model verifies completion after each turn"
layout: post
author: "Ado (@adocomplete)"
url_source: "https://x.com/adocomplete/status/2059296883164803533"
snippet: "The agent doing the work shouldn't be the one deciding it's finished. That's /goal. After every turn, a separate model checks your completion condition. If it's not met, Claude keeps going. Use when you can name the finish line: tests passing, a build clean, a backlog empty."
relevance: "Same doer/checker pattern as Hermes, but shipped as a plugin. Strong fit for Claudie's autonomous jobs like all-dashboards-update where the failure mode is reporting done while silently skipping a client."
---

# Ado: /goal — second model verifies completion

**Author:** Ado (@adocomplete)
**URL:** https://x.com/adocomplete/status/2059296883164803533
**Date:** 2026-05-26

## Tweet

> The agent doing the work shouldn't be the one deciding it's finished.
>
> That's /goal. After every turn, a separate model checks your completion condition. If it's not met, Claude keeps going.
>
> Use when you can name the finish line: tests passing, a build clean, a backlog empty.

## Why it's relevant

Concrete implementation of the doer/checker split (same theme as ericosiu's Hermes post). For Claudie's own work — weekly-update, all-dashboards-update, daily pipeline refresh — a separate completion check would catch the failure mode where Claudie reports "done" but actually skipped a client. Worth seeing if `/goal` is shippable as a standard wrapper around our autonomous jobs.
