# Seed Package 19 — Statistical Methodology

**Package ID:** `foundation.statistical_methodology`  
**Inheritance:** `METHOD_CORE` / `CORE`  
**Version:** 0.1.0 candidate

## Purpose

Finish Wave 3 by teaching Lantern how to choose and interpret statistical analyses rather than merely knowing statistical vocabulary.

The sequence should be:

```
question / estimand
      ↓
study design
      ↓
variable types + dependence
      ↓
dataset quality / missingness
      ↓
candidate methods
      ↓
assumption checks
      ↓
deterministic calculation
      ↓
effect + uncertainty
      ↓
scientific interpretation
```

## Method families

The seed establishes selection concepts for:
- descriptive summaries;
- one-sample inference;
- two-sample inference;
- paired vs independent comparisons;
- proportions/counts/contingency structures;
- multiple groups;
- correlation;
- regression;
- nonparametric alternatives;
- effect sizes;
- confidence intervals;
- power/sample-size planning;
- multiple testing.

Exact tests and calculations belong to Lantern's deterministic quantitative organ.

## Sample size

Sample size influences:
- sampling uncertainty;
- power;
- precision.

It does **not** repair:
- selection bias;
- invalid measurement;
- confounding;
- dependence;
- poor operationalization.

Therefore Lantern should never derive "large dataset = trustworthy result."

## Significance

Keep separate:

```
statistical significance
effect size
uncertainty
practical significance
causal evidence
theory support
```

These answer different questions.

## P-values

A p-value is calculated assuming a null model. It is not the probability that the null hypothesis is true.

## Confidence intervals

For standard frequentist intervals, coverage refers to the procedure across repeated samples. Lantern should not automatically translate a realized 95% CI into "95% probability the fixed parameter is inside" unless using a framework that licenses that interpretation.

## Exploratory discovery

Hypotheses discovered by searching dataset D cannot be independently confirmed by testing them on the same D.

Use held-out or independent evidence where feasible.

This is especially important if future Lantern searches large knowledge/data stores for previously unnoticed relationships.

## Multiple testing

Searching many relationships creates false-discovery risk. The more Lantern explores, the more important explicit multiple-testing/discovery control becomes.

## Dataset adequacy

Before analysis Lantern asks whether:
- required variables exist;
- measurements are valid for the question;
- population/sample is appropriate;
- dependence is represented;
- missingness is assessed;
- design can support the desired inference.

## Review checklist

- [ ] Method selection starts from question/estimand/design.
- [ ] Paired and independent data remain distinct.
- [ ] Effect and uncertainty are interpreted together.
- [ ] Significance does not become importance or causality.
- [ ] P-values are interpreted correctly.
- [ ] Large N does not erase bias.
- [ ] Small N does not make data false.
- [ ] Nonparametric does not mean assumption-free.
- [ ] Regression/correlation do not automatically become causal.
- [ ] Exploratory data do not independently confirm their own discoveries.
- [ ] Multiple testing is explicit.
- [ ] Arithmetic is delegated to deterministic computation.
