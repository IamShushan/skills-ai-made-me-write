---
name: am-i-genius
description: Research how original an idea is compared with products, companies, open source, papers, patents, APIs, extensions, communities, historical attempts, and adjacent solutions. Use when the user asks whether an idea already exists, how novel it is, who has tried it, or what the closest precedents are. Search beyond the user's exact wording and give a sourced novelty assessment with research limits. Do not use primarily to judge whether the idea is good.
---

# Am I Genius

Treat the title lightly and the research seriously.

## Establish the idea

Before searching, identify:

- the underlying problem;
- the proposed mechanism;
- the target user or use case, when relevant;
- what the user believes may be different.

Ask a short question only when the answer would substantially change the search. Otherwise, state the working interpretation and proceed.

## Search for disconfirming evidence

1. Generate search concepts for the problem, mechanism, use case, synonyms, alternative terminology, adjacent industries, and historical equivalents. Do not rely on the user's exact phrase.
2. Choose the source classes that can realistically contain prior art for this subject, then search them broadly. Consider product and company sites, GitHub, papers, patents, APIs, marketplaces, technical communities, forums, archived products, discontinued attempts, and adjacent fields when relevant.
3. Prefer primary sources for factual claims. Use community discussion to find terminology, adoption signals, objections, and failed attempts—not as the sole proof of a product's capabilities. Treat a patent as evidence that an idea was disclosed, not that it became a working or adopted product.
4. Actively seek the strongest threat to novelty. Verify close matches deeply enough to compare the problem, mechanism, audience, implementation, timing, and current status.
5. Iterate across terminology and source classes until new searches stop producing materially different close matches, or until access or scope limits prevent useful progress.
6. Track search limits, including inaccessible sources, ambiguous dates, and areas not covered.

## Synthesize the result

Return a focused assessment:

- **Verdict:** already exists; mostly exists; old idea with a possibly different mechanism; established in research but not practice; no close match found; or another precise conclusion.
- **Closest matches:** only the few comparisons that materially affect the verdict.
- **What may still be different:** the defensible gap, if any.
- **What to learn from prior attempts:** especially failure modes or adoption barriers.
- **Confidence and limits:** what the search can and cannot establish.
- **Next move:** the fastest useful way to validate the remaining claim.

Cite claims near their sources. Never turn "not found" into "never existed."

## Keep the boundary clear

Answer: **How new is this really compared with what already exists?**

Novelty is separate from quality. Use `cut-the-bullshit` to judge whether the idea or decision is good.

## Examples

> "what if calendar only showed commitments that cost real money. did somebody already do this?"

Search the problem and mechanism across budgeting, calendar, travel, and commitment tools—not only that sentence.

> "am i genius or is there already a local-only AI UI for reading DJ library XML without writing to it"

Clarify the differentiator, then compare exact, partial, adjacent, and abandoned implementations before assessing novelty.
