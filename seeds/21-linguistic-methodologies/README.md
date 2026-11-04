# Seed Package 21 — Linguistic Methodologies

**Package ID:** `foundation.linguistic_methodologies`  
**Inheritance:** `METHOD_CORE` / `CORE`  
**Version:** 0.1.0 candidate

## Purpose

Teach Lantern how humans investigate language—the primary medium through which Lantern currently encounters its owner, teachers and much of the world.

There is no single linguistic method. Different questions require different evidence.

## Levels of analysis

- phonetics;
- phonology;
- morphology;
- syntax;
- semantics;
- pragmatics/discourse.

Lantern should preserve distinctions among these rather than trying to solve every language problem as word association.

## Method families

### Formal/descriptive analysis
Identify structural patterns and constraints.

### Corpus linguistics
Study attested usage in systematically collected text/speech/sign corpora.

### Sociolinguistics
Study variation across speakers, groups, settings, identities, networks and power structures.

### Psycholinguistics
Experimentally/observationally study comprehension, production, acquisition and processing.

### Historical/comparative linguistics
Study language change and relationships across time.

### Field linguistics
Work with speakers/communities using elicitation and naturalistic evidence.

## Descriptive vs prescriptive

A style guide can legitimately say:

> use X in this institution/register.

That is different from:

> people who use Y have no grammar.

Nonstandard dialects have systematic grammars. Prestige is a social property, not evidence that one variety is inherently linguistically superior.

## Corpus limitations

A corpus is a sample of language use.

Rare in a corpus does not automatically mean impossible/ungrammatical, and frequent co-occurrence does not prove semantic identity.

This distinction is particularly important for Lantern's IdeaSpace/distributional systems.

## Speaker judgments

Acceptability judgments are useful evidence, but they are scoped to speakers, dialects, contexts and tasks. One person's judgment is not universal grammar.

## Semantics vs pragmatics

Literal/compositional meaning and contextual intended meaning can differ.

Lantern should be able to infer pragmatic interpretations while preserving that distinction rather than rewriting literal semantics to match every contextual use.

## Language change

Languages change. Change is not inherently corruption or decay.

Historical analysis should track chronology, community and semantic shift rather than treating modern usage as the timeless reference point.

## Annotation

Human linguistic annotations are evidence produced under guidelines/theories. They can be extremely useful training material without becoming unquestionable ground truth.

## Lantern relevance

This package should eventually help Lantern evaluate its own language failures:

```
phonological? (future speech)
morphological?
syntactic?
semantic?
reference/coreference?
pragmatic?
discourse continuity?
dialect/register mismatch?
```

That diagnostic structure can feed the Observatory/Gate-9 self-model.

## Review checklist

- [ ] Descriptive and prescriptive claims remain distinct.
- [ ] Dialects/registers are treated as systematic language.
- [ ] Corpus frequency does not become grammaticality or meaning automatically.
- [ ] Speaker judgments retain population/context scope.
- [ ] Semantics and pragmatics remain distinct.
- [ ] Distributional association is evidence, not semantic identity.
- [ ] Language change is not automatically decay.
- [ ] Translation is not perfect identity.
- [ ] Annotation is not unquestionable ground truth.
- [ ] Method choice follows the linguistic question.
