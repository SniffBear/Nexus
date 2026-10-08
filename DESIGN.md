---
version: alpha
name: Nexus
description: A premium dark-first AI-native trading and social markets terminal with dense, highly legible financial workflows.
colors:
  background: "#0B0D10"
  surface: "#11151A"
  surface-elevated: "#171C22"
  border: "#252C34"
  text-primary: "#F4F6F8"
  text-secondary: "#9BA6B2"
  text-muted: "#66717D"
  accent: "#6EA8FF"
  positive: "#39D98A"
  negative: "#FF5C6C"
  warning: "#F5B94C"
  info: "#69B7FF"
typography:
  display:
    fontFamily: "Geist"
    fontSize: 32px
    fontWeight: 650
    lineHeight: 1.05
    letterSpacing: -0.025em
  body:
    fontFamily: "Geist"
    fontSize: 14px
    fontWeight: 400
    lineHeight: 1.45
  label:
    fontFamily: "Geist"
    fontSize: 12px
    fontWeight: 550
    lineHeight: 1.2
    letterSpacing: 0.01em
  numeric:
    fontFamily: "Geist Mono"
    fontSize: 13px
    fontWeight: 500
    lineHeight: 1.25
rounded:
  sm: 6px
  md: 8px
  lg: 12px
spacing:
  xs: 4px
  sm: 8px
  md: 12px
  lg: 16px
  xl: 24px
---

# Nexus Design System

## 1. Visual Theme & Atmosphere

Nexus is a serious, premium trading terminal. The interface should feel precise, calm under pressure, information-dense, and engineered rather than decorative.

The visual language is dark-first with cool neutral surfaces, crisp separators, compact controls, restrained depth, and strong numerical alignment.

Target density: high.
Target variance: controlled.
Target motion: restrained and functional.

Do not use generic AI-purple gradients, excessive glassmorphism, oversized marketing typography, decorative bento layouts, or generic crypto-exchange visual clichés.

## 2. Color Palette & Roles

- Background #0B0D10: primary application canvas.
- Surface #11151A: primary workspace panels.
- Surface Elevated #171C22: overlays, dialogs, focused controls.
- Border #252C34: separators and panel boundaries.
- Text Primary #F4F6F8: important content and values.
- Text Secondary #9BA6B2: supporting information.
- Text Muted #66717D: tertiary metadata.
- Accent #6EA8FF: primary interaction and selected navigation.
- Positive #39D98A: gains, favorable movement, successful states.
- Negative #FF5C6C: losses, adverse movement, destructive states.
- Warning #F5B94C: risk, caution, attention.
- Info #69B7FF: informational status.

Never communicate financial meaning with color alone. Pair color with labels, icons, position, or state.

## 3. Typography

Use Geist for interface typography and Geist Mono for financial numerics.

Financial values use tabular numerals and consistent precision. Prices, quantities, percentages, timestamps, APY, PnL, rankings, and order values should align cleanly.

Avoid oversized headings inside dense product screens.

## 4. Components

### Navigation
Compact, persistent, keyboard-friendly. Selected navigation uses the accent token with restrained emphasis.

### Panels
Prefer flat surfaces and crisp separators. Do not turn every region into a floating rounded card.

### Cards
Use cards only when elevation communicates hierarchy. Dense data should usually use rows, tables, dividers, and grouped regions.

### Buttons
Compact, high-contrast, explicit labels. Primary actions use the accent token. Destructive actions use the negative token and require confirmation when consequential.

### Inputs
Dense but readable. Clear labels, visible focus states, useful placeholder examples, and keyboard support.

### Tables
Use tabular numerics, consistent column alignment, compact rows, hover states, and truncation rules.

### Order Book
Use bid/ask hierarchy, aligned price/size columns, subtle depth visualization, and clear separation between sides. Never make depth visualization overpower the numbers.

### Charts
The chart is a primary workspace object. Controls should be compact and discoverable. Avoid decorative chart effects that compete with data.

### Status
Live, paper, delayed, sample, connected, disconnected, warning, and error states must be visually unmistakable.

### Overlays
Use the elevated surface for command palettes, dialogs, sheets, floating tools, and confirmation flows. Glass may be used sparingly here.

## 5. Layout Principles

Desktop-first terminal composition.

Use a persistent shell with:
- global navigation
- market context
- primary workspace
- contextual side panels
- bottom or secondary workspace for positions and portfolio information

Dense content should breathe through spacing and hierarchy rather than oversized containers.

Responsive behavior should reorganize information instead of simply shrinking desktop layouts.

## 6. Motion

Motion communicates state change, hierarchy, feedback, or transition.

Use short transform/opacity transitions. Respect prefers-reduced-motion.

Do not use decorative perpetual motion in financial data panels.

## 7. Accessibility

All interactive elements require visible focus states and keyboard access.

Icon-only buttons require accessible labels.

Do not rely on color alone.

Use semantic HTML before ARIA.

Support reduced motion.

Maintain strong contrast across dark and light themes.

## 8. Financial UX

Nexus must clearly distinguish:
- information
- research
- analysis
- recommendation
- order preparation
- execution
- automated execution

Live trading and paper trading must never be ambiguous.

Financial calculations belong to deterministic application services. UI mock values must be clearly treated as sample data.

AI surfaces should expose sources, data inputs, catalysts, risks, uncertainty, proposed actions, and user approval boundaries. Never expose private chain-of-thought.

Agent controls must expose permissions, monitored conditions, proposed actions, execution state, and revocation.

## 9. Brand Rules

The product name is Nexus.

Do not introduce alternate product names.

Do not create a second visual language for an individual screen.

The design system should feel like one continuous terminal from Terminal through Markets, Social, Prediction, Earn, Calendar, Portfolio, AI, Search, and Settings.
