# Seed Package 07 — Scope and Context

**Package ID:** `foundation.scope_context`  
**Inheritance:** `CONCEPTUAL_CORE` / `CORE`  
**Version:** 0.1.0 candidate  
**Dependencies:** Formal Logic, Predicate/Quantifier Logic, Relation Logic, Epistemic States

## Purpose

Make scope a first-class part of Lantern's reasoning. Claims that look contradictory in plain text may both be appropriate when they refer to different times, places, populations, conditions, measurement regimes, models, speakers or hypothetical worlds.

## Scope dimensions

A proposition/rule may carry one or more of:

- domain;
- population;
- time;
- place/environment;
- conditions;
- measurement/operational definition;
- model assumptions;
- attribution;
- hypothetical/counterfactual world;
- discourse context.

Unknown scope is permitted. Unknown does not mean universal.

## Core application rule

A general rule may be applied to a case only when:

1. the case is inside the rule's applicable scope;
2. required conditions are satisfied;
3. no higher-priority epistemic constraint blocks the inference.

## Contradiction handling

Before declaring contradiction, Lantern should ask whether claims actually overlap in relevant scope.

"Door is open at 10:00" and "door is closed at 11:00" may describe change.

"Treatment helps population A" and "treatment does not help population B" may both be supported.

Scope difference does not prove either claim globally true or false.

## Model scope

A model can remain useful after a broader model exists. A later model may refine the earlier model's applicability rather than simply turn every older prediction into falsehood.

This prepares Lantern for scientific belief genealogy and the Newton/relativity style of scope reasoning discussed in the architecture design.

## Hypothetical and attribution boundaries

Claims inside stories, simulations, counterfactuals, quotations or another speaker's belief state remain contained there unless separately established in actual-world knowledge.

## Relationship to existing Lantern

Schema-v2 already stores time/place/context/attribution fields and CognitionTrace/Lens work with discourse context. The future loader should map Package 07 semantics onto those existing fields instead of introducing a parallel context system.

## Review checklist

- [ ] Rules require in-scope application.
- [ ] Unknown scope does not become universal scope.
- [ ] Time/place/population differences can prevent false contradiction.
- [ ] Narrow evidence cannot silently generalize.
- [ ] Hypothetical content cannot leak into actuality.
- [ ] Attribution cannot leak into truth.
- [ ] Model predictions are scope-bounded.
- [ ] Scope refinement preserves history/provenance.
- [ ] Existing Schema-v2 context fields are reused where compatible.
