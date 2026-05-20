# Pamela Fox's open-source presentation-skills

**Author:** Pamela Fox (@pamelafox)
**URL:** https://x.com/pamelafox/status/2049619027031674893
**Repo:** https://github.com/pamelafox/presentation-skills
**Date saved:** 2026-04-30

## Tweet
> I've added more presentation-skills:
> - pdf-to-markdown
> - review-presentation
> - capture-video-frames
> - convert-slides-to-images
> - extract-slide-text
> - extract-transcript
> - fetch-slides
> - outline-slides
> - generate-writeup
> - youtube-live-chat

## Why it's relevant — STRONG MATCH for our slide-deck-creation plugin
We already have a slide-deck-creation plugin (`generate-blueprint`, `add-visual-direction`, `prepare-image-assets`, `review-slides`, `design-slides`, `master`, `article-to-deck`). Pamela's set has direct overlap and gaps we're missing:
- **review-presentation** — independent QC layer; could improve our existing review-slides skill
- **convert-slides-to-images** + **extract-slide-text** — useful for ingesting client-provided decks during discovery
- **fetch-slides** — automate pulling decks from Drive
- **outline-slides** — likely simpler/faster than our blueprint flow for quick turnarounds
- **extract-transcript** — pairs with Granola transcripts → deck pipeline

## Action
Worth a 30-min review by Nityesh. Specifically: compare review-presentation to our review-slides loop (which has been catching missing-text bugs per recent feedback). If Pamela's prompts are tighter, adopt them.
