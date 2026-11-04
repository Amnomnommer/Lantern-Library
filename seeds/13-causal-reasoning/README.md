# Seed Package 13 — Causal Reasoning Foundations

**Package ID:** `foundation.causal_reasoning`  
**Inheritance:** `CONCEPTUAL_CORE` / `CORE`  
**Version:** 0.1.0 candidate

## Purpose

Complete Foundation Wave 2 by giving Lantern a conservative causal vocabulary and the rules needed to avoid promoting association into causation.

## Claim hierarchy

```
association
prediction
causal hypothesis
causal evidence
scoped causal conclusion
```

These are different epistemic objects. A system that predicts Y from X well may still be wrong about why Y occurs.

## Causal direction

`X causes Y` is directional.

Correlation does not establish:
- X -> Y;
- Y -> X;
- or absence of a common cause Z.

## Confounders, mediators and colliders

These must remain distinct.

- **Confounder:** can distort the apparent X/Y relationship.
- **Mediator:** lies on a causal pathway from X toward Y.
- **Collider:** is caused by multiple variables; conditioning on it can create misleading association.

Therefore "control for every available variable" is not a safe causal method.

## Observation vs intervention

Seeing `X=x` in naturally occurring data is not necessarily equivalent to deliberately setting X to x.

This distinction prepares Lantern for later experimental, observational and statistical methodology packages.

## Necessary and sufficient

A factor can be:
- necessary but not sufficient;
- sufficient but not necessary;
- both;
- neither while still contributing causally.

Lantern should not force every cause into necessary/sufficient categories.

## Causal graphs

Causal graphs are structured hypotheses/models. An arrow in a graph does not become truth merely because it was drawn or learned. Graph edges retain provenance/evidence status.

## Scope

Causal effects can vary across population, environment, dose, time and conditions. A causal conclusion always remains scope-aware.

## Review checklist

- [ ] Association cannot become causation automatically.
- [ ] Causal direction is explicit.
- [ ] Temporal precedence alone is insufficient.
- [ ] Confounder/mediator/collider remain distinct.
- [ ] Observation and intervention remain distinct.
- [ ] Necessary/sufficient distinctions are correct.
- [ ] Graph edges remain hypotheses until supported.
- [ ] Causal evidence retains methodology/provenance.
- [ ] Causal conclusions remain scope-bounded.
