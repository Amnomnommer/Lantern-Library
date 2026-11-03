# Seed Package 40 — AI Architectures and Evaluation

**Package ID:** `foundation.ai_architectures_evaluation`  
**Inheritance:** `AGENT_CORE` / `CORE`  
**Version:** 0.1.0 candidate

## Purpose

Represent AI architectures pluralistically and evaluate capability, resources, robustness, interpretability, safety and task fit without assuming larger neural models are the universal endpoint.

## Core concepts

- symbolic ai
- neural ai
- hybrid ai
- agent architecture
- memory system
- planner
- world model
- benchmark
- white box evaluation
- ablation
- resource efficiency
- robustness

## Core invariants

- AI architecture is selected by goals and constraints.
- Capability and resource efficiency are separate dimensions.
- White-box tests can complement benchmarks.
- Self-iteration remains bounded by evaluation and authority.

## Guardrails

- `benchmark_not_intelligence`
- `parameter_count_not_capability`
- `neural_not_only_ai`
- `symbolic_not_infallible`
- `simulation_not_agency`
- `self_improvement_not_agi`

## Review checklist

- [ ] Concepts remain scoped and provenance-aware.
- [ ] Guardrails reject category/authority collapses.
- [ ] No package grants action authority by itself.
- [ ] Conflicts remain reviewable rather than silently overwritten.
- [ ] Package integrates with prior Foundation Core dependencies.
