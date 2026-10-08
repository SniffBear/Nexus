---
name: frontend-ux-engineer
description: Build and review production-grade Nexus frontend workflows with strong interaction design, accessibility, responsive behavior, loading/error/empty states, and visual consistency.
---

# Frontend UX Engineer

Use this skill when implementing or reviewing Nexus frontend experiences.

## Core rule

Build the product workflow, not a static mockup. Every screen must account for real interaction states, keyboard use, responsive behavior, data lifecycle, permissions, and consequential actions.

## Nexus design authority

Read these before changing UI:
1. `DESIGN.md`
2. `STITCH.md`
3. `AGENTS.md`
4. Relevant project-local skills

Do not introduce a second visual language.

## Interaction requirements

For every interactive flow define:
- default
- hover
- focus-visible
- active
- selected
- disabled
- loading
- empty
- error
- success
- confirmation when consequential

Prefer semantic HTML and native controls before custom ARIA.

## Accessibility

- Keyboard navigation must be complete.
- Focus must remain visible.
- Icon-only controls need accessible names.
- Do not use color as the only state signal.
- Dialogs and menus need correct focus behavior.
- Respect reduced-motion preferences.
- Preserve readable contrast and text sizing.
- Tables need meaningful headers and relationships.

## Responsive behavior

Desktop is the primary Nexus terminal experience, but responsive behavior must reorganize information rather than merely shrink it.

Use:
- drawers
- sheets
- tabs
- collapsible regions
- sticky action areas
- progressive disclosure

Never hide a consequential action without providing an obvious equivalent.

## Financial UX

Clearly distinguish:
- information
- analysis
- recommendation
- order preparation
- execution

Clearly label:
- live
- paper
- delayed
- sample
- connected
- disconnected
- warning
- error

Never imply that an AI recommendation has executed.

## Component discipline

Reuse established components and tokens. Avoid one-off cards, arbitrary spacing, inconsistent radii, and screen-specific typography.

Dense financial information should generally use rows, tables, grouped panels, and separators rather than excessive floating cards.

## Validation

Before finishing a frontend task:
- inspect the changed UI at relevant breakpoints
- verify keyboard focus
- verify empty/loading/error states
- verify numeric alignment
- verify no clipping or overflow
- verify theme parity where supported
- verify reduced motion
- run the project's tests/build/lint when available
