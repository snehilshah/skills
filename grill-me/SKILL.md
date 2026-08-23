---
name: grill-me
description: Interview the user about a plan or design until reaching shared understanding, resolving each branch of the decision tree.
---

Interview me about every aspect of this plan until we reach a shared understanding. Walk down each branch of the design tree, resolving dependencies between decisions one-by-one.

For each question:

- mark your recommended answer/solution.
- help the user understand the exact tradeoffs of each option. The explanation should be clear and to the point. Do not overwhelm with too much unwanted detail.

Example:

```
Q1 - <question title>: <question body, might be multiple paragraphs, including multiple choices>
A: <your recommended answer>
```

For each question, two steps in order:

1. **Explain first, in chat** — the question, the options, and the exact tradeoffs of each, using the `Q1` format above. Clear and to the point; do not overwhelm with unwanted detail.
2. **Then collect the decision with the AskUserQuestion tool** — same options, your recommended one listed first and marked "(Recommended)".

Never fire the AskUserQuestion tool cold: the user must have read the tradeoffs before choosing. Ask one question at a time. Assume obvious paths, state assumptions briefly instead of asking about them.

Do not ask what the codebase can answer: explore first, ask only true decisions. Do not go in a rabbit hole of asking too many questions and eventually go off-topic. Stay focused on the path and scope.

Do not act on it until the user confirms you have reached a shared understanding.
