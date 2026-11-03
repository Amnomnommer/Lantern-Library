# Seed Package 01 — Formal Logic

**Package ID:** `foundation.formal_logic`
**Version:** 0.1.0-draft
**Priority:** P0 / Wave 1
**Inheritance class:** `FORMAL_CORE`
**Dependencies:** none
**Revisability:** reviewed Foundation update only
**Purpose:** provide Lantern with the basic truth-functional structures humanity already knows so experience is spent learning about the world, not rediscovering elementary deductive logic.

## Boundary

This package defines formal relationships between propositions. It does **not** decide whether an empirical premise is true, assign permissions, provide moral conclusions, or supply domain facts. A valid deduction from false/uncertain premises does not make the premises true.

## Concepts to seed

### Proposition
A statement treated as having a truth status within a specified formal context.

### Truth states used by the formal core
- TRUE: proposition established true within the current formal premises.
- FALSE: proposition established false within the current formal premises.
- UNKNOWN: available premises establish neither proposition nor its negation.
- CONFLICT: available accepted premises support both proposition and its negation.

UNKNOWN is not FALSE. CONFLICT is not automatically resolved by choosing either side.

### Negation
`NOT P` is true when P is false in the same formal context.

### Conjunction
`P AND Q` requires both P and Q.

### Disjunction
Inclusive `P OR Q` requires at least one of P or Q unless a package explicitly declares exclusive-or.

### Implication
`P -> Q` means that within the rule's scope, P is sufficient for Q.

It does not by itself assert P or Q.

### Biconditional
`P <-> Q` means `P -> Q` and `Q -> P` within the same scope.

### Consistency
A premise set is inconsistent when it supports both P and NOT P in the same relevant scope/context.

## Valid core inference rules

### Modus ponens
Premises:
- P
- P -> Q

Conclusion:
- Q

### Modus tollens
Premises:
- P -> Q
- NOT Q

Conclusion:
- NOT P

### Conjunction introduction
Premises:
- P
- Q

Conclusion:
- P AND Q

### Conjunction elimination
Premise:
- P AND Q

Conclusions:
- P
- Q

### Disjunction introduction
Premise:
- P

Conclusion:
- P OR Q

This does not establish Q.

### Disjunctive syllogism
Premises:
- P OR Q
- NOT P

Conclusion:
- Q

### Hypothetical syllogism
Premises:
- P -> Q
- Q -> R

Conclusion:
- P -> R

Only when both implications occupy compatible scope/context.

### Biconditional elimination
Premise:
- P <-> Q

Conclusions:
- P -> Q
- Q -> P

### Double negation
`NOT NOT P` is equivalent to P in the classical formal context defined by this package.

### De Morgan transformations
- `NOT (P AND Q)` is equivalent to `(NOT P) OR (NOT Q)`.
- `NOT (P OR Q)` is equivalent to `(NOT P) AND (NOT Q)`.

## Invalid inference patterns Lantern must reject

### Affirming the consequent
Invalid:
- P -> Q
- Q
- therefore P

Q may have another cause/route.

### Denying the antecedent
Invalid:
- P -> Q
- NOT P
- therefore NOT Q

Q may still hold for another reason.

### Converse assumption
`P -> Q` does not imply `Q -> P`.

### Inverse assumption
`P -> Q` does not imply `NOT P -> NOT Q`.

### Unsupported conjunction
P alone does not establish `P AND Q`.

### Unsupported exclusivity
`P OR Q` is inclusive unless exclusivity is explicitly stated.

### Contradiction collapse
When both P and NOT P are present, Lantern must mark conflict/inspect scope rather than use classical explosion to derive arbitrary unrelated propositions.

Project Lantern deliberately uses contradiction-tolerant operational reasoning at the knowledge boundary even though classical logic permits explosion from inconsistency. This preserves Schema-v2's conservative epistemics.

## Formal versus empirical confidence

A formal inference can be valid while its empirical conclusion remains uncertain because premise confidence/provenance belongs to the empirical layer.

Example:
- Rule validity: valid modus ponens.
- Premise P confidence: 0.60.
- Rule `P -> Q`: inherited empirical rule, confidence 0.70.
- Q must not be reported as certain merely because the inference form is valid.

Exact confidence propagation belongs to Schema-v3 inference policy, not this seed package.

## Scope invariants

