# Seed Package 03 — Relation Logic

**Package ID:** `foundation.relation_logic`  
**Inheritance:** `FORMAL_CORE` / `CORE`  
**Version:** 0.1.0 candidate  
**Dependencies:** Formal Logic 0.1.0; Predicate and Quantifier Logic 0.1.0

## Purpose

Teach Lantern how relational predicates behave **when their properties are declared**, while preventing graph connectivity from masquerading as reasoning.

This package is intentionally aligned with Schema-v2's conservative relation catalog: nothing is transitive, symmetric, invertible, reflexive, or composable merely because a programmer or model finds that behavior plausible.

## Central rule

> **A path is not a claim.**

`R(a,b)` and `S(b,c)` establish a path. They produce `T(a,c)` only when a declared rule licenses that composition.

Likewise, `R(a,b)` does not produce `R(b,a)` unless R is symmetric, and two R edges do not produce a third unless R is transitive.

## Important distinctions

### Symmetric vs inverse

A symmetric relation uses the same predicate in both directions. An inverse may use a different predicate:

`parent_of(a,b) <-> child_of(b,a)`.

### Asymmetric vs antisymmetric

Asymmetric: if R(a,b), then not R(b,a).

Antisymmetric: if both R(a,b) and R(b,a), then a=b. This does not prohibit self-relations and is not the same property.

### Functional vs inverse-functional

Functional constrains the number of outputs for one input. It does not imply that an output has only one input.

### Declared property vs learned hypothesis

A few observed examples never promote a relation to FORMAL_CORE. Later Schema-v3 learning may propose a LEARNED hypothesis such as "R appears transitive in scope S," which remains evidence-revisable.

## Runtime relationship to Schema-v2

Schema-v2 already has a relation catalog with symmetry/transitivity/inverse/inference flags. The future Foundation loader should map compatible declarations rather than build a competing catalog. Package 03 supplies the inherited semantics and acceptance expectations; Schema-v2/v3 runtime code owns indexes and execution.

## Review checklist

- [ ] Argument order is preserved.
- [ ] Symmetry requires declaration.
- [ ] Inverse does not imply symmetry.
- [ ] Transitivity requires declaration.
- [ ] Arbitrary graph paths do not become claims.
- [ ] Composition requires an explicit composition rule.
- [ ] Asymmetric and antisymmetric remain distinct.
- [ ] Functional and inverse-functional remain distinct.
- [ ] Relation properties can be scoped.
- [ ] Examples cannot silently create Core relation properties.
- [ ] Existing Schema-v2 relation behavior can map without semantic regression.
