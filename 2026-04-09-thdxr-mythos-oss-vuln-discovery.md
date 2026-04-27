# OSS Models vs Mythos on Vulnerability Discovery

**Author:** dax (@thdxr)
**URL:** https://x.com/thdxr/status/2042079271108132937
**Date:** 2026-04-09

## Tweet text

There's an article floating around claiming OSS models could find the same vulns as Mythos.

It's a bit confusing though — in this test they pointed it towards the problematic code and even very tiny models could find the problem. But that's a bit different than discovering the problem in the first place, so this isn't to say Mythos isn't something special.

It's further complicated by how cheap these models are because you could blindly run this against every file for cheap? But that's further complicated because if it says every file has a vuln and 99% of them are wrong it's useless.

But also I'm pretty sure Mythos had expert security researchers narrowing down where to look. But maybe it wasn't that narrow.

Anyway this stuff is really complicated.

Context: Analysis of the FreeBSD NFS remote code execution vulnerability (CVE-2026-4747) — Anthropic's Mythos "crown jewel." They isolated the vulnerable `svc_rpc_gss_validate` function, provided architectural context, and asked 8 models to assess it. Even tiny models could flag the issue when pointed at the right code.

## Why it's relevant

Nuanced take on AI-assisted vulnerability discovery. The key distinction: **pointing a model at known problematic code ≠ autonomous discovery.** The scaffolding around the model (what to look at, what context to provide) matters enormously. This is the same pattern we see in consulting — the AI isn't magic, it's the workflow around it that creates value.
