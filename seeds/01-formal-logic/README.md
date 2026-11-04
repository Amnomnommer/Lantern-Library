# Seed Package 01 — Formal Logic

**Package ID:** `foundation.formal_logic`  
**Inheritance:** `FORMAL_CORE` / `CORE`  
**Version:** 0.1.0 candidate  
**Dependencies:** none

## Purpose

Give Lantern a compact inherited propositional-logic floor. Lantern should not spend experiential-learning compute rediscovering modus ponens, implication direction, conjunction semantics, or elementary invalid inference patterns.

This package describes **formal derivability**, not empirical truth and never authority.

## Design choices

- Classical propositional logic is the initial formal system.
- Inclusive OR is the default; exclusive OR must be explicit.
- Contradiction in empirical/candidate knowledge does not enable unrestricted explosion. Lantern preserves conflict and abstains rather than deriving arbitrary claims.
- Failure to prove a proposition is not proof of its negation.
- Valid reasoning from false/unverified premises remains formally valid but does not promote the conclusion to authoritative factual memory.
- Rules are protected Core inheritance and cannot be modified by ordinary experiential learning.

## Machine files

- `package.json` — concepts, rules, invalid-inference guards, invariants and provenance.
- `tests.json` — loader/reasoner acceptance vectors.

The exact Schema-v3 loader contract may evolve in the main Lantern repository. These files are canonical seed intent; loader changes should migrate/validate them rather than silently reinterpret them.

## Scope intentionally deferred

Package 01 does **not** contain predicate variables over world entities, universal/existential quantification, relation transitivity metadata, set theory, probability, causality, modal logic, deontic logic, or empirical evidence rules. Those belong to later Core-45 packages.

## Review checklist

- [ ] Every rule is valid under the declared formal semantics.
- [ ] Every guard names an invalid inference or Lantern-specific conservative boundary.
- [ ] Tests include positive, negative/unknown and contradiction cases.
- [ ] No rule converts formal derivability into factual authority.
- [ ] No rule grants permissions or action capability.
- [ ] Package IDs and rule IDs remain stable after activation.
- [ ] Schema-v3A can load this package deterministically and reproduce the acceptance vectors.
