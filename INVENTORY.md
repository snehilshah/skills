# Skill Inventory

This branch quarantines skills found outside the canonical `main` inventory.
Nothing here is approved for active agent branches until it is audited.

## Pending audit

- `frontend-design` — preserved from Gemini's pre-alignment branch after it was
  retired from `main` in favor of `ui-craft`.
- `playwright` — preserved from the untracked Codex checkout state found during
  the 2026-08-24 branch alignment.

Codex-managed `.system/` skills are reproducible platform content and are not
part of this inventory.

After review, promote an approved skill through `main` or remove it from this
branch. Do not merge the inventory branch wholesale into an agent branch.
