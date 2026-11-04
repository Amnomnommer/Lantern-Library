# Seed Package 08 — Evidence Types and Inference Validity

**Package ID:** `foundation.evidence_inference_validity`  
**Inheritance:** `CONCEPTUAL_CORE` / `CORE`  
**Version:** 0.1.0 candidate

## Purpose

Begin Wave 2 by teaching Lantern what different evidence actually establishes.

The package does **not** define one universal ranking such as "experiment > document > testimony." Evidence quality depends first on whether the evidence is relevant to the claim and whether the method can justify that kind of conclusion.

## Evidence types

Initial types include:
- direct observation;
- measurement;
- testimony;
- documentary evidence;
- experimental evidence;
- observational evidence;
- simulation evidence;
- inferential/derived evidence;
- negative evidence;
- anecdotal evidence;
- convergent evidence.

Later methodology packages add discipline-specific evidence standards.

## Evidence vs claim

An evidence record and the claim inferred from it remain separate.

Examples:

- Alice saying "the door is open" directly supports **Alice reported the door open**. Whether the door is actually open requires evaluating the testimony.
- A simulation directly establishes **the model produced result R under assumptions A**, not that R occurred in reality.
- An instrument reading establishes a measurement result; connecting that result to a target property requires measurement validity.

## Validity vs soundness

A formally valid inference can begin with false or unsupported premises. Lantern should therefore be able to say:

> "The conclusion follows if those premises are accepted, but the premises themselves are not established."

This keeps Schema-v3's reasoning receipts separate from factual authority.

## Independence

Five websites repeating one report are not five independent confirmations. Evidence chains retain provenance so Lantern can detect copied/cited ancestry.

Independent methods/sources that converge on the same claim can provide stronger evidence.

## Anecdotes

Anecdotes are not worthless. A case can:
- establish that something occurred in that case;
- reveal a possible mechanism;
- generate a hypothesis;
- provide a counterexample to a universal claim.

It generally cannot establish population frequency/prevalence by itself.

## Review checklist

- [ ] Evidence type is separate from quality.
- [ ] Relevance is checked before strength.
- [ ] Testimony/documentation preserves attribution.
- [ ] Measurement requires construct/instrument validity.
- [ ] Simulation cannot masquerade as direct observation.
- [ ] Formal validity does not imply factual soundness.
- [ ] Source copies do not count as independent replication.
- [ ] Anecdotes are neither discarded nor overgeneralized.
- [ ] Observational association does not automatically become causation.
- [ ] Derived evidence retains provenance chain.
