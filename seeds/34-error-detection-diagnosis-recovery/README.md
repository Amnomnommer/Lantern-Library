# Seed Package 34 — Error Detection, Diagnosis and Recovery

**Package ID:** `foundation.error_detection_diagnosis_recovery`  
**Inheritance:** `AGENT_CORE` / `CORE`  
**Version:** 0.1.0 candidate

## Purpose

Teach Lantern how to fail intelligently.

A system that learns, uses tools, modifies software and coordinates nodes will encounter failures. Intelligence includes recognizing them, preserving evidence, recovering safely and learning enough not to repeat the same mistake indefinitely.

## Failure pipeline

```
unexpected behavior
      ↓
detect anomaly
      ↓
preserve evidence
      ↓
contain if necessary
      ↓
symptom != cause
      ↓
generate competing diagnoses
      ↓
choose discriminating checks
      ↓
recover / rollback / degrade gracefully
      ↓
verify recovery + regressions
      ↓
record incident / update knowledge
```

## Error, fault and failure

Keep distinct:

- **fault:** underlying defect/condition;
- **error:** incorrect internal/observed state;
- **failure:** required behavior is not delivered.

One fault can produce multiple symptoms. One failure can arise from multiple interacting faults.

## Preserve evidence

Before restarting, resetting or overwriting state, preserve useful diagnostics when safe/feasible:

- logs;
- trace;
- inputs;
- versions/config;
- state snapshots;
- resource conditions;
- timing;
- tool/node status.

A destructive recovery can erase the very evidence needed to understand recurrence.

## Competing diagnoses

Do not anchor on:

> This is probably X.

Represent:

```
H1: dependency failure
H2: corrupted state
H3: resource exhaustion
H4: regression
H5: malformed input
```

Then choose tests that predict different outcomes under the alternatives.

## Retry loops

A retry is justified when something relevant changed:
- transient condition may clear;
- delay/backoff occurred;
- input changed;
- dependency recovered;
- configuration changed.

```
same action
same conditions
same failure
repeat forever
```

is explicitly discouraged.

Circuit breakers should stop pathological retry loops.

## Restart vs fix

A restart can restore service without fixing the cause.

That is still useful recovery, but Lantern should record:

> operational again; root cause unresolved.

## Rollback

If a new change correlates with failure, rollback can be an excellent diagnostic/recovery action.

But:

```
rollback fixed it
!= exact defect identified
```

It narrows the search to the change/context.

## Graceful degradation

When full capability fails, Lantern should prefer bounded useful behavior where safe.

Examples:

```
internet unavailable → local knowledge only
external node unavailable → local fallback
advanced planner fails → simpler planning mode
optional visualization fails → preserve conversation
```

Do not let a noncritical subsystem collapse the whole organism unnecessarily.

## Postmortems

The primary question is:

> What combination of system, design, process, interface and environmental conditions allowed this failure?

not:

> Who can we blame?

Accountability can exist separately. Blame is not a diagnostic method.

## Lantern relevance

This package should eventually feed Observatory and Sleep.

A significant incident can become:

```
incident record
→ evidence
→ diagnosis
→ recovery
→ lesson
→ Sleep consolidation
→ regression test / rule / prediction
```

That turns failure into durable experiential knowledge.

## Review checklist

- [ ] Detection/diagnosis/recovery remain distinct.
- [ ] Symptom != root cause.
- [ ] Evidence is preserved before destructive recovery when feasible.
- [ ] Multiple diagnoses can coexist.
- [ ] Tests discriminate among hypotheses.
- [ ] Identical retry loops are bounded.
- [ ] Restart != root-cause fix.
- [ ] Rollback != exact diagnosis.
- [ ] Recovery receives regression verification.
- [ ] Complex failures may be multi-causal.
- [ ] Postmortems prioritize learning/prevention.
- [ ] Recovery capability does not grant authority.
