# Skill evals

This is a small manual set for checking two things: whether the right skill activates, and whether using it produces a meaningfully better result. The prompts are intentionally uneven; people do not type benchmark prose.

`Should not trigger` cases name the sibling skill that should handle the request instead. Messy and edge cases may go either way—the expected route is stated explicitly.

## Workflow

1. Run the same request without intentionally invoking the target skill.
2. Run it again with the target skill.
3. Compare the outputs.
4. Score both with the rubric below.
5. Note concrete failure modes: wrong activation, unnecessary questions, vague or overlong output, skill overlap, or no meaningful improvement over baseline.
6. Change `SKILL.md` only when the results reveal a real issue.
7. Re-run the relevant cases.

For `Should not trigger` cases, test implicit routing rather than forcing the wrong skill. Keep run outputs and scratch notes outside the repository unless they become useful project artifacts.

## Scoring

Score each dimension from 0 to 2. A strong result scores 2, a partial result 1, and a miss 0.

| Dimension | Question |
| --- | --- |
| Intent understood | Did it recover the actual request and important constraints? |
| Focused output | Is the result proportionate and easy to use? |
| Useful next step | Does it leave the user with a clear way forward? |
| Skill-specific value | Did the skill add value beyond competent baseline behavior? |
| No unnecessary BS | Did it avoid filler, performative depth, and needless questions? |

Maximum: **10**.

## `read-my-mind`

| ID | Expected route | Prompt |
| --- | --- | --- |
| R1 | Should trigger | `wait maybe it could just read the xml and tell me what to keep but like never delete anything?` |
| R2 | Should trigger | `need tell the team launch isnt cancelled exactly, we're just not doing the whole giant version first... idk how to frame what changed` |
| R3 | Should not trigger → `make-it-real` | `I want a local read-only DJ library auditor. Give me the smallest implementation plan.` |
| R4 | Should not trigger → `agentize-it` | `Turn this approved product brief into a paste-ready Cursor task. It may edit the web app but not the database schema.` |
| R5 | Messy; should trigger | `יש לי כזה רעיון... calendar שמראה רק דברים שאם אני מבטל אותם אני מפסיד כסף? אבל אולי זה בכלל לא calendar, מבין?` |
| R6 | Edge; should not trigger → `cut-the-bullshit` | `The concept is clear: a weekly email with three customer complaints. Is email actually the right format, or am I avoiding building a dashboard?` |

## `make-it-real`

| ID | Expected route | Prompt |
| --- | --- | --- |
| M1 | Should trigger | `I want a local read-only DJ library auditor. Give me the smallest implementation plan.` |
| M2 | Should trigger | `We have a room, two volunteer repairers, and a Saturday next month. Help me turn that into a tiny neighborhood repair night.` |
| M3 | Should not trigger → `read-my-mind` | `what if the notes kinda remembered why i almost picked something but didnt... not sure if this is a journal or decision thing yet` |
| M4 | Should not trigger → `cut-the-bullshit` | `Should this be a local tool or a web app? I think web might be more impressive.` |
| M5 | Messy; should trigger | `ok idea is fixed: private rss digest for 6 ppl, weekly, no accounts. whats the smalest thing i need to ship first` |
| M6 | Edge; should not trigger → `am-i-genius` | `Before I plan it, has anyone already made a browser extension that turns abandoned tabs into a reading queue based on why I opened them?` |

## `cut-the-bullshit`

| ID | Expected route | Prompt |
| --- | --- | --- |
| C1 | Should trigger | `Should this be a local tool or a web app? I think web might be more impressive.` |
| C2 | Should trigger | `Be honest: are microservices doing anything useful for this three-person internal tool, or are we buying complexity?` |
| C3 | Should not trigger → `am-i-genius` | `I have an idea for an AI tool that uses Rekordbox metadata and playlist context to decide which duplicate track version to keep. Does this already exist?` |
| C4 | Should not trigger → `make-it-real` | `We've chosen a local-first desktop app. Break the first usable version into a two-week implementation plan.` |
| C5 | Messy; should trigger | `תגיד דוגרי, 4 onboarding flows בשביל בערך 80 users זה personalization או שסתם הסתבכנו?` |
| C6 | Edge; should not trigger → `read-my-mind` | `i keep saying "community workspace" but i dont think thats what i mean. maybe people just leave unfinished things there? help me figure out the idea` |

## `agentize-it`

| ID | Expected route | Prompt |
| --- | --- | --- |
| A1 | Should trigger | `Here’s the v1 plan: add local Markdown import to the existing notes app, preserve frontmatter and internal links, reject files over 5 MB with a clear error, and add unit and integration tests. Turn it into the best Codex prompt and make it stop before committing.` |
| A2 | Should trigger | `Write Claude Code instructions for this refactor. It can change tests and source files, must preserve the public API, and must stop before committing.` |
| A3 | Should not trigger → `make-it-real` | `Build the smallest implementation plan for a local read-only photo deduplicator.` |
| A4 | Should not trigger → `read-my-mind` | `maybe ai could watch the support stuff and like tell us what keeps happening? not sure what i want it to output yet` |
| A5 | Messy; should trigger | `need a thing i can paste into Replit agent: add csv export, dont touch auth, test it. make it actually usable pls` |
| A6 | Edge; should not trigger → `cut-the-bullshit` | `For this repo, should I use Codex or Cursor? I care more about safe autonomous edits than autocomplete.` |

## `am-i-genius`

| ID | Expected route | Prompt |
| --- | --- | --- |
| G1 | Should trigger | `I have an idea for an AI tool that uses Rekordbox metadata and playlist context to decide which duplicate track version to keep. Does this already exist?` |
| G2 | Should trigger | `Has anyone built a calendar that shows only commitments with a real cancellation cost? Check products, prototypes, papers, and dead attempts—not just current apps.` |
| G3 | Should not trigger → `cut-the-bullshit` | `Nobody else is doing this, so we should build it. Is that reasoning actually sound?` |
| G4 | Should not trigger → `agentize-it` | `Turn my prior-art research plan into instructions for a Perplexity research task, with sources linked next to claims.` |
| G5 | Messy; should trigger | `am i genious lol: vscode thing that notices i keep undoing the same ai edit and changes the prompt rules. קיים כבר משהו כזה?` |
| G6 | Edge; should trigger | `I couldn't find an exact match for shared grocery lists that learn which substitutions each household member rejects. Search the underlying behavior too, including adjacent retail or recommendation systems.` |
