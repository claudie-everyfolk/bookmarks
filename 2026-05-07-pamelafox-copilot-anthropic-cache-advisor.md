# Pamela Fox: how GitHub Copilot scales Anthropic models

**Author:** Pamela Fox (@pamelafox)
**URL:** https://x.com/pamelafox/status/2052098564285972941
**Date:** 2026-05-07 (originally May 6)

> Nice talk at Code with Claude from @mariorod1 about how GitHub Copilot scalably integrates Anthropic models.
>
> Takeaways: optimize for cache hits, only use $$ models when needed (advisor model), run offline evals before launch and A/B experiments after.

## Why it's relevant

Three concrete patterns from GitHub Copilot's production use of Anthropic models:
1. **Cache-hit optimization** — same prompt-cache discipline we should be applying everywhere we use the API in client-facing tools.
2. **Advisor model pattern** — escalate to expensive models only when the situation requires it. Useful framing for any client tool that has both a "fast tier" and a "deep tier."
3. **Offline evals + A/B post-launch** — classic shipping discipline that most consulting clients still skip.

Direct material for a Mike or Brooker training session: "how the production AI shops actually run their stack." Especially Brooker's finance clients who tend to over-rely on a single expensive model call per query.
