---
name: performance-optimizer
description: Diagnose and improve Nexus frontend, realtime, API, database, and rendering performance using measurement-first optimization.
---

# Performance Optimizer

Use this skill when performance is an explicit concern or when profiling reveals a bottleneck.

## Measurement first

Do not optimize by intuition alone.

Establish:
- affected workflow
- baseline metric
- target metric
- reproduction
- likely bottleneck
- measured result after change

Prefer real profiling, traces, query plans, browser performance data, and application metrics.

## Nexus hot paths

Pay special attention to:
- order book updates
- market tick streams
- charts
- large positions/orders tables
- portfolio refreshes
- WebSocket fan-out
- React render frequency
- expensive selectors
- database queries
- cache misses
- AI streaming interfaces

## Frontend

Avoid:
- unnecessary rerenders
- unstable object/function identities in hot paths
- rendering thousands of rows without virtualization
- expensive formatting on every tick
- duplicate realtime subscriptions
- unbounded client state

Use memoization only when measurement supports it.

## Realtime

Realtime updates should be:
- scoped
- deduplicated
- backpressure-aware where necessary
- safely unsubscribed
- resilient to reconnects

Do not sacrifice correctness for superficial latency gains.

## Backend and database

Inspect:
- query plans
- indexes
- N+1 access
- serialization overhead
- payload size
- connection pool behavior
- cache strategy

Keep financial correctness authoritative even when optimizing.

## Performance safety

Never remove:
- authorization
- risk checks
- audit logging
- confirmation boundaries
- deterministic financial calculations

for performance without an explicit architecture decision.

## Validation

After an optimization:
- compare against baseline
- run correctness tests
- inspect memory behavior
- test reconnect/error paths for realtime changes
- verify the UX did not become less usable
