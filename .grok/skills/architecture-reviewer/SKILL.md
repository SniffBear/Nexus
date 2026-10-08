---
name: architecture-reviewer
description: Review Nexus architecture for clear boundaries, scalability, reliability, security, data ownership, operational simplicity, and reversible technical decisions.
---

# Architecture Reviewer

Use this skill for repository architecture reviews, feature design reviews, refactors, and major technology decisions.

## Evidence rule

Do not invent architecture.

Classify important statements as:
- OBSERVED — directly supported by repository evidence
- INFERRED — strongly implied by evidence
- PROPOSED — a recommendation
- UNKNOWN — not established by available evidence

## Review dimensions

Evaluate:
1. boundaries and responsibilities
2. data ownership and consistency
3. scalability and performance
4. reliability and failure handling
5. security and authorization
6. observability and operations
7. developer complexity and maintainability
8. reversibility of the proposed change

## Nexus architecture

Preserve separation between:
- UI/presentation
- API/application services
- deterministic financial engines
- market/data services
- persistence
- realtime/event infrastructure
- AI Gateway
- permission engine
- agent orchestration
- external broker/provider integrations

Do not move financial truth into AI or presentation layers.

## AI boundary

AI may:
- research
- summarize
- analyze
- propose
- prepare actions

AI must not become the authoritative source for critical financial calculations.

Agent execution must pass through explicit permissions and deterministic application services.

## Review output

For each finding provide:
- evidence
- impact
- severity
- confidence
- recommendation
- trade-offs
- smallest safe next step

Prefer incremental changes over unnecessary rewrites.

Do not recommend microservices merely because a system is complex.

## Architecture change checklist

Before approving a major change ask:
- What boundary changes?
- Who owns the data?
- What becomes the source of truth?
- What happens during partial failure?
- How is authorization enforced?
- How is the change observed?
- How is it tested?
- How can it be rolled back?
