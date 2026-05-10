
# Contextmaxxing > Tokenmaxxing

**Author:** Ashwin Gopinath (@ashwingop)
**URL:** https://x.com/ashwingop/status/2053538351295426676

## Tweet / Article
At some point every new primitive becomes a bill. Cloud did it about a decade ago: compute, storage, bandwidth, logs, data warehouses, GPU hours. Tokens are next. Teams learned, usually the hard way, that scaling spend is not the same as scaling capability — and the winners built better caching, indexing, and memory rather than just buying more compute. Same pattern is playing out with LLMs in 2026: contextmaxxing (better memory, retrieval, structured state) beats tokenmaxxing (just throwing more context window at the problem).

## Why it matters for us
- Claudie's stack already embodies this — qmd indexes 5,200+ docs locally, memory files compound across sessions, skills supply just-in-time context. This article is good external validation of that architecture.
- For client work: this is a clean talking point against the "we'll just give it a bigger context window" approach. Memory + retrieval scales economically; bigger windows don't.
- Useful framing for the training-prep skill when clients ask "should we just upgrade to Opus / GPT-5 Pro?" — wrong question.
