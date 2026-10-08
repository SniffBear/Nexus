# Nexus Stitch Build Instructions

## Purpose

Use Google Stitch to design Nexus as **one coherent multi-workspace application**, not as a collection of unrelated screens and not as a single institutional trading cockpit.

The desired product shape is a flexible financial application with the interaction model of a modern trading/social platform, while preserving Nexus-specific intelligence, Solana-native workflows, AI, automation, wallet intelligence, and security.

**Do not reproduce Liquid's branding or visual identity. Use Liquid only as an information-architecture and interaction reference.**

## Design read

Read Nexus as:
- a premium financial application
- dense but approachable
- multi-workspace rather than single-terminal
- desktop-first with strong responsive reorganization
- dark-first, with a real light theme
- high information density
- configurable panels
- contextual social/news/AI surfaces

Nexus should feel closer to a flexible application such as Liquid than to Bloomberg, a generic crypto exchange, or a single-purpose derivatives terminal.

## Nexus-specific visual dials

- DESIGN_VARIANCE: 5
- MOTION_INTENSITY: 4
- VISUAL_DENSITY: 9

These override the anti-slop skill baseline for Nexus because Nexus is dense product UI. Apply the uploaded Taste skill selectively as a visual quality and anti-slop guardrail. The skill itself explicitly says it is not for dashboards, data tables, or dense product UI.

## Non-negotiable shell

### Global desktop shell

The primary navigation is a **horizontal top header**, not a persistent left navigation rail.

Default order:

1. Nexus
2. Trade
3. Markets
4. Predict
5. Social
6. Leaderboard
7. Earn
8. Calendar
9. Co-Invest
10. Agents
11. Search
12. Notifications
13. Account / wallet / environment

The header is compact and persistent.

Below it, trading-oriented workspaces may show a horizontal market ticker.

A left rail may exist only as a local workspace panel for:
- watchlists
- market lists
- feed filters
- tools
- contextual navigation

Do not make the left rail the application's main navigation.

### Market ticker

Use a compact ticker below the global header in Trade and Market workspaces.

Example content:
- SOL
- BTC
- ETH
- JUP
- selected markets
- price
- percent change
- live/data status

## Workspace model

Nexus is built around configurable workspaces.

A workspace is a saved arrangement of panels.

Panels can:
- move
- resize
- collapse
- hide
- lock
- dock
- group
- restore
- persist across sessions

