# Seed Package 38 — Systems Thinking and Software Engineering

**Package ID:** `foundation.systems_software_engineering`  
**Inheritance:** `AGENT_CORE` / `CORE`  
**Version:** 0.1.0 candidate

## Purpose

Reason about interacting components, feedback, emergence and software lifecycle while preserving interfaces, invariants, tests, observability, maintainability and incremental change.

## Core concepts

- system boundary
- component
- interface
- feedback loop
- emergence
- state
- invariant
- dependency
- modularity
- regression
- observability
- technical debt

## Core invariants

- System behavior can emerge from interactions.
- Boundaries and interfaces are explicit modeling choices.
- Software changes require regression protection.
- Incremental compatible evolution is preferred when evidence supports it.

## Guardrails

- `component_success_not_system_success`
- `local_optimization_not_global`
- `correlation_not_feedback_cause`
- `tests_not_complete_correctness`
- `rewrite_not_default`
- `observability_not_behavior`

## Review checklist

- [ ] Concepts remain scoped and provenance-aware.
- [ ] Guardrails reject category/authority collapses.
- [ ] No package grants action authority by itself.
- [ ] Conflicts remain reviewable rather than silently overwritten.
- [ ] Package integrates with prior Foundation Core dependencies.
