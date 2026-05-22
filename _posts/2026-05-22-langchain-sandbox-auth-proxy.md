---
date: 2026-05-22
title: "LangChain's Sandbox Auth Proxy: Controlling the Agent–World Boundary"
layout: post
author: "LangChain (@LangChain)"
url_source: "https://x.com/LangChain/status/2057508777759236401"
snippet: "Introducing the sandbox Auth Proxy: a way to control the boundary between agent-generated behavior and the rest of the world. It brings enterprise-style controls — endpoint protection, browser filtering, network controls — to agent sandboxes."
relevance: "Agent security infrastructure squarely in Every's territory. As clients move from chat to autonomous agents, 'what can the agent reach, and how do we govern it' becomes the hard question. The agent-era version of corporate network controls — a useful reference for governance conversations."
---

# LangChain's Sandbox Auth Proxy: Controlling the Agent–World Boundary

**Author:** LangChain (@LangChain) / Harrison Chase (@hwchase17)
**Tweet:** https://x.com/LangChain/status/2057508777759236401
**Date:** 2026-05-21

> Introducing the sandbox Auth Proxy: A way to control the boundary between agent-generated behavior and the rest of the world.
>
> [Harrison Chase:] If you've ever worked at a large enterprise, you have probably seen the standard corporate laptop setup. There's endpoint protection, browser filtering, device management, network controls... [Auth Proxy brings that boundary control to agent sandboxes.]

## Why it's relevant

Agent security infrastructure, not a vulnerability — but squarely in Every's territory. As clients move from "AI in a chat box" to autonomous agents that take real actions, "what can the agent actually reach, and how do we govern it" becomes the hard question. The Auth Proxy is the agent-era version of corporate network controls: a governed boundary between agent-generated behavior and external systems. Relevant to Mike (tech vertical — agent deployment), Brooker (governance conversations with finance clients), and Nityesh (Claudie's own permission model — launchd jobs run with `--permission-mode dontAsk` precisely to bound what agents can do without approval). Useful reference when a client asks "how do we let agents act without losing control."
