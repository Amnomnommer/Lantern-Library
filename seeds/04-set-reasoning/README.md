# Seed Package 04 — Set Reasoning

**Package ID:** `foundation.set_reasoning`  
**Inheritance:** `FORMAL_CORE` / `CORE`  
**Version:** 0.1.0 candidate  
**Dependencies:** Packages 01–03

## Purpose

Give Lantern a compact formal model of sets and set operations. This package is especially important for category reasoning because membership and subset relationships are easy to collapse into the same vague notion of "belongs to."

## Central distinctions

### Membership is not subset

`sparrow IN birds` relates an object to a set/category.

`sparrows SUBSET_OF birds` relates one set to another.

Neither relation may be substituted for the other.

### Subset does not reverse membership

If birds are animals and a cat is an animal, that does not make the cat a bird.

### Overlap is not containment

Two sets sharing members does not establish that either contains all members of the other.

### Empty is not unknown

`EMPTY(A)` is a positive formal statement that A has no members. It must not be represented as "we don't know what is in A."

### Complement is scoped

There is no useful unbounded complement in Lantern's operational reasoning. `COMPLEMENT(A,U)` always names the universe U against which complement is evaluated.

## Cardinality

Package 04 introduces finite cardinality as a concept sufficient for later quantitative packages, but does not attempt infinite-cardinal arithmetic. Equal cardinality does not establish set equality.

## Relationship to Schema

Set relations should use the same typed relation/rule machinery as Schema-v3A. Do not create a separate "set engine" unless profiling demonstrates a compelling need. Efficient indexes/bitsets may later optimize execution without changing semantics.

## Scope intentionally deferred

- numerical probability over sets/events -> Package 11;
- empirical categories and taxonomies -> later knowledge packages;
- fuzzy membership -> future semantic/category work;
- infinite set theory -> not required for Foundation Core;
- database collection semantics -> implementation detail, not formal seed knowledge.

## Review checklist

- [ ] Membership and subset cannot be conflated.
- [ ] Subset transitivity works.
- [ ] Proper subset requires non-equality.
- [ ] Union/intersection/difference semantics are correct.
- [ ] Disjointness does not imply exhaustiveness.
- [ ] Empty set remains distinct from unknown membership.
- [ ] Complement requires explicit universe.
- [ ] Equal cardinality does not imply equality.
- [ ] No formal set derivation grants empirical authority.
