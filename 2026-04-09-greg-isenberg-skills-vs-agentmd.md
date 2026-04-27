# Greg Isenberg: Skills Are the Actual Unlock, Not agent.md

**Author:** Greg Isenberg (@gregisenberg)
**URL:** https://x.com/gregisenberg/status/2042010418454184325
**Date:** 2026-04-09

## Tweet text (key points)

1. **agent.md files are mostly unnecessary.** Every single line in an agent.md file gets added to every conversation — ~7000 tokens burning on every run. Save agent.md for proprietary information the model genuinely cannot know on its own.

2. **Skills are the actual unlock.** A skill.md file loads into context only the name and description (~50 tokens). Full instructions only appear when the agent recognizes it needs that skill. Instead of 7000 tokens per run, you have 50, and the agent stays sharp.

3. **How to build a skill the right way:** Run the workflow by hand with the agent first. Walk it through every single step. Tell it what to check, what good looks like, what bad looks like. Correct it in real time. Once you have a full successful run, tell the agent to review everything and write the skill itself.

4. **Recursively building skills** is how you go from frustrated to reliable. When the skill breaks, ask the agent exactly why it failed. Fix it together. Update the skill file so that failure mode never happens again.

5. **Sub agents are something you earn, not something you set up on day one.** Start with one agent, build one workflow, turn it into one skill. Once that works, add another.

6. **Your workflow is the thing the model cannot get anywhere else.** What it does not have is your specific process, your taste, your way of doing things. That is what skills capture. Downloading someone else's skill means downloading their context onto your setup — it will not work.

References @rasmic (Ras Mic, The Professor) as demonstrating this approach.

## Why it's relevant

This is basically a public validation of how Claudie was built. Nityesh and Natalia's 200+ hour investment in understanding the Claude Code harness follows this exact pattern — iterative skill building, earned complexity, workflow-specific context. The "your workflow is what the model can't get elsewhere" line is our consulting thesis in one sentence.

Also relevant for client training: this framework is exactly what we should teach clients. Not "here's how to use Claude" but "here's how to build skills that encode YOUR specific process."
