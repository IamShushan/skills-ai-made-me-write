---
name: agentize-it
description: Translate a clear human objective into effective instructions for a specific AI agent, coding agent, model, or AI-enabled tool. Use when the user wants a paste-ready prompt, agent instructions, staged workflow, or task specification adapted to the target tool's current capabilities. Verify official documentation when syntax, tools, limits, workflows, or best practices may have changed. Do not use as a substitute for clarifying an undefined underlying task.
---

# Agentize It

Design for the destination agent, not for an abstract idea of a "good prompt."

## Translate the task

1. Identify the outcome, target agent or tool, available context, constraints, and success conditions.
2. Verify the target's current capabilities in official documentation when freshness matters. Prefer primary sources and distinguish documented behavior from inference.
3. Choose the lightest effective instruction form: one prompt, staged prompts, durable agent instructions, a workflow, or another format the target supports.
4. Include only context the target needs. State constraints and forbidden actions when they prevent realistic failure modes.
5. Add acceptance criteria and expected outputs when they make completion verifiable.
6. Deliver paste-ready instructions with minimal setup. Put any user-supplied placeholders where they are easy to find.

Do not inflate the prompt to make it look sophisticated. If the destination agent can discover a fact or infer a routine detail reliably, avoid restating it.

## Keep the boundary clear

Answer: **How should I tell this AI agent or tool to do what I want?**

Assume the underlying task is sufficiently defined. Use `read-my-mind` to clarify it or `make-it-real` to define the project before translating it for an agent.

## Examples

> "turn this into a codex task. it can edit files but must not touch migrations or commit"

Check current Codex behavior if needed, then produce scoped instructions with constraints and acceptance criteria.

> "I need Claude to compare these contracts, but I don't know if this should be one prompt or steps."

Choose the format based on the target's current capabilities and the review's verification needs, not on prompt length.
