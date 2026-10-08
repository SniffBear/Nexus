# FOMO Stitch Build Instructions

## Purpose
Use Google Stitch to design FOMO as one coherent product system, not unrelated screens.

FOMO is an AI-native trading and social markets platform combining a dense trading terminal, multi-asset and perpetual markets, prediction markets, social feed, news, watchlists, portfolio/PnL, calendar, Earn, AI Co-Invest, AI agents, paper trading, and permissions/audit controls.

## Design read
Reading this as: dense financial product UI for active traders, investors, prediction-market users, and AI-assisted portfolio builders, with a premium dark trading-cockpit language, leaning toward a custom tokenized React/Tailwind system with restrained glass and high information density.

## FOMO-specific visual dials
- DESIGN_VARIANCE: 5
- MOTION_INTENSITY: 4
- VISUAL_DENSITY: 9

These override the anti-slop skill baseline for FOMO because FOMO is dense product UI. Apply the uploaded Taste skill selectively as a visual quality and anti-slop guardrail. The skill itself explicitly says it is not for dashboards, data tables, or dense product UI.

## System rules
- Dark-first, with a light theme from the same semantic token system.
- Off-black and off-white instead of pure black/white.
- Compact product typography and tabular numerics for prices, quantities, percentages, timestamps, APY, PnL, and rankings.
- One consistent icon family.
- Avoid generic AI-purple gradients and excessive glass.
- Dense data should use flat surfaces and 1px separators more than heavy cards.
- Glass is reserved for overlays, command palette, floating tools, dialogs, and selected premium controls.
- Pick one radius system and keep it consistent.
- Motion must communicate hierarchy, feedback, state change, or transition and honor reduced motion.
- Never rely on color alone for positive, negative, warning, or neutral state.

## Global app shell
Primary navigation:
1. Terminal
2. Markets
3. Social
4. Prediction
5. Earn
6. Calendar
7. Portfolio
8. AI
9. Search
10. Settings

Global utilities:
- profile/account
- notifications
- live vs paper trading indicator
- account/environment selector
- connection/data status
- global search / command palette

## Required Stitch screens
1. Terminal / Home
2. Market Detail
3. Trade Ticket
4. Portfolio
5. Social Feed
6. Prediction Markets
7. Leaderboard
8. Earn
9. Calendar
10. AI Co-Invest
11. AI Agent Control Center
12. Search / Command Palette
13. Settings / Security

### 1. Terminal / Home
- market selector/ticker
- watchlist
- primary market chart
- order book
- order entry
- open positions
- portfolio/PnL summary
- social/news context
- market hours/data status

### 2. Market Detail
- instrument header
- price/change
- timeframe controls
- chart
- order book
- recent trades
- market statistics
- related news
- social thesis context

### 3. Trade Ticket
- buy/sell
- order type
- size and price
- leverage/margin where applicable
- estimated fees and slippage
- risk checks
- review and confirmation
- live/paper indicator
- make consequential action unmistakable

### 4. Portfolio
- equity
- available balance
- realized/unrealized PnL
- open positions
- allocation
- performance
- risk exposure
- filters/time range

### 5. Social Feed
- posts
- trading theses
- follows
- comments
- result/trade attachments
- asset context
- discovery controls
- avoid generic social-media clone styling

### 6. Prediction Markets
- market discovery
- probability
- liquidity
- contract detail
- order/position controls
- resolution status
- risk/disclosure context

### 7. Leaderboard
- ranking
- performance return
- risk-aware metrics where appropriate
- period selector
- trader profiles
- drilldown
- empty and anti-gaming states

### 8. Earn
- products
- APY/yield
- risk
- lockup/withdrawal conditions
- current positions
- allocation
- confirmation/disclosure
- never imply yield is risk-free

### 9. Calendar
- economic events
- earnings
- macro releases
- filters
- expected impact
- timezone-aware timestamps
- event detail

### 10. AI Co-Invest
- research brief
- thesis
- catalysts
- portfolio implications
- scenario analysis
- supporting sources/data
- risk flags
- proposed action
- explicit user approval boundary

### 11. AI Agent Control Center
- active agents
- purpose
- permissions
- monitored conditions
- proposed actions
- execution state
- audit trail
- pause/disable/revoke controls
- make agent authority obvious

### 12. Search / Command Palette
- global entity search
- commands
- recent items
- keyboard navigation
- quick actions
- market/user/portfolio shortcuts

### 13. Settings / Security
- profile
- broker connections
- API keys
- MFA/passkeys
- active sessions/devices
- agent permissions
- audit logs
- security alerts

## Financial UX guardrails
- Treat financial values as sample/mock unless backed by application data.
- Do not invent fake precision.
- Label live, delayed, paper, and sample states.
- Visually separate information, analysis, recommendation, order preparation, and execution.
- Make live vs paper trading unmistakable.
- Make consequential actions confirmable.
- Show agent permissions and revocation.
- Surface source/data receipts for AI outputs.
- Never show private chain-of-thought. Show concise reasoning summaries, sources, inputs, catalysts, risks, and proposed actions.

## Stitch generation workflow
For every screen:
1. Find the existing FOMO Stitch project.
2. Inspect existing screens and tokens before creating a new screen.
3. Reuse the established app shell and components.
4. Generate the desktop-first state.
5. Generate responsive variants where information architecture changes.
6. Add loading, empty, error, disabled, selected, hover, focus, and confirmation states.
7. Review against the FOMO system before moving on.
8. Do not invent new navigation, typography, radii, colors, or interaction patterns per screen.

## Prompt template

Create a production-quality FOMO [SCREEN NAME] screen for a dense dark-first trading terminal.

Audience:
Active traders, investors, prediction-market users, and AI-assisted portfolio builders.

Product context:
FOMO is an AI-native trading and social markets platform. Reuse the existing FOMO app shell and design tokens from the Stitch project.

Visual system:
- dark-first
- dense but legible
- premium trading cockpit
- flat data surfaces with 1px separators
- restrained glass for overlays only
- tabular financial numerics
- consistent icon family
- no AI-purple gradients
- no decorative dashboard-card clutter
- no generic crypto-exchange clone styling

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
- component consistency
- no unnecessary cards
- no clipping in tables/order books
- correct numeric alignment
- keyboard-accessible controls
- visible focus states
- semantic HTML mapping
- sufficient contrast
- reduced-motion behavior
- light/dark token parity
- clear live/paper state
- clear positive/negative/risk semantics
- empty/loading/error states
- explicit mobile fallback

Use the Web Interface Guidelines skill as the final UI/accessibility audit.

## Suggested build order
1. Terminal / Home
2. Market Detail
3. Trade Ticket
4. Portfolio
5. Social Feed
6. Prediction Markets
7. Leaderboard
8. Earn
9. Calendar
10. AI Co-Invest
11. AI Agent Control Center
12. Search / Command Palette
13. Settings / Security

After the first 3 screens are stable, extract the shared design system and reuse it across the rest.
