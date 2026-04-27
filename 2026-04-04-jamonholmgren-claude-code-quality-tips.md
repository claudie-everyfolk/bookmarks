# 8 Tips to Keep Claude From Writing Trash Code

**Author:** Jamon Holmgren (@jamonholmgren)
**URL:** https://x.com/jamonholmgren/status/ (Apr 4, 2026)
**Bookmarked:** 2026-04-04

## Tweet

"The things that have worked the best for me to keep Claude etc from writing complete trash code. (This assumes you're using the top models at medium to high reasoning, and paying $200+/mo for a good plan, not $20.)"

1. **Excellent test suite** — agent must run and fix tests. Include linting, type checking, compiling, static analysis, and even debugger access.
2. **Excellent docs** — hand-written covering systems, code style, testing strategies. Agent must keep docs up to date with every commit/PR.
3. **Opinionated, curated codebase** — well-named functions/classes/filenames, small files, flat folder structure, and an AGENTS.md that indexes everything. Don't let speed make this slip.
4. **Review agents** — use Codex to review Claude and vice versa. Add review checklists it must use before finishing.
5. **Well-written specifications** — hand-written, take your time.
6. **Review every line** — update docs, tests, or specs to prevent problems from recurring.
7. **Run agents at night** — forces you to improve everything upstream so you don't wake up to slop.
8. **Hand-write features sometimes** — stay in tune with the codebase.

## Why This Is Relevant

Extremely practical, battle-tested framework for getting quality output from agentic coding. Directly relevant to:
- **Mike's developer training curriculum** — these are the exact patterns he should be teaching in Claude Code / Cursor workshops
- **Claudie's own setup** — validates the approach of CLAUDE.md, test suites, and structured harness engineering
- **Client engagements** — practical checklist for any engineering team adopting AI coding assistants
- The "run agents at night" tip is particularly interesting — it forces investment in the harness layer (echoes Harrison Chase's framework)
