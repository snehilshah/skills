---
name: handoff
description: Compact the current conversation into a handoff document for another agent to pick up
argument-hint: "What will the next session be used for?"
---

Write a handoff document summarising the current conversation so a fresh agent can continue the work. Save it in the current project directory as `HANDOFF.md` (project root, or the project's docs folder if one exists).

## Structure

Use exactly these sections, in this order. Drop a section only if truly empty, never pad one.

1. Goal — what the overall effort is trying to achieve, one or two lines.
2. Current state — what is done and verified vs. done but unverified.
3. Next steps — ordered, concrete, starting with the immediate next action.
4. Blockers / open questions — anything unresolved, and who or what resolves it.
5. Key files & artifacts — paths and URLs (specs, plans, issues, commits, diffs) with a few words on why each matters.
6. Decisions & constraints — choices already made (with the why, if non-obvious) and every guideline the user stated this session: conventions, preferences, scope limits. The next agent must inherit these.

If the user passed arguments, treat them as what the next session will focus on and tailor the doc accordingly — especially Next steps.

## Style

Terse, maximum signal. Inline rules — do not invoke other skills for this:

- Drop articles, filler, pleasantries, hedging. Fragments OK.
- Keep every technical detail exact: names, paths, commands, versions, error messages quoted verbatim.
- Never compress into ambiguity. The reader has zero context — for orderings, warnings, and multi-step sequences, write full sentences.

## Content Rules

- No repetition inside the doc: each fact appears exactly once, in the section where it belongs.
- Content that already lives in other artifacts is referenced by path or URL in Key files, never pasted in.
- Never copy secrets (tokens, keys, passwords, connection strings) into the doc.
