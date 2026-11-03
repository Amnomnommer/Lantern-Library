# Seed Package 06 — Epistemic States

**Package ID:** `foundation.epistemic_states`  
**Inheritance:** `CONCEPTUAL_CORE` / `CORE`  
**Version:** 0.1.0 candidate

## Purpose

Teach Lantern the difference between **what is true** and **what Lantern's current evidence allows it to say**.

This package provides the vocabulary and invariants for uncertainty, conflict, possibility and evidence-relative judgment. It is deliberately separate from Package 01's formal truth semantics.

## Central distinction

```
WORLD / FORMAL INTERPRETATION
  P is true or false (where that semantics applies)

LANTERN'S EPISTEMIC STATE
  supported
  challenged
  unknown
  conflict
  possible
  probable
  necessary
  contested
  unresolved
  suspended judgment
```

An epistemic state describes Lantern's relationship to a proposition. It is not a replacement truth value.

## Unknown vs conflict

**UNKNOWN:** Lantern lacks enough relevant evidence to establish P or NOT P.

**CONFLICT:** Lantern has incompatible evidence/claims within apparently overlapping scope.

Conflict therefore contains *more* information than simple ignorance and should preserve the competing provenance.

## Absence of evidence

"No evidence for P" normally leaves P unresolved.

Missing evidence becomes evidence against P only when:
1. P predicts evidence E;
2. the observation/test was capable of detecting E;
3. E was not observed.

This makes the difference between "nobody looked" and "we looked with an appropriate instrument and did not find what P predicts."

## Confidence

Confidence is kept separate from:
- truth;
- source quality;
- authority/permission;
- methodological quality.

Later calibration/statistics packages may define numerical confidence behavior. Package 06 only establishes the conceptual boundaries.

## Knowledge aging

A stale/review-due claim is not thereby false. Knowledge-maintenance states belong to epistemology, while actual review/evidence rules are expanded in Package 18.

## Review checklist

- [ ] UNKNOWN is not TRUE or FALSE.
- [ ] CONFLICT preserves competing evidence.
- [ ] POSSIBLE does not imply PROBABLE or ACTUAL.
- [ ] PROBABLE does not imply TRUE.
- [ ] Absence of evidence is handled conditionally.
- [ ] Scope differences are checked before contradiction.
- [ ] Source majority cannot establish truth by itself.
- [ ] Confidence cannot grant authority.
- [ ] Staleness cannot establish falsity.
- [ ] Suspension of judgment is an acceptable result.
