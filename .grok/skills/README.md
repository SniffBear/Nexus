# Nexus Agent Skills

This directory contains the project-local skills used by Grok Build.

## Design

- `design-taste-frontend` — visual quality and anti-slop guardrails.
- `web-design-guidelines` — accessibility and interface-quality review.
- `nexus-stitch` — Nexus design-system and Stitch workflow authority.

## Engineering

- `frontend-ux-engineer` — production UI behavior, accessibility, responsive UX, and states.
- `nextjs-fullstack` — Next.js server/client boundaries, data flow, mutations, auth, and caching.
- `architecture-reviewer` — evidence-based architecture and boundary review.
- `performance-optimizer` — measurement-first frontend, realtime, API, and database performance work.

## Quality

- `tdd-test-engineer` — behavior-first tests and regression protection.
- `repo-health-check` — repository health and architectural-drift checks.
- `git-github-flow` — focused branches, commits, PRs, and verification.

## Nexus-specific

- `nexus-financial-engineering` — deterministic financial correctness, execution boundaries, risk, permissions, and auditability.

## Usage

Grok Build discovers project-local skills from `.grok/skills/`. Run:

```bash
grok inspect
```

to verify which skills are discovered.

These Nexus-local skills are intentionally concise and project-specific. They are not intended to replace upstream framework documentation or security standards.
