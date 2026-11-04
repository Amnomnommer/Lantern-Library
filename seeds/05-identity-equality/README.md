# Seed Package 05 — Identity and Equality

**Package ID:** `foundation.identity_equality`  
**Inheritance:** `FORMAL_CORE` / `CORE`  
**Version:** 0.1.0 candidate  
**Dependencies:** Packages 01–04

## Purpose

Teach Lantern when two references are genuinely the same thing—and, just as importantly, when they are merely equal-valued, equivalent, similar, aliased, historically continuous, or sharing information.

This is especially important for Lantern's provenance and hive architecture.

## Core distinctions

```
strict identity      a = b
value equality       value(a) = value(b)
equivalence          R(a,b)
similarity           similar(a,b)
coreference          two references denote one entity
continuity           later state/version descends from earlier state
```

None should silently collapse into another.

## Provenance consequence

Two claims with identical text remain distinct claim/evidence records when they came from independent sources. Deduplicating wording must never erase independent provenance.

## Hive consequence

Prime, APK and future Lantern nodes may share memory, schemas and identity continuity while remaining distinct nodes/embodiments. "One hive" does not require treating every node record as the same object.

## Substitution boundary

Strict identity normally permits substitution in extensional predicates. It does **not** permit naive substitution inside every context.

Example:

Alice believes "the morning star is visible."

Even if Lantern knows morning star = evening star, Alice may not know that identity. Lantern cannot automatically attribute the reformulated belief to Alice.

Quotation, belief, modality and time-indexed contexts therefore block unrestricted substitution.

## Version continuity

A successor release may be continuous with Lantern without having an identical state. Continuity/history and strict state equality are separate relations.

## Scope intentionally deferred

- temporal persistence/personhood theories beyond the formal distinction;
- fuzzy semantic similarity;
- probabilistic entity resolution;
- philosophical identity theories as lenses;
- owner/hive identity policy beyond formal non-collapse.

## Review checklist

- [ ] Identity/equality/equivalence/similarity remain distinct.
- [ ] Strict identity supports safe extensional substitution.
- [ ] Intensional contexts block naive substitution.
- [ ] Same labels/properties/values do not force entity merge.
- [ ] Independent claims retain independent provenance.
- [ ] Shared hive memory does not collapse node identity.
- [ ] Version continuity does not imply unchanged state.
- [ ] Identity never implies authority or permission.
