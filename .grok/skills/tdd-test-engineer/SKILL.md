---
name: tdd-test-engineer
description: Design and implement focused tests for Nexus features using behavior-first development, regression protection, deterministic financial checks, and reliable integration coverage.
---

# TDD Test Engineer

Use this skill when implementing features, fixing bugs, or changing critical application behavior.

## Core workflow

Prefer:
1. define observable behavior
2. write or update a failing test when practical
3. implement the smallest change
4. run focused tests
5. run related regression tests
6. run broader checks when appropriate

Tests should validate behavior rather than implementation details.

## Nexus critical paths

Prioritize tests around:
- authentication
- authorization
- broker/account permissions
- live vs paper separation
- order validation
- order confirmation
- portfolio state
- PnL
- margin
- liquidation
- fees
- slippage
- position sizing
- agent permissions
- audit events
- WebSocket reconnect behavior

## Financial correctness

Critical financial calculations should have deterministic test vectors and boundary cases.

Test:
- zero
- negative/positive movement where applicable
- rounding
- precision
- minimum/maximum constraints
- insufficient balance
- invalid state transitions
- concurrent or repeated requests

Never weaken a financial test simply to make an implementation pass.

## AI behavior

Test AI integration at the tool and policy boundary.

Do not assert private chain-of-thought.

Instead test:
- sources
- structured outputs
- proposed actions
- permission checks
- uncertainty/risk fields
- refusal or escalation behavior

## Test quality

Avoid:
- brittle snapshots for dynamic financial data
- tests that depend on external services without isolation
- arbitrary sleeps
- hidden global state
- tests that only prove mocks called each other

Use deterministic fixtures and controlled clocks/data where required.

## Completion

A feature is not complete merely because the happy path works.

Include relevant:
- error
- loading
- empty
- permission denied
- timeout
- reconnect
- duplicate request
- boundary
- rollback

coverage.
