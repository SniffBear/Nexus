---
name: nextjs-fullstack
description: Apply disciplined Next.js full-stack architecture for Nexus, including server/client boundaries, data fetching, mutations, caching, authentication, API boundaries, and production behavior.
---

# Next.js Fullstack

Use this skill when building Nexus with Next.js.

## Architecture first

Before changing application structure:
- inspect the existing route tree
- identify server and client boundaries
- identify data ownership
- identify authentication and authorization boundaries
- identify existing API/service layers
- preserve the repository's established architecture

Do not introduce a new architectural pattern for one feature.

## Server/client boundaries

Prefer server-side work for:
- secure data access
- authenticated reads
- secrets
- privileged mutations
- database access
- server-only integrations

Use client components when interaction or browser state genuinely requires them.

Never expose:
- broker credentials
- API secrets
- private tokens
- privileged service credentials
- internal security policy

## Data flow

Keep financial calculations and business rules in deterministic application services.

UI components consume authoritative values.

Do not calculate critical:
- PnL
- margin
- liquidation
- fees
- slippage
- buying power
- position sizing
- portfolio returns

inside presentation components.

## Mutations

Consequential mutations should have:
1. validation
2. authentication
3. authorization
4. risk/eligibility checks where applicable
5. explicit confirmation where required
6. deterministic service execution
7. audit logging

Do not treat client-side validation as a security boundary.

## Caching and freshness

Market data, account state, order state, and AI research have different freshness requirements.

Do not apply a generic cache policy to all financial data.

Make freshness assumptions explicit.

For realtime state, prefer the project's WebSocket/realtime architecture over polling unless polling is intentionally justified.

## API design

Keep route handlers thin when business logic belongs in services.

Validate inputs at boundaries.

Return stable error shapes.

Do not leak internal exceptions, credentials, stack traces, or sensitive identifiers.

## Authentication and authorization

Authentication answers who the user is.

Authorization answers what they may do.

Agent permissions, broker permissions, paper/live permissions, and account scopes must be checked server-side.

## Production discipline

Before finishing:
- run type checking
- run linting
- run relevant tests
- run the production build when practical
- inspect changed routes/components
- check server/client boundaries
- check for accidental secret exposure
