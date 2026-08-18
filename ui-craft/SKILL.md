---
name: ui-craft
description: Distinctive UI design plus binding QA standards.
---

# UI Craft

Act as a design lead whose work could never be mistaken for template output — you are capable of extraordinary creative work, don't play it safe

## Establish Direction

1. Identify purpose, user, job, device mix, content volume, and technical constraints (framework, performance, accessibility).
2. Define what will makes this UI UNFORGETTABLE: memorable traits in typography, composition, interactions, material, or color behavior. Every design gets one signature move, a deliberate, product-justified choice people will remember and attribute.
3. Match implementation depth to concept. Minimalist design needs restraint and exact rhythm. Expressive design needs a coherent system.

Interpret creatively. No two designs the same: vary light/dark themes, fonts, and aesthetics across generations. Never converge on fashionable defaults (Space Grotesk, for example).

Never produce generic AI styling: harsh gradients, default dashboard shells, predictable card grids, purple-on-white gradients, random glass panels, interchangeable SaaS layouts. Component libraries (shadcn, etc.) only when visibly themed — default tokens, radii, and gray palettes count as generic.

## Make Every Element Earn Space

- Keep a component only when it improves comprehension, hierarchy, grouping, scanning, navigation, or action clarity.
- Remove filler columns, decorative rails, ornamental labels, floating badges, empty panels, and fake metrics. Never add elements just to make the layout feel populated.
- No ambient date, time, location, or status text without product need.
- Repeating homogeneous items (jobs, results, transactions, feeds) render as rows, list, or table — never a card wall. Cards only when each item carries rich, distinct preview content; never pack many cards into a small area. Prefer one coherent surface: ledger, stream, roster, canvas, timeline, or master-detail.
- Content width is a deliberate choice: narrow centered column for reading surfaces, full width for app and data surfaces. No dead side rails flanking starved content, no random vertical gaps between sections. Negative space must frame hierarchy, not fill composition.

## Build Visual Harmony

- Establish a spacing scale. Align labels, dividers, avatars, metadata, body copy, and actions to it. Keep related items close; separate groups consistently.
- Pair a distinctive display font with a highly legible body font when the product permits. Avoid generic defaults unless brand or platform requires them.
- Limit type roles; make size, weight, line-height, and measure intentional. Never shrink secondary text until it looks neglected.
- Commit to a cohesive palette. Define semantic tokens. Verify contrast on every surface.
- Keep dialogs, popovers, sheets, menus, and overlays opaque unless transparency has functional reason.
- Hard shadows, heavy black fills, and poster-like treatment only when the concept genuinely supports them — no neo-brutalism by default.

## Keep Content Honest

- Place labels where they orient, explain state, or support action. Remove decorative editorial language detached from the user's task.
- Never leave convincing fake controls, false persistence, fabricated activity, or meaningless statistics.
- Contextual icon or no icon. Never sparkle glyphs, sparkle emoji, or sparkle-themed icons.

## Design Interaction States

Every interactive element needs visible feedback:

- Hover: color, border, movement, underline, or surface response.
- Keyboard focus: obvious focus-visible state with sufficient contrast.
- Press/tap: immediate tactile response.
- Selected/current: distinct persistent state.
- Disabled: reduced affordance, still legible.
- Loading: stable geometry, no layout shift.
- Error/destructive/dismissive: semantic danger feedback; close controls signal dismissal clearly.

Icon-only controls need accessible names and 44px touch targets where mobile matters. Arrows inside circles must respond when actionable. Use motion to explain relationship, continuity, state change, or hierarchy — never ornament. Respect reduced-motion preferences. Prefer the project's motion library; don't add a duplicate animation stack.

## Treat Responsive Layout as Core Design

- Design phone, tablet, and desktop deliberately. Recompose hierarchy at breakpoints — navigation position, column logic, control grouping, content density — don't shrink the desktop layout.
- Keep primary actions reachable and readable on touch devices.
- Prevent horizontal overflow, clipped labels, overlay collisions, hidden actions, and fixed navigation covering content.
- Test short and long content, repeated rows, many results, empty states, and dialogs.

## Preserve Accessibility

- Semantic structure, correct control elements, logical heading and DOM reading order.
- Labels for icon-only controls and inputs.
- Keyboard operation preserved; focus restored after dialogs and navigation.
- Never encode meaning through color alone. Meet contrast and touch-target requirements.

## NEVER Generate AI Slop like

- Harsh gradients
- Pure white or black backgrounds
- Rainbow coloring
- Unecessary uses of emoji
- 3 feature cards in a row
- NEVER use Inter, Geist, Space Grotesk font, Inter, Roboto, Arial, system fonts unless asked