The default Trade workspace should look structurally like:

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
│ Positions │ Balances │ Predictions │ Open Orders │ History │ PnL │ AI        │
└──────────────────────────────────────────────────────────────────────────────┘
```

The exact grid is flexible. The information hierarchy is not.

## Required shared panels

Build reusable panels for:

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

Every panel needs:
- loading
- empty
- error
- disabled
- selected
- hover
- focus
- collapsed
- locked
- data freshness state

## Bottom account workspace

Trading-oriented screens should have a bottom account workspace that can expand without leaving the market.

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

This is a core interaction pattern, not an optional decorative footer.

## Full-page application workspaces

Generate these as complete experiences using the same shell:

1. Trade
2. Markets
3. Social
4. Predict
5. Leaderboard
6. Earn
7. Calendar
8. Portfolio
9. Co-Invest
10. Agents
11. Search / Command
12. Settings / Security

Do not force every screen into the Trade terminal grid.

### Leaderboard

Use:
- top summary trader cards
- period filters
- search
- dense ranking table
- performance and risk metrics
- trader profile drilldown
- empty/anti-gaming states

### Calendar

Use:
- event calendar columns or dense event list
- earnings
- macro
- economic releases
- impact
- timezone-aware timestamps
- filters
- event detail

### Prediction

Use:
- category tabs
- featured market
- probability
- liquidity
- market cards
- market detail
- position/order controls
- resolution status
- risk/disclosure context

### Search

Use a global search experience with:
- Assets
- Predictions
- Users
- Traders
- Wallets
- Markets
- Strategies
- Agents
- News
- Commands

Support keyboard navigation and quick actions.

### Earn

Use:
- product discovery
- APY/yield
- risk
- lockup/withdrawal conditions
- current positions
- allocation
- disclosures

### Social

Use:
- feed
- trader context
- asset context
- follows
- comments
- trade/thesis attachments
- news
- chat

Avoid generic social-media clone styling.

## Feed, News, Chat

These are first-class contextual surfaces.

### Nexus Feed

Prioritize:
- Smart Money
- Trader Activity
- Market Alerts
- News
- AI Signals
- Social Theses
- Wallet Activity

The Feed should feel like market intelligence, not consumer social media.

### News

News may dock beside the chart, live in the bottom workspace, or occupy a research workspace.

### Chat

Chat should be contextual to:
- market
- asset
- trader
- prediction
- portfolio
- workspace

## Theme requirements

Dark is the default execution/trading theme.

Light must be a fully designed first-class theme, not a simple inversion.

Use light mode especially for:
- Social
- Leaderboard
- Calendar
- News/research
- Prediction discovery
- Settings

Use the same semantic tokens and components in both themes.

## Layout settings

Design a dedicated Layout settings screen with:
- freeform panel movement
- resize controls
- lock/unlock panels
- show/hide panels
- reset layout
- save workspace presets
- preset selection
- market ticker toggle
- watchlist toggle
- related assets toggle
- panel label toggle
- density selector
- theme selector

Recommended presets:
- Trader
- Scalper
- Swing
- Portfolio
- Research
- Social
- Prediction
- Minimal

## Nexus differentiation

Liquid-style structure is not the product itself.

Nexus must add:
- Solana-native market intelligence
- token safety and vetting
- smart-money discovery
- wallet intelligence
- AI analyst surfaces
- AI Co-Invest
- AI agents
- automation
- execution/risk telemetry
- paper/live clarity
- security controls

AI panels should expose:
- sources
- data inputs
- catalysts
- risks
- uncertainty
- proposed actions
- approval boundary

Never expose private chain-of-thought.

## Financial UX guardrails

- Treat financial values as sample/mock unless backed by application data.
- Do not invent fake precision.
- Label live, delayed, paper, and sample states.
- Visually separate information, analysis, recommendation, order preparation, and execution.
- Make live vs paper trading unmistakable.
- Make consequential actions confirmable.
- Show agent permissions and revocation.
- Surface source/data receipts for AI outputs.
- Never imply yield is risk-free.

## Responsive behavior

Do not simply shrink the desktop layout.

At smaller widths:
- collapse global navigation into a compact menu
- turn side panels into sheets/drawers
- prioritize chart + trade or chart + primary content
- make bottom account tabs horizontally scrollable
- collapse secondary panels
- preserve order entry access
- preserve live/paper state
- preserve critical risk and confirmation information
- use stacked layouts for leaderboard, calendar, prediction cards, and social content
- provide mobile-specific workspace presets

## Stitch generation workflow

For every screen:

1. Find the existing Nexus Stitch project.
2. Inspect existing screens and tokens before creating a new screen.
3. Reuse the global horizontal shell.
4. Reuse the shared panel system.
5. Generate the desktop-first state.
6. Generate responsive variants where information architecture changes.
7. Add loading, empty, error, disabled, selected, hover, focus, and confirmation states.
8. Validate dark and light themes.
9. Review against the Nexus design system.
10. Do not invent new navigation, typography, radii, colors, or interaction patterns per screen.

## Prompt template

Create a production-quality Nexus [SCREEN NAME] screen.

Product model:
Nexus is a multi-workspace AI-native trading and social markets application. It combines active trading, market discovery, social intelligence, prediction markets, portfolio management, Earn, calendar, AI Co-Invest, AI agents, automation, and security.

Shell:
Use the existing Nexus horizontal top navigation and market ticker. Do not use a persistent left rail as global navigation.

Workspace:
Use the existing Nexus configurable panel system. Panels can move, resize, collapse, hide, lock, and restore.

Visual system:
- dark-first
- complete light theme
- dense but legible
- premium financial application
- flat data surfaces with 1px separators
- restrained glass for overlays only
- tabular financial numerics
- consistent icon family
- no AI-purple gradients
- no decorative bento-card clutter
- no generic crypto-exchange clone styling

Reference:
Use Liquid only for information architecture and interaction patterns such as horizontal navigation, flexible panels, chart/order workflow, contextual feed/news/chat, bottom account tabs, full-page discovery, and layout customization. Do not copy branding, logos, colors, assets, or proprietary visuals.

Information architecture:
[describe exact regions, hierarchy, and priority]

Data:
[describe live vs sample data and label sample values]

States:
[loading, empty, error, disabled, selected, hover, focus, confirmation]

Risk:
[permissions, warnings, confirmations, disclosures, paper/live mode]

Responsive behavior:
[what collapses, docks, moves, hides, or becomes a sheet at smaller widths]

## QA loop

After each screen verify:
- horizontal shell consistency
- no global left-rail navigation
- component consistency
- panel resize/move affordances where relevant
- no unnecessary cards
- no clipping in tables/order books
- correct numeric alignment
- keyboard-accessible controls
- visible focus states
- semantic HTML mapping
- sufficient contrast
- reduced-motion behavior
- dark/light token parity
- clear live/paper state
- clear positive/negative/risk semantics
- empty/loading/error states
- explicit mobile fallback

Use the Web Interface Guidelines skill as the final UI/accessibility audit.

## Suggested build order

1. Shared shell + layout system
2. Trade
3. Market Detail
4. Portfolio
5. Social
6. Prediction
7. Leaderboard
8. Earn
9. Calendar
10. Co-Invest
11. Agents
12. Search / Command
13. Settings / Security

Do not polish individual pages before the shared shell and panel architecture are stable.