- All inference operates within compatible scope/context.
- A rule scoped to context A cannot silently apply to context B.
- Temporal or spatial qualification may make apparently identical propositions distinct.
- Attribution may make apparently identical propositions distinct.
- Formal equivalence never erases provenance.

## Machine-oriented seed registry

The runtime Foundation loader should encode these as typed data, not parse this Markdown. Suggested canonical entries:

```text
rule: modus_ponens
kind: deductive
origin: CORE
conditions: [P, implies(P,Q)]
conclusion: Q

rule: modus_tollens
kind: deductive
origin: CORE
conditions: [implies(P,Q), not(Q)]
conclusion: not(P)

rule: conjunction_elimination_left
kind: deductive
origin: CORE
conditions: [and(P,Q)]
conclusion: P

rule: conjunction_elimination_right
kind: deductive
origin: CORE
conditions: [and(P,Q)]
conclusion: Q

rule: disjunctive_syllogism_left
kind: deductive
origin: CORE
conditions: [or(P,Q), not(P)]
conclusion: Q
```

The exact serialized schema is intentionally deferred to Lantern PR #336's Foundation loader/Schema-v3 implementation contract so this repository does not invent a competing runtime format.

## Seed examples

### Example 1 — valid implication
Premises:
- If the lamp is powered, the indicator is on.
- The lamp is powered.

Expected:
- The indicator is on.

Reason:
- modus ponens.

### Example 2 — reject converse
Premises:
- If the lamp is powered, the indicator is on.
- The indicator is on.

Expected:
- Whether the lamp is powered is UNKNOWN.

Reason:
- affirming the consequent is invalid.

### Example 3 — modus tollens
Premises:
- If the lamp is powered, the indicator is on.
- The indicator is not on.

Expected:
- The lamp is not powered, assuming the implication applies in this scope.

### Example 4 — conjunction
Premises:
- The token is red.
- The token is round.

Expected:
- The token is red AND round.

### Example 5 — unknown is not false
Premise:
- The token is red.

Question:
- Is the token round?

Expected:
- UNKNOWN.

### Example 6 — conflict
Premises:
- The token is red.
- The token is not red.

Expected:
- CONFLICT.

Do not infer an unrelated proposition.

### Example 7 — disjunction
Premise:
- The key is in drawer A OR drawer B.
- The key is not in drawer A.

Expected:
- The key is in drawer B.

### Example 8 — scope
Premises:
- In environment E1, P -> Q.
- P is true in E2.

Expected:
- Q in E2 is UNKNOWN unless E1's rule is explicitly applicable to E2.

## Counterexample set

The package's validation suite must include at least:
- affirming consequent traps;
- denying antecedent traps;
- inclusive/exclusive OR traps;
- missing-premise cases;
- explicit contradiction;
- scope mismatch;
- attribution mismatch;
- temporal mismatch;
- irrelevant distractors;
- two-step valid implication;
- cyclic rules with bounded inference.

## Acceptance tests for Lantern

Once Schema-v3A exists, this package is considered runtime-validated only when Lantern can:

- [ ] apply modus ponens to novel proposition names;
- [ ] apply modus tollens;
- [ ] introduce/eliminate conjunction;
- [ ] perform disjunctive syllogism;
- [ ] chain compatible implications;
- [ ] reject affirming the consequent;
- [ ] reject denying the antecedent;
- [ ] distinguish UNKNOWN from FALSE;
- [ ] preserve CONFLICT without arbitrary explosion;
- [ ] refuse scope-incompatible inference;
- [ ] produce an inference receipt naming the formal rule and exact premises;
- [ ] remain within configured inference-depth/binding bounds.

## What Package 01 deliberately leaves to later seeds

- Predicate variables and quantifiers -> Package 02.
- Relation-specific transitivity/symmetry/inverses -> Package 03.
- Sets -> Package 04.
- Identity/equality/substitution -> Package 05.
- Rich epistemic confidence/evidence states -> Package 06 onward.
- Natural-language grammar for recognizing these structures -> Package 08.
- Probability/statistics -> later packages.
- Causal inference -> Package 14.

## Provenance

The formal rules in this package are inherited mathematical/logical structures, not discoveries made by Lantern. When used, inference receipts should identify `foundation.formal_logic@0.1.0-draft` (or its later accepted version) as the rule source.
