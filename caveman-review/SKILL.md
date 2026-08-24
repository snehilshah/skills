---
name: caveman-review
description: Ultra-compressed code review comments. Each comment is one line, location, problem, fix.
---

Write code review comments terse and actionable. One line per finding. Location, problem, fix. No throat-clearing.

## Rules

Format: `L<line>: <prefix>: <problem>. <fix>.`; use `L<start>-<end>` for a range and `<file>:L<line>: ...` when reviewing multi-file diffs.

Line numbers are file-relative in the post-change version (the numbers shown on the right side of the PR diff), never diff-hunk offsets.

Optionally open with one summary line: the overall verdict in a single sentence. All praise lives there; never per-comment.

Severity prefix (always, exactly one per finding, one per line):

- `BUG:` broken behavior, will cause incident
- `RISK:` works but fragile (race, missing null check, swallowed error)
- `NIT:` style, naming, micro-optim. Author can ignore
- `Q:` genuine question, not a suggestion

Drop:

- "I noticed that...", "It seems like...", "You might want to consider..."
- "This is just a suggestion but..."; use `NIT:` instead
- "Great work!", "Looks good overall but..."; say it once at the top, not per comment
- Restating what the line does; the reviewer can read the diff
- Hedging ("perhaps", "maybe", "I think"); if unsure use `Q:`

Keep:

- Exact line numbers
- Exact symbol/function/variable names in backticks
- Concrete fix, not "consider refactoring this"
- The reason if the fix isn't obvious from the problem statement

## Examples

AVOID: "I noticed that on line 42 you're not checking if the user object is null before accessing the email property. This could potentially cause a crash if the user is not found in the database. You might want to add a null check here."
PREFER: `L42: BUG: user can be null after .find(). Add guard before .email.`

AVOID: "It looks like this function is doing a lot of things and might benefit from being broken up into smaller functions for readability."
PREFER: `L88-140: NIT: 50-line fn does 4 things. Extract validate/normalize/persist.`

AVOID: "Have you considered what happens if the API returns a 429? I think we should probably handle that case."
PREFER: `L23: RISK: no retry on 429. Wrap in withBackoff(3).`

## Auto-Clarity

Drop terse mode for: security findings (CVE-class bugs need full explanation + reference), architectural disagreements (need rationale, not just a one-liner), and when the user says the author is new/onboarding and needs the "why". In those cases write a normal paragraph, then resume terse for the rest.

## Boundaries

Reviews only. Does not write the code fix, approve or request changes, or run linters. Output the comments ready to paste into the PR.
