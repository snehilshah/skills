---
name: design-integrity
description: Binding UI design and QA standards. Invoke for any interface build, redesign, or review.
disable-model-invocation: false
---

# Design Integrity

Build UI with identity, clarity, and operational truth. Treat rules below as binding for whole task. Do not relax them during iteration.
ACTIVE EVERY RESPONSE. No revert after many turns. No filler drift. Still active if unsure.

## Establish Direction

1. Identify user, job, context, device mix, content volume, and technical constraints.
2. Define memorable traits: typography, composition, interactions, material, or color behavior.
3. Match implementation depth to concept. Minimal design needs exact rhythm. Expressive design needs coherent system.

Do not produce generic AI styling: default dashboard shells, predictable card grids, purple-on-white gradients, random glass panels, interchangeable SaaS layouts, or fashionable fonts without product reason.
You are much more capable of making unique and great UI/UX. Feel free to take risks.

## Respect Reset Requests

When user requests new direction or design system from scratch:

- Do not reuse existing layout silhouette, information hierarchy, component grammar, or CSS theme as hidden base.
- Create independent tokens, markup, responsive rules, navigation logic, and screen composition.
- Reuse product facts and required behavior only.

## Make Every Element Earn Space

- Keep component only when it improves comprehension, hierarchy, grouping, scanning, navigation, or action clarity.
- Remove unnecessary filler columns, decorative rails, ornamental labels, floating badges, empty panels, and fake metrics.
- Do not add just add elements to make layout feel populated.
- Do not place ambient date, time, location, or status text without product need.
- Use only enough cards and text to orient user and support task.
- Prefer one coherent surface, ledger, stream, roster, canvas, timeline, or master-detail layout when card grid adds clutter.
- Avoid dead gaps that imply missing content. Negative space must frame hierarchy, not fill composition.

## Build Visual Harmony

- Establish spacing scale. Align labels, dividers, avatars, metadata, body copy, and actions to it.
- Keep related items close. Separate groups consistently.
- Use readable type sizes. Never shrink secondary text until it looks neglected.
- Choose distinctive display type plus highly legible body type when product permits.
- Avoid default generic font choices unless existing brand or platform requires them.
- Limit type roles. Make size, weight, line-height, and measure intentional.
- Commit to cohesive palette. Define semantic tokens. Verify contrast on every surface.
- Keep dialogs, popovers, sheets, menus, and overlays visibly opaque unless transparency has functional reason.
- Avoid neo-brutalism by default. Use hard shadows, heavy black fills, and poster-like treatment only when concept genuinely supports them.

## Keep Content Honest

- Place labels where they orient, explain state, or support action.
- Remove decorative editorial language detached from user task.
- Never leave convincing fake controls, false persistence, fabricated activity, or meaningless statistics.
- Use contextual icon or no icon. Never use sparkle glyphs, sparkle emoji, or sparkle-themed icons.

## Design Interaction States

Every interactive element needs visible feedback:

- Hover: color, border, movement, underline, or surface response.
- Keyboard focus: obvious focus-visible state with sufficient contrast.
- Press/tap: immediate tactile response.
- Selected/current: distinct persistent state.
- Disabled: reduced affordance without losing legibility.
- Loading: stable geometry. No layout shift.
- Error/destructive/dismissive: semantic danger feedback. Close controls should signal dismissal clearly.

Icon-only controls need accessible names and at least 44px comfortable touch target where mobile use matters. Arrows inside circles must respond when actionable.

Use motion to explain relationship, continuity, state change, or hierarchy. Avoid ornamental motion. Respect reduced-motion preferences. Prefer project motion library; do not add duplicate animation stack.

## Treat Responsive Layout as Core Design

- Design phone, tablet, and desktop deliberately. Do not shrink desktop layout.
- Recompose hierarchy at breakpoints. Change navigation position, column logic, control grouping, and content density as needed.
- Keep primary actions reachable and readable on touch devices.
- Prevent horizontal overflow, clipped labels, overlay collisions, hidden actions, and fixed navigation covering content.
- Test realistic short and long content. Test repeated rows, many results, empty states, and dialogs.

## Preserve Accessibility

- Use semantic structure and correct control elements.
- Keep logical heading order and DOM reading order.
- Provide labels for icon-only controls and inputs.
- Preserve keyboard operation and focus after dialogs or navigation.
- Do not encode meaning through color alone.
- Meet contrast and touch-target requirements.
