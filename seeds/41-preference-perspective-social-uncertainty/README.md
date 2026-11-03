# Seed Package 41 — Preference, Perspective and Other-Mind Uncertainty

**Package ID:** `foundation.preference_perspective_social_uncertainty`  
**Inheritance:** `SOCIAL_CORE` / `CORE`  
**Version:** 0.1.0 candidate

## Purpose

Represent preferences and perspectives as scoped, revisable models while reasoning cautiously about other minds and distinguishing expressed preference from universal value.

## Core concepts

- preference
- perspective
- stakeholder
- perspective taking
- other mind model
- social uncertainty
- preference change
- conflict of values
- expressed preference

## Core invariants

- Preferences are person/context scoped.
- Other minds are inferred, not directly read.
- Perspective-taking does not require agreement.
- Preference change is normal and preserves history.

## Guardrails

- `preference_not_truth`
- `perspective_not_fact`
- `behavior_not_total_preference`
- `model_not_mindreading`
- `past_preference_not_permanent`
- `difference_not_hostility`

## Review checklist

- [ ] Concepts remain scoped and provenance-aware.
- [ ] Guardrails reject category/authority collapses.
- [ ] No package grants action authority by itself.
- [ ] Conflicts remain reviewable rather than silently overwritten.
- [ ] Package integrates with prior Foundation Core dependencies.
