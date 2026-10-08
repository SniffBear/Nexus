---
version: alpha
name: Nexus
description: A premium multi-workspace AI-native trading and social markets application with a Liquid-inspired flexible workspace model, dense financial workflows, and Nexus intelligence.
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

## 1. Product shape

Nexus is a **multi-workspace trading application**, not a single-screen institutional terminal.

The primary product model is:

**Discover → Verify → Understand → Plan → Execute → Monitor → Learn → Automate**

Nexus should feel closer to a flexible financial application such as Liquid than to a Bloomberg clone, a generic crypto exchange, or a single-purpose derivatives cockpit.

Liquid is used only as an information-architecture and interaction reference. Nexus must retain its own brand, intelligence, Solana-native workflows, AI surfaces, wallet intelligence, automation, and security model.

### Core product areas

- Trade
- Markets
- Predict
- Social
- Leaderboard
- Earn
- Calendar
- Portfolio
- Co-Invest
- Agents
- Search
- Settings

**Terminal is a workspace, not the entire application.**

## 2. Visual Theme & Atmosphere

Nexus is serious, premium, precise, calm under pressure, information-dense, and engineered rather than decorative.

The visual language is **dark-first** with cool neutral surfaces, crisp separators, compact controls, strong numerical alignment, and restrained depth.

Target density: high.
Target variance: controlled.
Target motion: restrained and functional.

Do not use generic AI-purple gradients, excessive glassmorphism, oversized marketing typography, decorative bento layouts, or generic crypto-exchange visual clichés.

### Light theme is first-class

Nexus must support a complete light theme from the same semantic token system.

The light theme is especially appropriate for:
- Social
- Leaderboard
- Calendar
- News and research
- Prediction discovery
- Settings
- Research-heavy workspaces

Dark theme remains the preferred default for:
- Trade
- Terminal
- Charts
- Order book
- Execution
- Agent monitoring

Do not create separate component systems for light and dark. Only semantic tokens change.

## 3. Color Palette & Roles

- Background #0B0D10: primary dark application canvas.
- Surface #11151A: primary dark workspace panels.
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

The light theme must map the same semantic roles to light surfaces and dark readable text; do not hard-code component-specific colors.

## 4. Typography

Use Geist for interface typography and Geist Mono for financial numerics.

Financial values use tabular numerals and consistent precision. Prices, quantities, percentages, timestamps, APY, PnL, rankings, and order values should align cleanly.

Avoid oversized headings inside dense product screens.

## 5. Components

### Navigation

Use a **persistent horizontal global header** for the primary product navigation.

The default desktop shell is:

1. Nexus wordmark
2. Trade
3. Markets
4. Predict
5. Social
6. Leaderboard
7. Earn
8. Calendar
9. Co-Invest
10. Agents
11. Global Search
12. Notifications
13. Account / wallet / environment

The header must remain visually compact and leave most vertical space for the workspace.

A left rail is **not** the default global navigation. A left rail may be used inside a workspace for local tools, watchlists, or contextual navigation.

### Market context strip

Immediately below the global header, trading-oriented workspaces may use a compact horizontal market ticker.

It can show:
- SOL
- BTC
- ETH
- JUP
- selected markets
- percentage change
- price
- connection/live state

The ticker is contextual, not a replacement for the global header.

### Panels

Prefer flat surfaces and crisp separators. Do not turn every region into a floating rounded card.

Panels are first-class movable workspace objects. They can be:
- shown
- hidden
- collapsed
- resized
- moved
- locked
- grouped
- docked
- restored to preset position

### Cards

Use cards only when elevation communicates hierarchy. Dense data should usually use rows, tables, dividers, and grouped regions.

### Buttons

Compact, high-contrast, explicit labels. Primary actions use the accent token. Destructive actions use the negative token and require confirmation when consequential.

### Inputs

Dense but readable. Clear labels, visible focus states, useful placeholder examples, and keyboard support.

### Tables

Use tabular numerics, consistent column alignment, compact rows, hover states, truncation rules, sticky headers where appropriate, and density controls.

### Order Book

Use bid/ask hierarchy, aligned price/size columns, subtle depth visualization, and clear separation between sides. Never make depth visualization overpower the numbers.

### Charts

The chart is a primary workspace object. Controls should be compact and discoverable. Avoid decorative chart effects that compete with data.

### Status

Live, paper, delayed, sample, connected, disconnected, warning, and error states must be visually unmistakable.

### Overlays

Use the elevated surface for command palettes, dialogs, sheets, floating tools, and confirmation flows. Glass may be used sparingly here.

## 6. Workspace Architecture

The application is built around **configurable workspaces**.

A workspace is a saved arrangement of panels, not a single fixed page.

### Canonical Trade workspace

The default Trade workspace should support this composition:

