# Claude Code fileSuggestion Setting for Large Codebases

**Author:** Anthropic / Claude Code team
**Date:** 2026-04-09
**URL:** https://code.claude.com/docs/en/settings#file-suggestion-settings

## Tweet Text

> So we introduced a new fileSuggestion setting in Claude Code, so customers with large codebases could plug in their custom code index (using SourceGraph, an in-house index, etc.).

> quick guide to improve and make faster your Claude Code file suggestion — before all you have to install ripgrep, jq, fzf. Add this to your ~/.claude/settings.json: `"fileSuggestion": { "type": "command", "command": "~/.claude/file-suggestion.sh" }`

## Why This Is Relevant

Practical Claude Code feature for scaling to enterprise codebases. Relevant for Mike's developer training sessions — clients with large repos will benefit from custom file suggestion configs. Also relevant to our own setup if Claudie ever needs to work across larger project directories.

**Relevant to:** Mike (developer training), Nityesh (Claudie config optimization)
