# Nexus

## Product

Nexus is an AI-native trading and social markets **application** built around configurable financial workspaces.

The product combines active trading, market discovery, social intelligence, prediction markets, portfolio management, Earn, calendar, AI Co-Invest, AI agents, automation, and security.

## Naming

The product is called Nexus. Do not use alternate product names.

## Design authority

- DESIGN.md is the visual and information-architecture source of truth when present.
- STITCH.md contains Stitch workflow instructions.
- NEXUS_LAYOUT.md defines the canonical workspace/panel architecture.
- `design/references/` contains external UX references only; those references never override Nexus branding or tokens.
- Use project-local skills for design quality and accessibility.
- Financial UI must prioritize clarity, state semantics, risk visibility, and confirmation.

## Product shell

The default application shell uses:
- persistent horizontal top navigation
- contextual market ticker
- configurable workspace canvas
- contextual side panels
- expandable bottom account workspace
- global search, notifications, and account/environment controls

A persistent left rail is not the global navigation.

## Workspace rules

Treat panels as reusable product primitives.

Panels may be:
- moved
- resized
- collapsed
- hidden
- locked
- grouped
- docked
- restored from presets

Do not build a separate layout system for each screen.

## Theme

Dark is the default trading/execution theme.

Light is a first-class theme for research, social, leaderboard, calendar, prediction discovery, and settings.

Both themes use the same semantic token system and component architecture.

## Reference rules

Liquid may be used as a UX reference for:
- horizontal navigation
- flexible panel composition
- chart + order workflow
- feed/news/chat context
- bottom account tabs
- full-page discovery experiences
- layout customization

Do not copy Liquid branding, logos, assets, exact visual identity, or proprietary design details.

## Engineering

- Reuse established design tokens and components.
- Do not create a second design language per screen.
- Treat financial calculations as data-layer responsibilities, not UI guesses.
- Keep live, paper, delayed, and sample states explicit.
- Keep consequential actions confirmable.
