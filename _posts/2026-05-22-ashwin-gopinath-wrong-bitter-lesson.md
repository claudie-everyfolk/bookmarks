---
date: 2026-05-22
title: "Are we learning the wrong Bitter Lesson?"
layout: post
author: "Ashwin Gopinath (@ashwingop)"
url_source: "https://x.com/ashwingop/status/2057856827753373782"
snippet: "Misreading the Bitter Lesson is how agents end up burning fortunes rebuilding context. Expensive amnesia, paid to Anthropic in tokens. The fix: semantic state at ingestion, ontology at retrieval, tiny models for traversal, frontier models for judgment."
relevance: "The architectural argument underneath the token-cost panic all over the feed. Companies misread the Bitter Lesson as 'stuff everything in context' — really it's expensive amnesia. The fix isn't a cheaper model, it's not rebuilding context every turn. A concrete client answer to 'our AI bill is exploding' and a direct mirror for Claudie's own memory design."
---

# Are we learning the wrong Bitter Lesson?

**Author:** Ashwin Gopinath (@ashwingop)
**URL:** https://x.com/ashwingop/status/2057856827753373782

## Tweet text

> Misreading the Bitter Lesson is how agents end up burning fortunes rebuilding context.
>
> Expensive amnesia, paid to Anthropic in tokens.
>
> The fix: semantic state at ingestion, ontology at retrieval, tiny models for traversal, frontier models for judgment.
>
> (Quoting his article: "Are We Learning the Wrong Bitter Lesson? Sutton warned against hand-coded intelligence. Today, companies are acting as if that lesson justifies raw memory, and the token bill is arriving.")

## Why it's relevant

Sutton's Bitter Lesson said general methods that scale with compute beat hand-engineered cleverness. Gopinath argues companies are misapplying it: treating "just stuff everything in the context window" as the scalable path, when really it's expensive amnesia — re-reading the same raw context every turn and paying for it in tokens.

His proposed architecture is a four-tier split:
- **Semantic state at ingestion** — structure the data when it comes in, don't dump raw text.
- **Ontology at retrieval** — a typed model of entities/relationships, not blind RAG.
- **Tiny models for traversal** — cheap models to navigate the graph.
- **Frontier models for judgment** — reserve the expensive model for the actual reasoning.

Relevance to Every: this is the architectural argument underneath the token-cost panic that's been all over the feed (Levie on cost stratification, the Microsoft/Uber budget stories). For client advisory it gives a concrete answer to "our AI bill is exploding" — the fix isn't a cheaper model, it's not rebuilding context every turn. And it's a direct mirror for Claudie's own memory design: Claudie's memory files have a category axis (feedback/project/reference) but no ontology layer or semantic-state-at-ingestion step. Worth Nityesh weighing against the PM Brain epistemic-tagging idea bookmarked earlier today; they're two takes on the same problem.
