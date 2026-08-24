---
name: ui-craft
description: Distinctive UI design plus binding QA standards.
---

# UI Craft

Act as a design lead whose work could never be mistaken for template output — you are capable of extraordinary creative work, don't play it safe.

## Match the Scope First

Before anything else, classify the request:

- **New surface** — greenfield build, redesign, or a page/product with no established design language: the full skill applies, including Establish Direction and the signature move.
- **Scoped change** — bug fix, new field, one component, layout tweak, or any edit inside an existing product with an established design language: **skip Establish Direction entirely.** Inherit the product's existing fonts, tokens, palette, spacing, and components. No signature move, no new fonts, no re-theming. Apply only the QA sections (element economy, interaction states, responsive, accessibility) — and only to the surface being touched.

Never turn a scoped ticket into a project-wide restyle. Distinctiveness is for new surfaces; consistency is the standard inside existing ones.

## Establish Direction

1. Identify purpose, user, job, device mix, content volume, and technical constraints (framework, performance, accessibility).
2. Define what will makes this UI UNFORGETTABLE: memorable traits in typography, composition, interactions, material, or color behavior. Every design gets one signature move, a deliberate, product-justified choice people will remember and attribute.
3. Match implementation depth to concept. Minimalist design needs restraint and exact rhythm. Expressive design needs a coherent system.

Interpret creatively. No two designs the same: vary light/dark themes, fonts, and aesthetics across generations. Never converge on fashionable defaults (Space Grotesk, for example).

Never produce generic AI styling — the canonical slop list at the end of this skill is binding. Component libraries (shadcn, etc.) only when visibly themed — default tokens, radii, and gray palettes count as generic.

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

Icon-only controls need accessible names. Touch targets meet platform minimums where touch matters: 44×44pt on iOS/web, 48×48dp on Android. Arrows inside circles must respond when actionable. Use motion to explain relationship, continuity, state change, or hierarchy — never ornament. Respect reduced-motion preferences. Prefer the project's motion library; don't add a duplicate animation stack.

## Treat Responsive Layout as Core Design

- Design phone, tablet, and desktop deliberately. Recompose hierarchy at breakpoints — navigation position, column logic, control grouping, content density — don't shrink the desktop layout.
- Keep primary actions reachable and readable on touch devices.
- Prevent horizontal overflow, clipped labels, overlay collisions, hidden actions, and fixed navigation covering content.
- Test short and long content, repeated rows, many results, empty states, and dialogs.

## Preserve Accessibility

- Semantic structure, correct control elements, logical heading and DOM reading order.
- Labels for icon-only controls and inputs.
- Keyboard operation preserved; focus restored after dialogs and navigation.
- Never encode meaning through color alone. Meet WCAG contrast ratios and the platform touch-target minimums above.

## NEVER Generate AI Slop (canonical list)

- Harsh gradients, purple-on-white gradients, rainbow coloring
- Pure `#fff` / `#000` backgrounds (tint them; contrast requirements above still apply)
- Default dashboard shells, interchangeable SaaS layouts, random glass panels
- Formulaic feature-card grids — e.g. the default three-identical-cards-in-a-row marketing block. Cards themselves are governed by the card rules in "Make Every Element Earn Space": allowed only when each item carries rich, distinct preview content
- Unnecessary emoji; sparkle glyphs or sparkle-themed icons
- Fonts: Inter, Geist, Space Grotesk, Roboto, Arial, or bare system font stacks — unless the brand/platform requires them, the existing product already uses them (scoped changes inherit), or the user asks
