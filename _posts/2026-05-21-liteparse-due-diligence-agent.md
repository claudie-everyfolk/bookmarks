---
date: 2026-05-21
title: "LlamaIndex ships a free, open-source financial due-diligence agent (LiteParse)"
layout: post
author: "Jerry Liu (@jerryjliu0)"
url_source: "https://x.com/jerryjliu0/status/2057162684328505835"
snippet: "We built an AI agent for due diligence, with exact audit trails back to the source page, that you can use as a template without paying a single dime for PDF parsing. The secret sauce is LiteParse — our free, open-source, model-free document parser."
relevance: "Every's finance vertical is one of its biggest. The exact pain — parsing financial PDFs with auditable, source-linked citations — appears verbatim in SummitTX, TowerBrook, and Engineers Gate discovery calls. A ready-made demo and reference architecture for Brooker's finance clients."
---

# LlamaIndex ships a free, open-source financial due-diligence agent (LiteParse)

**Author:** Jerry Liu (@jerryjliu0), CEO of LlamaIndex
**Date:** 2026-05-21
**URL:** https://x.com/jerryjliu0/status/2057162684328505835

## Tweet

> We built an AI agent for due diligence, with exact audit trails back to the source page, that you can use as a template without paying a single dime for PDF parsing.
>
> The secret sauce is LiteParse — our free, open-source, model-free document parser. It can extract text from financial documents with complex layouts and tables, and return citations that describe exact bounding boxes in the source text.
>
> For a free, open-source parser, it is extremely powerful and is a key ingredient in agentic workflows!

Blog: https://llamaindex.ai/blog/building-a-financial-due-diligence-agent-with-liteparse

## Why it's relevant

Every Consulting's finance vertical is one of its biggest, and the exact pain point this solves — parsing financial PDFs with auditable, source-linked citations — appears verbatim in multiple client discovery calls. Free and model-free is a strong cost story for small funds.

## Relevance report

**Finance clients (confirmed).** Every runs an active Non-Tech/Finance vertical led by Brooker Belcourt. Named finance clients in the logs:
- **SummitTX Capital** — hedge fund (event-driven index-trading strategy). Discovery 2026-01-05.
- **TowerBrook Capital Partners** — private equity firm. Discovery + 4-session training; ~22/27 sessions delivered by 3/31/2026.
- **Engineers Gate (EGLP)** — quant hedge fund; 9 sessions delivered March 2026; in active pipeline outreach.

**Due-diligence / document-parsing pain in transcripts (direct quotes).**
- *SummitTX discovery* has a dedicated **"PDF Parsing Needs"** section: *"Translate index methodology and rules into code... Extract required fields and criteria from methodology documents."* The PM: *"put in a PDF and it tells us here's the fields that you need... the PDF parsing would be helpful."*
- *TowerBrook discovery*: associates run a full **"Investment diligence process"** — *"Memo and model creation, Investment diligence process, Transaction execution to close."* Biggest opportunity flagged: quarterly fund reporting. Notably: *"Has not explored file uploads or data extraction."*
- *TowerBrook training*: "Investment Process Documentation" — building a prompt library for **"Due diligence workflows."**

**Brooker is the natural owner.** His profile: "Non-Tech/Finance Vertical Lead... AI for analysis, practical workflows for non-engineers." Background: former hedge fund analyst, Goldman Sachs, Citadel, Perplexity finance vertical lead.

**Prior PDF discussion.** Nityesh proposed a local PDF-to-Markdown engine using Gemma; internal `nano-pdf` tooling exists — but nothing with bounding-box citations / audit trails. That is the gap LiteParse fills.

**Concrete actions:**
1. **Send to Brooker** as a training asset for the "Claude Code for Finance" course — a ready-made, model-free demo for SummitTX / TowerBrook / Engineers Gate.
2. **Reference architecture for a TowerBrook deliverable** — quarterly fund reporting and diligence memos are the textbook use case; auditable citations matter for PE memos.
3. **Custom tool for SummitTX** — they explicitly asked for "put in a PDF → get the fields." LiteParse + the agent template is a near-exact answer.
4. Best framed as **upsell / renewal hooks** — SummitTX has only a discovery call on record; TowerBrook's core engagement ended 3/31/2026.
