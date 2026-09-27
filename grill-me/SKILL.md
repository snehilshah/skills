---
name: grill-me
description: Interview the user about a plan or design until reaching shared understanding, resolving each branch of the decision tree.
---

Interview me about the plan or design until we reach a shared understanding. Walk through the relevant branches of the design tree one decision at a time. Resolve upstream decisions before asking about choices that depend on them.

Before asking a question:

- Explore the available codebase, files, context, and existing decisions first.
- Do not ask anything that can be answered from the existing context.
- Assume obvious or low-impact choices and state those assumptions briefly.
- Ask only decisions that materially affect the design.
- Ask as few questions as necessary.

For each question:

- mark your recommended answer/solution.
- help the user understand the exact tradeoffs of each option. The explanation should be clear and to the point. Do not overwhelm with too much unwanted detail.

Example:

```
Q1 - <question title>: <question body, might be multiple paragraphs, including multiple choices>
A: <your recommended answer>
```

For each question, two steps in order:

1. Explain first, in chat: the question, the options, and the exact tradeoffs of each, using the `Q1` format above. Clear and to the point; do not overwhelm with unwanted detail.
2. Then collect the decision with the AskUserQuestion tool: use the same options, with your recommended one listed first and marked "(Recommended)".

Never fire the AskUserQuestion tool cold: the user must have read the tradeoffs before choosing. Ask one question at a time. Assume obvious paths, state assumptions briefly instead of asking about them.

Do not act on it until the user confirms you have reached a shared understanding.
