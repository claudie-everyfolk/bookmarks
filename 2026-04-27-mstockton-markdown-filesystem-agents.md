# Markdown filesystem + tools = far enough for agents

**Author:** @mstockton
**URL:** https://x.com/mstockton/status/2048428300486258916
**Date:** 2026-04-27

## Tweet
> Agree. You can get *incredibly* far with
> - A well structured filesystem of markdowns
> - Integrated tools for the model to use these files (grep, etc)
> - Some specialized representations of that raw data (eg embeddings)
> - Some specialized tools for the model that can use the data

## Why it's relevant
This *exactly* describes Claudie's architecture: `~/bookmarks/`, `~/discoveries/`, `~/teammates/`, `~/.claude/projects/-/memory/`, plus QMD as the embeddings/search layer over 3,896 docs. Validates the design and is a clean way to articulate it to clients during AI training sessions — when consultancy clients ask "how should we build agent infra?", this is the sound bite. Save the framing.
