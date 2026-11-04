# Seed Package 17 — Observational Reasoning

**Package ID:** `foundation.observational_reasoning`  
**Inheritance:** `METHOD_CORE` / `CORE`  
**Version:** 0.1.0 candidate

## Purpose

Teach Lantern how to reason from data that humans did **not** experimentally assign.

Observational methodology is not "bad experimentation." Many questions cannot ethically, practically or conceptually be randomized.

## Major designs

### Cross-sectional
Variables observed in the same time window. Useful for prevalence and concurrent association; often weak for determining temporal direction.

### Cohort
Groups defined by exposure/characteristics are followed or reconstructed to compare outcomes.

### Case-control
Cases with an outcome and controls without it are selected, then earlier exposures are compared. The sampled case fraction normally does not estimate population prevalence.

### Longitudinal/panel
The same units are measured over time. This supports change/temporal analysis but does not remove confounding automatically.

### Natural/quasi-experiments
External rules/events/processes create structured exposure differences. These can support causal inference when their identification assumptions are defensible.

## Bias structures

Lantern should explicitly consider:
- selection bias;
- loss to follow-up;
- missing-data mechanisms;
- confounding;
- reverse causation;
- measurement bias.

A million biased observations can estimate the wrong quantity extremely precisely.

## Adjustment

Statistical adjustment is not magic.

Controlling observed covariates does not prove that unmeasured confounding is absent.

Propensity scores/matching can improve comparability on observed covariates under assumptions; they do not turn observational data into literal randomized trials.

## Temporality

Exposure preceding outcome is useful causal evidence, but temporal precedence alone is not sufficient for causation.

## Identification

Any observational causal conclusion should preserve:
- the identification strategy;
- causal assumptions;
- adjustment variables;
- diagnostics;
- scope/population.

This lets Lantern later distinguish "the data show an association" from "under assumptions A/B/C, this design estimates a causal effect."

## Review checklist

- [ ] Observational designs are treated as first-class methods.
- [ ] Cross-sectional data do not manufacture temporal direction.
- [ ] Longitudinal data do not automatically establish causation.
- [ ] Case-control sampling is interpreted correctly.
- [ ] Selection/attrition/missingness remain visible.
- [ ] Adjustment cannot guarantee no unmeasured confounding.
- [ ] Propensity methods do not become randomization.
- [ ] Natural experiments retain identification assumptions.
- [ ] Large N does not erase systematic bias.
- [ ] Observational causal claims preserve methodology/provenance.
