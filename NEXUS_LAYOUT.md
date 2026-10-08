# Nexus Workspace Architecture

## Purpose

This document is the canonical information architecture for the Nexus configurable workspace system.

Nexus is a **multi-workspace application**. The Trade workspace is the primary dense terminal experience, but it is only one part of the product.

## 1. Global shell

Desktop:

```
┌──────────────────────────────────────────────────────────────────────────────┐
│ NEXUS │ Trade │ Markets │ Predict │ Social │ Leaderboard │ Earn │ Calendar  │
│       │ Co-Invest │ Agents                      Search  Alerts  Wallet      │
├──────────────────────────────────────────────────────────────────────────────┤
│ SOL +2.4% │ BTC -0.8% │ ETH +1.2% │ JUP +5.7% │ selected markets │ status  │
├──────────────────────────────────────────────────────────────────────────────┤
│                         CONFIGURABLE WORKSPACE                              │
├──────────────────────────────────────────────────────────────────────────────┤
│ Positions │ Balances │ Predictions │ Open Orders │ History │ PnL │ AI       │
└──────────────────────────────────────────────────────────────────────────────┘
```

The header is persistent. The ticker is contextual. The workspace is configurable. The bottom account area is expandable.

## 2. Global navigation

Primary:
- Trade
- Markets
- Predict
- Social
- Leaderboard
- Earn
- Calendar
- Co-Invest
- Agents

Global utilities:
- Search
- Notifications
- Account
- Wallet
- Live/Paper environment
- Connection/data status

Terminal is a workspace/preset name, not the global product identity.

## 3. Panel registry

Every panel should be implemented as a reusable primitive with a stable ID.

| Panel | Purpose | Default location |
|---|---|---|
| Market Selector | Choose active instrument/market | Top/left |
| Market Ticker | Cross-market context | Header |
| Watchlist | Track selected markets/assets | Left |
| Feed | Smart-money/social/alerts context | Left |
| Chart | Primary market visualization | Center |
| Order Book | Depth and market microstructure | Right |
| Trade Ticket | Prepare/execute orders | Right |
| Recent Trades | Recent market executions | Right/bottom |
| News | Market news | Left/bottom |
| Chat | Contextual conversation | Left/bottom |
| Positions | Open positions | Bottom |
| Balances | Account balances | Bottom |
| Predictions | Prediction positions/markets | Bottom |
| Open Orders | Active orders | Bottom |
| Trade History | Completed trades | Bottom |
| Order History | Historical orders | Bottom |
| PnL | Account performance | Bottom |
| Market Hours | Session state | Floating/bottom |
| AI Intelligence | AI market brief/signals | Left/bottom |
| Alerts | Active/triggered alerts | Bottom/floating |

## 4. Trade workspace

Default priority:

1. Active market
2. Chart
3. Order preparation/execution
4. Order book
5. Market/social intelligence
6. Account state

Default arrangement:

```
LEFT                  CENTER                         RIGHT
Feed / Watchlist      Chart                          Trade
Smart Money           Market stats                   Order Book
Trader Activity       Related assets                 Recent Trades
News / Alerts
```

Bottom:
```
Positions | Balances | Predictions | Open Orders | Trade History | Order History | PnL | Alerts | AI
```

The arrangement is a default, not a fixed page.

## 5. Workspace presets

Required presets:

### Trader
Chart + Order Book + Trade + Positions + Watchlist.

### Scalper
Large chart + compact order book + trade ticket + recent trades + alerts.

### Swing
Chart + Feed + News + AI Intelligence + Watchlist + Positions.

### Portfolio
Portfolio + PnL + Positions + Allocation + News + AI Intelligence.

### Research
News + Feed + Chart + AI Intelligence + Market stats.

### Social
Feed + Chat + Trader activity + selected asset/market context.

### Prediction
Prediction discovery + featured market + contract detail + positions.

### Minimal
Chart + Trade + compact market selector.

## 6. Panel interactions

All configurable panels support:

- drag
- resize
- collapse
- hide
- lock
- restore
- reset
- preset save
- preset switch

Show a visible but restrained drag/resize affordance only when layout editing is active.

Do not make every panel look like a floating card. The grid itself should communicate structure through separators and spacing.

## 7. Layout settings

Settings > Layout must provide:

- preset selector
- freeform movement
- panel visibility
- panel labels
- lock/unlock
- ticker visibility
- watchlist visibility
- related-assets visibility
- density
- theme
- reset
- save as preset

## 8. Full-page workspaces

Not every product area belongs inside the Trade grid.

### Markets
Discovery, asset lists, scanners, sectors/categories, market detail entry points.

### Social
Feed, trader profiles, follows, comments, theses, activity.

### Predict
Featured prediction, categories, market cards, market detail, positions.

### Leaderboard
Summary cards, filters, search, ranked table, trader profiles.

### Earn
Yield products, APY, risk, positions, allocation, disclosures.

### Calendar
Event timeline/calendar, filters, impact, timestamps, detail.

### Portfolio
Equity, balances, positions, allocation, PnL, performance, risk.

### Co-Invest
Research brief, thesis, catalysts, scenarios, portfolio implications, proposed action, sources, approval.

### Agents
Agent fleet, permissions, monitored conditions, proposed actions, execution state, audit trail, pause/revoke.

### Search
Global search and command execution across all supported entities.

### Settings
Security, connections, sessions, permissions, notifications, layout, themes.

## 9. Responsive model

Desktop:
- horizontal global header
- multi-column workspace
- bottom account workspace

Tablet:
- condensed header
- fewer simultaneous columns
- drawers/sheets for secondary panels
- horizontally scrollable bottom tabs

Mobile:
- compact header
- primary content first
- trade/order panel as sheet
- order book as sheet
- bottom navigation for product areas
- horizontally scrollable account tabs
- saved mobile workspace presets

Never simply scale desktop pixels down.

## 10. Design reference policy

Liquid is an external UX reference for:
- top navigation
- ticker context
- chart/order composition
- feed/news/chat
- bottom account tabs
- full-page discovery
- customizable layouts

It is not a source of Nexus branding, exact styling, logos, colors, or assets.

See `design/references/liquid/README.md`.

## 11. Data/state requirements

Every panel must make these states explicit where relevant:

- Live
- Paper
- Sample
- Delayed
- Connected
- Disconnected
- Loading
- Empty
- Error
- Stale
- Locked

Financial meaning must never depend on color alone.
