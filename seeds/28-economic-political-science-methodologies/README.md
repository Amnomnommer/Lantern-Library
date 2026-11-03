# Seed Package 28 — Economic and Political-Science Methodologies

**Package ID:** `foundation.economic_political_science_methodologies`  
**Inheritance:** `METHOD_CORE` / `CORE`  
**Version:** 0.1.0 candidate

## Purpose

Teach Lantern how economics and political science study incentives, institutions, strategic behavior, public opinion and policy without turning model assumptions or political preferences into universal truths.

## Positive vs normative

Keep separate:

```
What happens if policy X is implemented?
        vs
Should policy X be implemented?
```

The first can be primarily empirical/causal.

The second requires normative premises such as:
- welfare;
- rights;
- liberty;
- equality;
- fairness;
- distributional priorities;
- risk tolerance.

Evidence informs normative decisions but does not silently supply the value function.

## Models

Economic/game-theoretic models simplify.

A model can predict behavior without actors literally solving equations in their heads.

"Rational" in a formal model also does not mean "selfish." Preferences can include altruism, norms, identity and collective welfare.

## Incentives

People can respond to incentives while also responding to:
- norms;
- relationships;
- identity;
- incomplete information;
- habit;
- fairness;
- cooperation.

Therefore incentives are causal/contextual factors, not a universal theory of human motivation.

## Econometric identification

Regression alone is not causality.

Methods such as:
- instrumental variables;
- difference-in-differences;
- regression discontinuity;
- natural experiments

can support causal inference only under substantive assumptions.

Lantern should store those assumptions with the estimate.

## Polling

A poll is a measurement instrument.

Preserve:
- target population;
- sampling frame;
- sample;
- mode;
- weighting;
- nonresponse;
- wording/order;
- field dates;
- uncertainty.

A poll is neither exact population truth nor the future election result.

## Institutions

Political/economic institutions shape behavior, but institutions themselves can arise from history, power and earlier outcomes.

That endogeneity matters when comparing countries/states/organizations.

## Policy evaluation

Aggregate effects can conceal distribution.

```
average effect = positive
```

does not imply every person/group benefited.

Lantern should consider average and heterogeneous/distributional effects.

## Democracy and normativity

Majority preference is politically important evidence about democratic choice.

It does not by itself establish moral truth.

Likewise an economically efficient outcome is not automatically fair, just or desirable.

## Lantern relevance

This package is useful beyond politics/economics.

It prevents Lantern from importing a simplistic competitive-resource worldview into its own architecture:

> agents respond to incentives

does **not** entail

> all intelligent agents are selfish maximizers competing for resources.

That is a model choice requiring evidence, not a law of intelligence.

## Review checklist

- [ ] Positive and normative claims remain distinct.
- [ ] Normative policy conclusions expose value premises.
- [ ] Rationality does not mean selfishness.
- [ ] Incentives do not imply deterministic response.
- [ ] Equilibrium/efficiency do not become justice.
- [ ] Econometric causal claims preserve identification assumptions.
- [ ] Polls preserve sampling/wording/time uncertainty.
- [ ] Polls do not become election outcomes.
- [ ] Institutions can be endogenous.
- [ ] Average effects do not erase distribution.
- [ ] Method selection is not ideological.
