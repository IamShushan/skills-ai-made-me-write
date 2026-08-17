# skills-ai-made-me-write

**Serious AI agent skills for serious work. Also some stuff I made because AI kept annoying me.**

A personal collection of reusable [Agent Skills](https://agentskills.io/) I built for work I actually do: half-formed thoughts, repeated annoyances, ideas that need pressure-testing, and things I want to make real. They do the thinking and keep the result focused instead of handing back a thinking dump.

Skills trigger by intent, not by exact keywords. Use the distinction below to choose one directly or understand why an agent picked it.

| Skill | What it does / when to use it | Example |
| --- | --- | --- |
| [`read-my-mind`](skills/read-my-mind/SKILL.md) | Clarifies a messy or incomplete thought before planning. | `wait what if i make it local and it reads the xml but never changes anything and ai is just the interface` |
| [`make-it-real`](skills/make-it-real/SKILL.md) | Turns a clear idea into practical scope and immediate next steps. | `I want to run a tiny neighborhood repair night next month. How do I get it moving?` |
| [`cut-the-bullshit`](skills/cut-the-bullshit/SKILL.md) | Pressure-tests a decision and gives a clear recommendation. | `Our hosting costs are growing. Should we stay on Vercel or move to AWS? Check the current pricing and operational tradeoffs, then tell me whether the migration is actually worth it.` |
| [`agentize-it`](skills/agentize-it/SKILL.md) | Translates a clear goal into instructions for a specific AI agent or tool. | `Turn this into a Cursor task. It can edit the frontend but must not touch migrations or commit.` |
| [`am-i-genius`](skills/am-i-genius/SKILL.md) | Researches whether an idea already exists and how novel it really is. | `What if a calendar only showed commitments that cost real money? Did somebody already do this?` |

## Install

```bash
npx skills add IamShushan/skills-ai-made-me-write
```

The installer lets you choose which skills to add and handles the destination for supported agents. The skills follow the open [Agent Skills specification](https://agentskills.io/specification) and are intended for compatible tools such as Claude Code, Codex, Cursor, and GitHub Copilot. Exact support depends on each tool's implementation.

Each folder contains the canonical, portable `SKILL.md`. Read one to inspect the workflow, or copy the folder into a location supported by your tool. The shared working principles are in [`PRINCIPLES.md`](PRINCIPLES.md).
