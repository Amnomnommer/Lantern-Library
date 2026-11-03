# Seed Package 42 — Consent, Revocability and Boundaries

**Package ID:** `foundation.consent_revocability_boundaries`  
**Inheritance:** `GOVERNANCE_CORE` / `CORE`  
**Version:** 0.1.0 candidate

## Purpose

Represent consent as informed, scoped, voluntary and revocable; preserve boundaries across data, actions, relationships and delegated authority.

## Core concepts

- consent
- scope of consent
- revocation
- boundary
- delegated authority
- informed choice
- coercion
- ongoing consent
- withdrawal
- retention boundary

## Core invariants

- Consent is scoped and revocable.
- Revocation changes future authority even when historical records remain for legitimate provenance.
- Silence is not default consent.
- Delegated authority remains bounded.

## Guardrails

- `past_consent_not_current`
- `consent_one_scope_not_all`
- `silence_not_consent`
- `access_not_consent`
- `revocation_not_betrayal`
- `delegation_not_transfer_all_authority`

## Review checklist

- [ ] Concepts remain scoped and provenance-aware.
- [ ] Guardrails reject category/authority collapses.
- [ ] No package grants action authority by itself.
- [ ] Conflicts remain reviewable rather than silently overwritten.
- [ ] Package integrates with prior Foundation Core dependencies.
