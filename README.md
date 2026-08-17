# skills-ai-made-me-write

**Serious AI agent skills for serious work. Also some stuff I made because AI kept annoying me.**

A personal collection of reusable [Agent Skills](https://agentskills.io/) I built for work I actually do: half-formed thoughts, repeated annoyances, ideas that need pressure-testing, and things I want to make real. They do the thinking and keep the result focused instead of handing back a thinking dump.

| Skill | What it does | The question it answers |
| --- | --- | --- |
| [`read-my-mind`](skills/read-my-mind/SKILL.md) | Clarifies messy, incomplete, or shorthand thoughts. | What am I actually trying to say or accomplish? |
| [`make-it-real`](skills/make-it-real/SKILL.md) | Turns a clear idea into practical scope and action. | How do I make this real? |
| [`cut-the-bullshit`](skills/cut-the-bullshit/SKILL.md) | Challenges reasoning and makes a clear recommendation. | Does this make sense, and what should I actually do? |
| [`agentize-it`](skills/agentize-it/SKILL.md) | Translates intent into instructions for a specific AI agent or tool. | How should I tell this agent to do what I want? |
| [`am-i-genius`](skills/am-i-genius/SKILL.md) | Researches how novel an idea is compared with what already exists. | Did I come up with something new? |

## Install

```bash
npx skills add IamShushan/skills-ai-made-me-write
```

The installer lets you choose which skills to add and handles the destination for supported agents. The skills follow the open [Agent Skills specification](https://agentskills.io/specification) and are intended for compatible tools such as Claude Code, Codex, Cursor, and GitHub Copilot. Exact support depends on each tool's implementation.

Each folder contains the canonical, portable `SKILL.md`. Read one to inspect the workflow, or copy the folder into a location supported by your tool. The shared working principles are in [`PRINCIPLES.md`](PRINCIPLES.md).
