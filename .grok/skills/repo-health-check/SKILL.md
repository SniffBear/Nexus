---
name: repo-health-check
description: Audit the Nexus repository for structural drift, broken builds, dependency issues, dead code, inconsistent conventions, missing tests, and maintainability risks.
---

# Repo Health Check

Use this skill for periodic repository reviews or before major implementation work.

## Inspect before changing

Establish:
- repository structure
- package manager
- framework/runtime
- scripts
- test setup
- lint/typecheck/build commands
- environment/config conventions
- existing skill and instruction files

Do not rewrite project structure merely to make it look cleaner.

## Health areas

Review:
- build and type errors
- lint failures
- failing tests
- dependency drift
- duplicated components
- dead code
- inconsistent naming
- architecture boundary violations
- missing error handling
- missing accessibility states
- stale documentation
- accidental secrets/config exposure
- oversized or fragile modules

## Nexus-specific checks

Look for:
- inconsistent design tokens
- duplicated financial calculations in UI
- unclear live/paper state
- missing permission boundaries
- AI actions that bypass application services
- missing audit events for consequential operations
- realtime subscriptions that are not cleaned up
- sample data presented as authoritative

## Output

Rank findings:
- critical
- high
- medium
- low
- informational

For each finding include evidence and the smallest safe remediation.

Do not create a large refactor plan when a small fix is sufficient.

## Finish

If tools are available, run:
- typecheck
- lint
- tests
- build

Report exact failures rather than assuming their cause.