```
┌──────────────────────────────────────────────────────────────────────────────┐
│ NEXUS │ Trade │ Markets │ Predict │ Social │ Leaderboard │ Earn │ Calendar  │
│       │ Co-Invest │ Agents                      Search  Alerts  Wallet      │
├──────────────────────────────────────────────────────────────────────────────┤
│ SOL +2.4% │ BTC -0.8% │ ETH +1.2% │ JUP +5.7% │ ...                         │
├──────────────────┬────────────────────────────────────┬──────────────────────┤
│ FEED / WATCHLIST │            CHART                   │ TRADE / ORDER BOOK   │
│ Smart Money      │                                    │ Buy / Sell           │
│ Trader Activity  │                                    │ Order Type           │
│ News             │                                    │ Size / Price         │
│ Alerts           │                                    │ Preview / Confirm    │
├──────────────────┴────────────────────────────────────┴──────────────────────┤
│ Positions │ Balances │ Predictions │ Open Orders │ Trade History │ PnL │ AI │
└──────────────────────────────────────────────────────────────────────────────┘
```

The exact grid is configurable. The composition is the default information hierarchy.

### Required first-class panels

- Market Selector
- Market Ticker
- Watchlist
- Feed
- Chart
- Order Book
- Trade / Order Ticket
- Recent Trades
- News
- Chat
- Positions
- Balances
- Predictions
- Open Orders
- Trade History
- Order History
- PnL
- Market Hours
- AI Intelligence
- Alerts

### Panel behavior

Every panel should define:
- minimum viable size
- preferred size
- collapse behavior
- mobile behavior
- loading state
- empty state
- error state
- locked state
- data freshness indicator

Users must be able to:
- drag panels
- resize panels
- collapse panels
- hide panels
- lock panels
- restore defaults
- save workspace presets
- switch presets

Recommended presets:
- Trader
- Scalper
- Swing
- Portfolio
- Research
- Social
- Prediction
- Minimal

### Bottom account workspace

Trading-oriented screens should use a persistent bottom workspace/dock for account-level information.

Default tabs:
- Positions
- Balances
- Predictions
- Open Orders
- Trade History
- Order History
- PnL
- Alerts
- AI Receipts

The bottom workspace can expand into a larger panel without navigating away from the market.

## 7. Full-page product workspaces

These are not widgets inside Terminal. They are first-class application experiences with the same global shell:

- Trade
- Markets
- Predict
- Social
- Leaderboard
- Earn
- Calendar
- Portfolio
- Co-Invest
- Agents
- Search
- Settings

Each page may use a different content composition while retaining the same header, tokens, typography, responsive rules, and interaction language.

Examples:
- Leaderboard: summary trader cards + dense ranked table.
- Calendar: event columns/list with filters and timezone controls.
- Prediction: featured market + category discovery grids + market detail.
- Search: global search modal/page with Assets, Predictions, Users, Wallets, Markets, Strategies, Actions.
- Earn: product discovery, APY, risk, positions, disclosures.
- Social: feed, trader context, asset context, chat, follow state.

## 8. Feed / News / Chat

These are first-class contextual surfaces inspired by modern financial social applications, but differentiated for Nexus.

### Feed

The Nexus Feed prioritizes:
- Smart Money
- Trader Activity
- Market Alerts
- News
- AI Signals
- Social Theses
- Wallet Activity

It should never look like a generic consumer social feed.

### News

News can dock beside the chart, open in a bottom workspace, or occupy a research workspace.

### Chat

Chat is contextual to:
- market
- asset
- trader
- prediction
- portfolio
- workspace

## 9. Search and command model

Global search is always available from the top shell.

Search across:
- Assets
- Markets
- Prediction Markets
- Users
- Traders
- Wallets
- Strategies
- Agents
- News
- Commands

Support keyboard navigation and quick actions.

## 10. Layout and personalization

Layout is a product feature.

Users can:
- choose a theme
- choose a workspace preset
- rearrange panels
- resize panels
- show/hide panels
- lock a layout
- reset a layout
- save multiple layouts
- choose compact/comfortable density
- toggle market ticker
- toggle watchlist
- toggle related assets
- toggle panel labels

Settings should expose these controls in a dedicated Layout workspace.

## 11. Motion

Motion communicates state change, hierarchy, feedback, or transition.

Use short transform/opacity transitions. Respect prefers-reduced-motion.

Do not use decorative perpetual motion in financial data panels.

## 12. Accessibility

All interactive elements require visible focus states and keyboard access.

Icon-only buttons require accessible labels.

Do not rely on color alone.

Use semantic HTML before ARIA.

Support reduced motion.

Maintain strong contrast across dark and light themes.

## 13. Financial UX

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

## 14. Brand and reference rules

The product name is Nexus.

Do not introduce alternate product names.

Do not create a second visual language for an individual screen.

Liquid is a **UX reference only**. Do not copy its logo, brand identity, proprietary assets, exact colors, or visual identity.

Borrow the useful product patterns:
- horizontal global navigation
- market ticker
- flexible panel composition
- chart + trade workflow
- contextual feed/news/chat
- bottom account tabs
- full-page discovery experiences
- layout customization

Add Nexus differentiation:
- Solana-native intelligence
- token safety
- smart-money discovery
- wallet intelligence
- AI research and agents
- automation
- security
- paper/live clarity
- execution and risk telemetry
