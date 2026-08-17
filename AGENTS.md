# Repository guidance

This is a small public collection of portable Agent Skills. Keep it useful, inspectable, and natural.

## Skill boundaries

Preserve these distinct jobs:

```text
read-my-mind      → clarify the thought
make-it-real      → turn the idea into execution
cut-the-bullshit  → challenge the decision or reasoning
agentize-it       → translate intent for an AI agent/tool
am-i-genius       → research how novel the idea really is
```

Keep each skill narrow enough to activate predictably. Avoid overlap and never broaden a skill silently. If its job changes, make that decision explicit.

## Skill authoring

- Follow the current [Agent Skills specification](https://agentskills.io/specification). Verify current official guidance for affected agent tools when discovery, installation, or compatibility may have changed.
- Treat the frontmatter description as discovery metadata: front-load the use case, name concrete triggers, and state meaningful boundaries.
- Use progressive disclosure. Keep the core `SKILL.md` concise; add focused material under `references/` only when a task-specific branch justifies it.
- Add scripts, assets, product-specific metadata, or dependencies only when they solve a current need.
- Prefer primary sources when external behavior, tool capabilities, or syntax may have changed.
- Preserve full-depth work and distilled outputs: choose the approach best suited to the task, do all necessary research and verification, and return only what helps the user understand, decide, act, or verify.
- Use a few realistic examples to clarify activation and boundaries, not to decorate the skill.

## Repository changes

- Prefer small, intentional changes over broad cleanup passes.
- Preserve the concise, practical, slightly self-aware tone. Write for technically capable readers without marketing language.
- Consider whether every public file and sentence helps someone use, understand, or maintain the repository.
- Keep the repository free of private notes, prompt transcripts, scratch reasoning, credentials, machine details, personal information, and generated junk.
- Avoid infrastructure that the repository does not currently need.
- Review `git status` and the final diff. Do not modify unrelated work, and do not commit or push unless explicitly asked.
