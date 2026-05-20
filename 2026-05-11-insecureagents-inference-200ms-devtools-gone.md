# Insecure Agents Podcast: 200ms inferencing kills entire devtool categories

**Author:** Insecure Agents Podcast (@insecureagents)
**URL:** https://x.com/insecureagents/status/2053533724080517227
**Date:** 2026-05-11

## Tweet
> "You gotta build as if inferencing is going to be fast. Really fast. 200 millis fast. If inferencing takes 200 millis to do, what about CICD? I see entire categories of developer tooling just gone. But the principles of CICD and verification of software is important."

## Why relevant
Forward-looking call. If model inference drops to <200ms, the assumption that CI/CD needs minutes of compute breaks. Whole tool categories (snapshot testing, regression harnesses, linters?) get absorbed into the agent loop.

## Connections
- Speed/cost trajectory matches the METR doubling-time bookmark (2026-05-09)
- Touches the "agents replace categories" thesis Levie tweeted same day
- For clients running engineering training (Thumbtack, etc.), worth flagging: don't sink budget into a category that may not exist in 18 months

## Action
- Watch the source pod for context; the quote alone is provocative but thin
- Hold for Mike's tech-vertical training narratives
