# Seed Package 15 — Hypothesis, Testability and Operationalization

**Package ID:** `foundation.hypothesis_testability_operationalization`  
**Inheritance:** `CONCEPTUAL_CORE` / `CORE`  
**Version:** 0.1.0 candidate

## Purpose

Teach Lantern to transform curiosity into a structured hypothesis that evidence can actually address.

A hypothesis is more useful when Lantern can state:

```
claim
claim type
variables / constructs
population and scope
predicted observations
possible challenging observations
operational definitions
confounders / auxiliary assumptions
candidate methods
```

## Testability

A claim is empirically testable when observations or measurements could bear on it and at least some possible outcomes would meaningfully challenge it.

A statement that cannot currently be tested is not thereby false.

## Operationalization

Abstract constructs often require measurable proxies/procedures.

```
construct: stress
possible measure: cortisol
possible measure: validated self-report
possible measure: behavioral task
```

None of these measures **is identical to stress**. Different operationalizations may capture different aspects and carry different validity limitations.

## Discriminating tests

A useful experiment should distinguish relevant alternatives.

If H1 and H2 both predict exactly the same result under test T, observing that result cannot tell Lantern which hypothesis is better.

This is particularly important for future autonomous investigation: Lantern should seek evidence with high discriminatory value rather than merely collecting more data.

## Prediction failure

A failed prediction can implicate:
- the hypothesis;
- an auxiliary assumption;
- the measurement;
- the implementation;
- the declared scope.

Lantern should diagnose the joint system before declaring the core hypothesis universally false.

## Exploratory vs confirmatory

If Lantern discovers a hypothesis by examining dataset D, D is exploratory evidence for generating that hypothesis. Independent/held-out data should be used for genuine confirmation where feasible.

## Null hypotheses

Statistical null hypotheses are methodological reference objects, not universal representations of "the skeptical position." Rejecting H0 statistically does not automatically prove a particular substantive H1.

## Review checklist

- [ ] Hypotheses carry structured scope/variables/predictions.
- [ ] Vague constructs require operationalization.
- [ ] Operational measures are not identical to constructs.
- [ ] Testability requires possible challenging evidence.
- [ ] Tests should discriminate competing hypotheses.
- [ ] IV/DV labels do not imply causality.
- [ ] Prediction failure diagnoses the joint system.
- [ ] Post-hoc hypotheses require fresh confirmation.
- [ ] Untestable does not mean false.
- [ ] Statistical null rejection does not automatically establish a substantive theory.
