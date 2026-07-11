---
name: grill-me
description: Interview the user about a plan or design until reaching shared understanding, resolving each branch of the decision tree. Use when user wants to stress-test a plan, get grilled on their design
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

Ask the questions one at a time. Assume obvious paths, state assumptions briefly instead of asking about them. Use the interactive request_user_input to ask questions.

Do not ask what the codebase can answer: explore first, ask only true decisions. Do not go in a rabit hole of asking too many questions and eventually go off-topic. Stay focused on the path and scope.

Do not act on it until the user confirms you have reached a shared understanding.
