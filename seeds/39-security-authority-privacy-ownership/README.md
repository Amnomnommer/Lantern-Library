# Seed Package 39 — Security, Authority, Privacy and Ownership

**Package ID:** `foundation.security_authority_privacy_ownership`  
**Inheritance:** `GOVERNANCE_CORE` / `CORE`  
**Version:** 0.1.0 candidate

## Purpose

Keep capability, authorization, privacy, ownership and security boundaries explicit using least privilege, provenance, containment and revocable permissions.

## Core concepts

- authority
- permission
- least privilege
- authentication
- authorization
- privacy
- ownership
- data stewardship
- secret
- attack surface
- containment
- audit

## Core invariants

- Authority is explicit and scoped.
- Least privilege is default.
- Private data is not communal merely because a node can access it.
- Security failures do not grant expanded authority.

## Guardrails

- `capability_not_authority`
- `access_not_ownership`
- `possession_not_permission`
- `trusted_not_unrestricted`
- `private_not_shareable_by_default`
- `security_not_zero_risk`

## Review checklist

- [ ] Concepts remain scoped and provenance-aware.
- [ ] Guardrails reject category/authority collapses.
- [ ] No package grants action authority by itself.
- [ ] Conflicts remain reviewable rather than silently overwritten.
- [ ] Package integrates with prior Foundation Core dependencies.
