# Seed Package 02 — Predicate and Quantifier Logic

**Package ID:** `foundation.predicate_quantifier_logic`  
**Inheritance:** `FORMAL_CORE` / `CORE`  
**Version:** 0.1.0 candidate  
**Dependency:** `foundation.formal_logic >= 0.1.0`

## Purpose

Extend Package 01 from whole propositions to predicates over entities and bounded domains. This gives Schema-v3A the inherited semantics required for variables, bindings, universal/existential claims, all/some/none reasoning, witnesses and counterexamples.

## Critical boundaries

- `FOR ALL` does not prove that an instance exists.
- `EXISTS/SOME` proves at least one witness exists but does not identify which object without a binding.
- SOME does not mean MOST or ALL.
- Quantifier order matters: `forall x exists y` is not `exists y forall x`.
- Quantified claims remain inside their declared domain/scope.
- A counterexample challenges a universal claim; it does not erase provenance or silently rewrite the original source claim.
- Free variables may not leak into conclusions.
- Predicate argument roles remain ordered.

## Empty-domain note

Classical first-order semantics can make universal statements vacuously true over an empty domain. Lantern should therefore keep **formal truth under a declared semantics** separate from ordinary-language existential implications. The seed forbids existential import from a universal statement unless non-emptiness/existence is separately established.

The `NOT FOR_ALL -> EXISTS NOT` transformation is marked with a non-empty-domain condition for Lantern's bounded operational semantics. The loader/reasoner must preserve declared rule conditions rather than dropping them.

## Scope intentionally deferred

Package 02 does not define whether particular world relations are symmetric/transitive/invertible; Package 03 owns relation logic. It also does not add set operations, probability, modal logic, causal inference, or empirical evidence weighting.

## Review checklist

- [ ] Universal instantiation respects domain membership.
- [ ] Existential generalization requires an actual witness.
- [ ] Universal claims do not gain existential import.
- [ ] Quantifier order cannot be silently reversed.
- [ ] Counterexamples produce conflict/challenge rather than arbitrary deletion.
- [ ] No free-variable leakage.
- [ ] Empty-domain semantics are explicit in implementation.
- [ ] Tests preserve NO/UNKNOWN/CONFLICT distinctions.
- [ ] Formal derivability never grants factual or action authority.
