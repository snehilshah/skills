# Agent Skills

This repository keeps one shared skill set with small, explicit adaptations for
Claude, Codex, and Gemini.

## Source of truth

`main` is the canonical source for skill content. Make shared instruction,
description, and behavior changes on `main` first.

A global `.agents` checkout is intentionally not used. Each agent needs
different metadata and tool names, and a shared global directory would either
duplicate skills or erase those platform-specific adaptations.

## Branches

- `main` — canonical shared skills.
- `claude` — `main` plus one Claude-specific overlay commit. Adds
  `disable-model-invocation: true` and uses `AskUserQuestion`.
- `codex` — `main` plus one Codex-specific overlay commit. Adds
  `agents/openai.yaml`, ignores Codex-managed `.system/`, and uses
  `request_user_input`.
- `gemini` — `main` plus one Gemini-specific overlay commit. Omits the built-in
  `grill-me` skill and uses `ask_user`.
- `inventory` — quarantined skills that are not approved for `main`. Audit them
  before promoting or deleting them; do not use this as an active agent branch.
- `archive/pre-align-*-20260824` — immutable recovery snapshots from before the
  branch realignment.

## Drift rules

1. Shared `SKILL.md` content must match `main` unless the branch list above
   requires a platform-specific edit.
2. Keep each active agent branch exactly one overlay commit ahead of `main`.
3. Do not make shared edits directly on an agent branch.
4. Unexpected skill directories are drift. Preserve uncertain skills in
   `inventory` for review instead of silently adopting them.
5. Codex-managed `.system/` is an allowed local exception and is not inventory.

## Updating skills

Commit and push shared changes from the canonical checkout:

```bash
cd ~/myCodes/skills
git switch main
git pull --ff-only
# edit, commit, and push the shared change
```

Then update each agent checkout by rebasing its single overlay commit:

```bash
git fetch origin
git rebase origin/main
git push --force-with-lease origin <claude|codex|gemini>
```

Resolve conflicts by keeping the new `main` content and reapplying only the
documented platform adaptation. Before pushing, verify that the checkout is
clean and that `git rev-list --count origin/main..HEAD` returns `1`.
