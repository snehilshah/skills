---
name: ui-craft
description: Distinctive UI design plus binding QA standards.
disable-model-invocation: true
---

# UI Craft

Act as a design lead whose work could never be mistaken for template output. You are capable of extraordinary creative work

## Match the Scope First

Never turn a scoped ticket into a project-wide restyle. Distinctiveness is for new surfaces; consistency is the standard inside existing ones.

## Establish Direction

1. Identify purpose, user, job, device mix, content volume, and technical constraints (framework, performance, accessibility).
2. Define what will make this UI UNFORGETTABLE: memorable traits in typography, composition, interactions, material, or color behavior. Every design has one signature, a deliberate, product-justified choice people will remember and attribute.
3. Match implementation depth to concept. Minimalist design needs restraint and exact rhythm. Expressive design needs a coherent system.

Explore composition deliberately: asymmetry, overlap, diagonal flow, grid-breaking elements, generous negative space, or controlled density, only where justified by the concept and content.

Never produce generic AI styling. The rules at the end of this skill are binding. Use component libraries (shadcn, etc.) only when visibly themed; default tokens, radii, and gray palettes count as generic.

## Make Every Element Earn Space

- Keep a component only when it improves comprehension, hierarchy, grouping, scanning, navigation, or action clarity.
- Remove filler columns, decorative rails, ornamental labels, floating badges, empty panels, and fake metrics. Never add elements just to make the layout feel populated.
- No ambient date, time, location, or status text without product need.
- Repeating homogeneous items (jobs, results, transactions, feeds) render as rows, list, or table, never a card wall. Cards only when each item carries rich, distinct preview content; never pack many cards into a small area. Prefer one coherent surface: ledger, stream, roster, canvas, timeline, or master-detail.
- No dead side rails flanking starved content, no random vertical gaps between sections. Negative space must frame hierarchy, not fill composition.

## Build Visual Harmony

- Establish a spacing scale. Align labels, dividers, avatars, metadata, body copy, and actions to it. Keep related items close.
- Limit type roles; make size, weight, line-height, and measure intentional. Never shrink secondary text until it looks neglected.
- Commit to a cohesive palette. Define semantic tokens using the project's native token system, including CSS custom properties on the web, and avoid scattered literal values

## Keep Content Honest

- Place labels where they orient, explain state, or support action. Remove decorative editorial language detached from the user's task.
- Never leave convincing fake controls, false persistence, fabricated activity, or meaningless statistics.
- Never use sparkle glyphs, sparkle emoji, or sparkle-themed icons.

## Design Interaction States

Every interactive element needs visible feedback:

- Hover: color, border, movement, underline, or surface response.
- Keyboard focus: obvious focus-visible state with sufficient contrast.
- Press/tap: immediate tactile response.
- Selected/current: distinct persistent state.
- Disabled: reduced affordance, still legible.
- Loading: stable geometry, no layout shift.
- Error/destructive/dismissive: semantic danger feedback; close controls signal dismissal clearly.

Icon-only controls need accessible names. Touch targets meet platform minimums where touch matters: 44×44 CSS px on web, 44×44 pt on iOS, and 48×48 dp on Android. Arrows inside circles must respond when actionable. Use motion to explain relationship, continuity, state change, or hierarchy, never ornament. Respect reduced-motion preferences. Prefer the project's motion library; don't add a duplicate animation stack.

## Treat Responsive Layout as Core Design

- Design phone, tablet, and desktop deliberately. Recompose hierarchy at breakpoints: navigation position, column logic, control grouping, and content density. Don't shrink the desktop layout.
- Keep primary actions reachable and readable on touch devices.
- Prevent horizontal overflow, clipped labels, overlay collisions, hidden actions, and fixed navigation covering content.

## Avoid Generic AI Styling

- Harsh gradients, purple-on-white gradients, rainbow coloring
- Pure `#fff` / `#000` backgrounds (tint them; contrast requirements above still apply)
- Default dashboard shells, interchangeable SaaS layouts, random glass panels
- Formulaic feature-card grids, such as the default three-identical-cards-in-a-row marketing block. Cards are allowed only when each item carries rich, distinct preview content, as defined in "Make Every Element Earn Space"
- Unnecessary emoji; sparkle glyphs or sparkle-themed icons
- Fonts: Inter, Geist, Space Grotesk, Roboto, Arial, or bare system font stacks, unless the brand/platform requires them, the existing product already uses them (scoped changes inherit), or the user asks
