---
name: nexus-financial-engineering
description: Enforce Nexus financial correctness, execution boundaries, risk controls, deterministic calculations, live/paper separation, and auditable AI-agent financial workflows.
---

# Nexus Financial Engineering

This is a domain-specific safety and correctness skill for Nexus.

## Source of truth

Financial calculations belong to deterministic application services or engines.

Never use an LLM as the source of truth for:
- PnL
- margin
- liquidation price
- position sizing
- allocation
- fees
- slippage
- returns
- buying power
- leverage
- risk limits

AI may explain authoritative values returned by those systems.

## Execution boundary

Separate:
1. information
2. research
3. analysis
4. recommendation
5. order preparation
6. execution
7. automated execution

Moving from one stage to another requires an explicit application boundary.

## Live vs paper

Live and paper trading must be unambiguous.

Every consequential trading surface should expose the environment/state.

Never allow a UI ambiguity to determine execution environment.

Server-side authorization must enforce the selected environment.

## Order safety

Before consequential execution verify:
- authenticated user
- account scope
- live/paper environment
- product eligibility
- instrument validity
- order validity
- buying power/balance
- position/risk constraints
- user/agent permission
- confirmation requirement
- audit event

The exact checks depend on the product and execution architecture; do not invent unsupported rules.

## AI and agents

AI can:
- research
- summarize
- analyze
- identify catalysts
- identify risks
- propose strategies
- prepare orders

AI agents must have:
- explicit permissions
- scoped capabilities
- visible monitored conditions
- clear execution state
- revocation
- auditability

Never imply that a proposal has executed.

Do not expose private chain-of-thought. Use concise reasoning summaries, sources, data inputs, risks, uncertainty, proposed action, and resulting user action.

## Financial UI

Never invent financial precision.

Clearly label mock/sample values.

Do not make financial meaning depend only on red/green color.

Use consistent numerical precision and tabular alignment.

## Data integrity

Prefer authoritative backend values.

If data is delayed, stale, estimated, simulated, or unavailable, surface that state.

Never silently substitute fabricated values.

## Failure behavior

When an execution-related dependency fails:
- fail closed where safety requires it
- preserve the user's intent without silently executing a modified action
- surface a clear error
- record the appropriate audit/security event
- make retry behavior explicit

## Review questions

Before shipping a financial feature ask:
- Where is the authoritative calculation?
- Where is authorization enforced?
- Can live and paper be confused?
- Can an AI recommendation appear executed?
- What happens on stale/missing market data?
- What is logged?
- Can permissions be revoked?
- Are boundary cases tested?
