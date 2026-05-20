# The .gitignore That Saves Your Career — .claude/ leak risk

**Author:** darkzodchi (@zodchiii)
**URL:** https://x.com/zodchiii/status/2050505359584788850
**Date:** 2026-05-01

## Tweet

> Anthropic leaked 512,000 lines of their own source code because someone forgot to add one line to an ignore file. If it happens to them, it's happening to you. Within hours the code was mirrored on GitHub and got 50,000 stars in two hours, likely the fastest-growing repository in GitHub history.
>
> The .claude/ directory is the newest threat. Claude Code stores your settings.json there, and if you've pre-approved bash commands with API tokens in them, those tokens are now sitting in a file that gets packaged into npm, PyPI, and RubyGems by default.
>
> Lakera security researchers confirmed this in April 2026: build tools for Python, Ruby, and JavaScript all package files from your project directory. If .claude/ isn't in your ignore file, your approved shell commands with embedded secrets ship to the public registry.

Tier 1 (immediate $$ loss): `.env*`, `.claude/settings.json`, `*.pem`, `credentials.json`, `.npmrc`, `.pypirc`
Tier 2 (account takeover): `.aws/credentials`, `.ssh/id_rsa`, `.docker/config.json`, `.kube/config`, `.terraform/terraform.tfstate`
Tier 3 (info leak): `.vscode/settings.json`, `.idea/`

## Why this is relevant

The headline leak claim (Anthropic, 50K stars in 2hrs) needs verification — likely sensational. But the underlying advice is correct and matches a real, recurring failure mode the team should care about:

- **Every client repo Claudie touches** likely has `.claude/settings.json` with pre-approved bash patterns. If clients later publish those repos to npm/PyPI without a proper `.gitignore`, embedded tokens leak.
- This is a **client-training talking point** — adding `.claude/`, `.aider*`, `.cursor/` to `.gitignore` should be in any "AI hygiene" handout.
- For Every Consulting's training decks (Mike/Brooker), this is a 1-slide insert: "the new files your `.gitignore` doesn't cover."

## Actions

- [ ] Verify the Anthropic leak claim independently before citing in client materials (no fabricated claims rule)
- [ ] Add `.claude/` to the default `.gitignore` recommendation in any onboarding skill we hand to clients
- [ ] Consider whether Claudie's own repos under `~/Projects/` have `.claude/` ignored
