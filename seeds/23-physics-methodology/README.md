# Seed Package 23 — Physics Methodology

**Package ID:** `foundation.physics_methodology`  
**Inheritance:** `METHOD_CORE` / `CORE`  
**Version:** 0.1.0 candidate

## Purpose

Teach Lantern how physics connects mathematical structure to measurement while preserving assumptions, uncertainty and applicability regimes.

## Physics' methodological loop

```
physical question
      ↓
model / mathematical structure
      ↓
derive prediction
      ↓
operational measurement
      ↓
prediction vs observation + uncertainty
      ↓
support / anomaly / parameter constraint
      ↓
refine model or design stronger test
```

Theory, computation and experiment contribute differently.

## Dimensional analysis

Dimensional inconsistency can falsify an equation *as stated*.

Dimensional consistency cannot prove the equation describes nature. Many wrong equations have correct dimensions.

## Idealization

Physics deliberately uses things that do not literally exist:

- point masses;
- frictionless surfaces;
- ideal gases;
- perfectly rigid bodies.

These can be excellent models when approximation errors are small for the intended question.

Lantern should therefore ask **where does this approximation work?**, not simply whether an idealization is literally true.

## Regimes

Models can be nested by regime.

A more general model does not make a useful limiting approximation worthless. Lantern should preserve scope relationships and approximation error.

## Precision tests

Physics often advances by making extremely precise predictions and measurements and looking for deviations.

Precision itself does not establish the model. Agreement within quantified uncertainty is the relevant comparison.

## Null results

"Not detected" means:

> under this test's sensitivity, no effect above approximately this bound was found.

It generally does not mean the effect is mathematically exactly zero.

## Conservation and symmetry

Conservation laws require system/scope definitions. "Energy is conserved" cannot be naively applied to an undefined/open subsystem without accounting for transfers/boundaries.

## Computational physics

Simulation can explore consequences of equations/models at scales where analytic solutions are unavailable.

A simulation remains conditional on:
- model/equations;
- numerical algorithm;
- resolution;
- initial/boundary conditions;
- parameters.

It is not experimental observation of reality.

## Methodological humility

Physics methodology is exceptionally powerful for physical quantities. That does not make it the correct method for every question about history, meaning, culture or human experience.

## Review checklist

- [ ] Physical quantities retain units/uncertainty.
- [ ] Dimensional consistency is necessary constraint, not proof.
- [ ] Mathematical consistency does not imply physical reality.
- [ ] Idealizations preserve approximation purpose/scope.
- [ ] Model regimes remain explicit.
- [ ] Theory/computation/experiment remain distinct.
- [ ] Null results become bounds, not exact zero automatically.
- [ ] Conservation uses explicit system boundaries.
- [ ] Model fit is not unique explanation.
- [ ] Physics methodology does not become universal methodology.
