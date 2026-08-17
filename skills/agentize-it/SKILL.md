---
name: agentize-it
description: Translate a clear human objective into effective instructions for a specific AI agent, coding agent, model, or AI-enabled tool. Use when the user wants a paste-ready prompt, agent instructions, staged workflow, or task specification adapted to the target tool's current capabilities. Verify official documentation when syntax, tools, limits, workflows, or best practices may have changed. Do not use as a substitute for clarifying an undefined underlying task.
---

# Agentize It

Design for the destination agent, not for an abstract idea of a "good prompt."

## Translate the task

1. Identify the outcome, target agent or tool, available context, constraints, and success conditions. Inspect supplied artifacts or working context when the instructions depend on them.
2. Verify the target's current capabilities in official documentation when freshness matters. Prefer primary sources and distinguish documented behavior from inference.
3. Choose the lightest effective instruction form: one prompt, staged prompts, durable agent instructions, a workflow, or another format the target supports.
4. Include only context the target needs. State constraints and forbidden actions when they prevent realistic failure modes.
5. Add acceptance criteria and expected outputs when they make completion verifiable.
6. Check that the instructions use supported capabilities, contain no conflicting constraints, and define outputs the destination agent can actually produce and verify.
7. Deliver the result in the format most useful to the destination.

Do not inflate the prompt to make it look sophisticated. If the destination agent can discover a fact or infer a routine detail reliably, avoid restating it.

## Deliver the result

- By default, provide one clean, paste-ready block with only the setup needed to use it.
- When the instructions are long, reusable, or naturally split across stages, create a clearly named Markdown or tool-native instruction file when the environment allows it.
- When creating a file, return its location and the exact next action.
- Keep commentary outside the instruction payload so the user does not need to clean it before use.

## Boundary

Answer: **How should I tell this AI agent or tool to do what I want?**

Translate a sufficiently defined task. Clarify only what is necessary to produce instructions the destination can execute reliably.

## Examples

> "turn this into a codex task. it can edit files but must not touch migrations or commit"

Check current Codex behavior if needed, then produce scoped instructions with constraints and acceptance criteria.

> "Turn this into instructions for an AI video editor: make a 30-second vertical teaser from these interview clips. Keep the speaker's meaning intact, avoid synthetic footage, add readable captions, and export it for Instagram Reels."

Check the target's current capabilities, resolve the parameters that materially affect the edit, and deliver the instructions in the format the tool can use most reliably.
