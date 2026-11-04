# Seed Package 11 — Probability and Conditional Probability

**Package ID:** `foundation.probability_conditional`  
**Inheritance:** `FORMAL_CORE` / `CORE`  
**Version:** 0.1.0 candidate

## Purpose

Give Lantern the semantic foundations for probabilistic reasoning. The package teaches **what probability expressions mean and which transformations are valid**; deterministic numerical code should perform arithmetic whenever available.

## Critical distinction: inverse probability

```
P(evidence | hypothesis)
        !=
P(hypothesis | evidence)
```

A highly sensitive test does not imply that almost everyone who tests positive has the condition. The base rate and alternative explanations matter.

## Independence vs mutual exclusivity

Independent events do not affect each other's probability and may occur together.

Mutually exclusive events cannot occur together. Except for zero-probability edge cases, mutually exclusive events are therefore not independent.

## Probability 0 and 1

Within a mathematical model, events can receive probability 0 or 1. Lantern must not automatically turn those values into metaphysical impossibility or logical necessity outside that model.

## Expected value

Expected value is a distribution summary, not a prediction that the next observation equals that value. A fair six-sided die has expected value 3.5 even though 3.5 cannot appear on one roll.

## Empirical estimates

Package 11 defines probability semantics. It does not license population estimates from arbitrary samples. Sampling, uncertainty and statistical inference are expanded in Package 19 and the deterministic quantitative organ.

## Computational boundary

The seed library should not make Lantern approximate arithmetic through symbolic prose. Schema selects the applicable probability rule; deterministic computation evaluates the expression; Schema interprets the result.

## Review checklist

- [ ] Conditional direction is preserved.
- [ ] Base rates are required for Bayesian reversal.
- [ ] Independence and mutual exclusivity remain distinct.
- [ ] Probability is scoped to a model/sample space.
- [ ] Probability 0/1 does not automatically become metaphysical truth.
- [ ] Expected value is not treated as a guaranteed outcome.
- [ ] Sample rates do not automatically become population probabilities.
- [ ] Probability cannot grant authority.
