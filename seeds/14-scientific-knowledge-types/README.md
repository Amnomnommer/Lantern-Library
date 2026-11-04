# Seed Package 14 — Scientific Knowledge Types

**Package ID:** `foundation.scientific_knowledge_types`  
**Inheritance:** `CONCEPTUAL_CORE` / `CORE`  
**Version:** 0.1.0 candidate

## Purpose

Begin Wave 3 by giving Lantern a typed scientific ontology.

The central rule is:

> **Scientific object type is not a confidence ranking.**

A theory does not become a law when enough evidence accumulates. Laws and theories generally perform different epistemic jobs.

## Initial object types

### Observation
Records what was observed under stated conditions.

### Measurement
A structured quantitative/qualitative observation with method, uncertainty and scope.

### Hypothesis
A proposed testable/evaluable claim, explanation or prediction.

### Empirical regularity
A recurring observed relationship/pattern, potentially without explanation.

### Scientific law
A compact descriptive generalization of a regularity under stated scope/conditions.

### Scientific model
A simplified representation used to describe, explain, predict or simulate.

### Scientific theory
A broader explanatory framework integrating evidence/models/mechanisms and generating predictions.

## Relationships

Schema-v3 should be able to represent relationships such as:

```
theory EXPLAINS observation
theory EXPLAINS law
theory PREDICTS observation
law DESCRIBES regularity
model PREDICTS result
observation SUPPORTS hypothesis
observation CHALLENGES theory
model REFINES model
theory SUPERSEDES theory in scope
```

These are explicit relationships, not automatic type transitions.

## Confidence is orthogonal

A theory may be extremely well supported.

A proposed law-like regularity may be weakly supported.

The type tells Lantern **what kind of scientific claim/object it is**. Evidence/status tells Lantern **how strongly it is currently supported**.

## Consensus

Scientific consensus is useful metadata about the state of expert/evidence convergence. It is neither meaningless nor a truth-maker.

## Anomalies

A reliable anomaly should trigger investigation. It should not be suppressed because a theory is established, nor should one anomaly automatically destroy an otherwise successful theory before measurement, assumptions and scope are checked.

## Historical development

Later Package 18 handles review/freshness, and future historical-belief packages will represent how scientific objects changed over time. Package 14 establishes the object types required for that genealogy.

## Review checklist

- [ ] Theory is not represented as "unproven law."
- [ ] Law is not represented as "more true than theory."
- [ ] Confidence/status is separate from type.
- [ ] Observations remain distinct from interpretations.
- [ ] Models retain assumptions and scope.
- [ ] Predictions retain provenance.
- [ ] Consensus is informative but not truth.
- [ ] Anomalies trigger investigation rather than automatic rejection.
- [ ] Superseded models may remain valid approximations in narrower scopes.
