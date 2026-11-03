# Foundation Core Integration and Consistency Audit

Status: pre-implementation audit
Scope: Foundation Core 01-45 on branch `foundation/core-45-package-01`

## Executive finding

The 45-package curriculum is conceptually broad enough to proceed to implementation planning, but it is **not yet a single loader-ready schema**.

Packages 01-36 are comparatively rich machine-readable seeds. Packages 37-45 were intentionally authored as rapid design stubs and require normalization before activation.

The repository does not itself contain the current Lantern Schema v3/runtime implementation, so this audit maps **required runtime capabilities** rather than claiming those capabilities already exist.

## 1. Required Schema v3 / runtime capability map

### A. Typed knowledge objects
Required by: 06, 08-29, 35, 39-45.

Schema needs typed objects for at minimum:
- proposition/claim;
- observation/measurement;
- evidence;
- source/provenance;
- hypothesis;
- model;
- theory;
- law;
- prediction;
- preference/value;
- plan/task;
- incident/error;
- permission/consent;
- node/person/stakeholder.

Each object needs stable identity, type, provenance, timestamps/version, scope and status.

### B. Typed relations / graph
Required by: 02-05, 07, 09-10, 13-18, 20-45.

Needs directed typed edges such as:
- supports / challenges;
- caused_by / causes;
- depends_on;
- derived_from;
- supersedes;
- scoped_to;
- observed_by;
- contributed_by;
- authorized_by;
- consented_by;
- conflicts_with;
- predicts;
- explains;
- member_of / subset_of.

Relations need provenance and scope, not only subject-predicate-object strings.

### C. Epistemic state separate from content
Required by: 06, 08-19, 35, 44-45.

Need independent fields/objects for:
- true/false/unknown/conflict/possible;
- confidence;
- evidence strength;
- contested/retracted/superseded/stale;
- uncertainty source.

Do not encode these as mutually exclusive truth values.

### D. Scope/context
Required across nearly every package.

Need structured:
- temporal;
- spatial;
- population;
- domain;
- conditional;
- conversational/task scope.

Inference must preserve/intersect scope.

### E. Provenance / belief genealogy
Required by: 09-10, 18, 20, 25, 34-36, 44.

Need immutable or append-only lineage:
`source -> evidence -> inference -> claim -> revision/supersession`.

Retraction must not erase history.

### F. Rule and guard engine
Required by: 01-45.

Must distinguish:
- positive inference rules;
- forbidden inference/guard rules;
- invariants;
- method-selection rules;
- authority constraints.

Guards should block inference, not merely attach prose warnings.

### G. Dependency/package loader
Required by all packages.

Must:
- validate package schema/version;
- resolve dependency DAG;
- reject cycles;
- load in topological order;
- distinguish inheritance classes;
- preserve package provenance/version;
- run acceptance tests before activation;
- support package disable/rollback.

### H. Quantitative deterministic organ
Required by: 11-12, 16-19, 23, 25, 28, 32-33.

Needed for exact:
- arithmetic;
- probability/statistics;
- units/conversion;
- uncertainty propagation;
- graph/scheduling computations;
- scoring where explicitly licensed.

Seeds select/interpret methods; deterministic code executes them.

### I. Executive/problem/plan state
Required by: 30-38.

Need explicit runtime objects for:
- goals;
- constraints;
- subproblems;
- dependencies;
- plan status;
- decision alternatives;
- tool calls;
- incidents;
- confidence predictions;
- handoffs.

This is the Gate-3/agent substrate.

### J. Node/hive identity and permissions
Required by: 36-44.

Need:
- node identity;
- local vs shared state;
- contribution provenance;
- domain-scoped trust;
- privacy visibility;
- permission/authority scopes;
- consent/revocation;
- resource allocation without ownership-by-reward.

### K. Review/Sleep integration
Required by: 10, 18, 30, 34-36.

Sleep/review should be able to:
- consolidate incidents;
- evaluate prospective predictions;
- update calibration;
- flag stale knowledge;
- preserve belief genealogy;
- propose rules/tests;
- never silently mutate protected Core inheritance.

## 2. P0 structural inconsistencies

### P0.1 Dependency schema drift

Packages 01-36 use dependency objects:
```json
{"package_id":"foundation.x","minimum_version":"0.1.0"}
```

Packages 37-45 use bare package-id strings.

**Fix:** normalize 37-45 to dependency objects. Loader should support exactly one canonical representation.

### P0.2 Package maturity drift at 37-45

Packages 37-45 contain:
- concepts;
- guards;
- invariants;
- tests.

But they contain **zero positive inference rules**, unlike most earlier conceptual/agent packages.

Their tests use generic placeholder forms such as `TRIGGER(...)` / `INVALID_COLLAPSE(...)`, which test manifest wiring more than domain reasoning.

**Fix before activation:** expand 37-45 to the same rule/test quality bar as 01-36. They may remain authored/in-review, but should not be marked loader-ready yet.

### P0.3 Inheritance-class vocabulary expanded without declared loader contract

Observed classes now include:
- FORMAL_CORE;
- CONCEPTUAL_CORE;
- METHOD_CORE;
- AGENT_CORE;
- GOVERNANCE_CORE;
- SOCIAL_CORE;
- NORMATIVE_CORE.

**Fix:** Schema v3 must define allowed classes and mutation/activation semantics for each. Do not let unknown classes silently degrade to generic packages.

### P0.4 Repository layout duplication

Package 01 exists in both:
- `foundation/01-formal-logic`
- `seeds/01-formal-logic`

The remaining active curriculum is under `seeds/`.

**Fix:** declare `seeds/` canonical and archive/remove/redirect the old prototype location after verifying no loader depends on it.

## 3. Cross-package semantic collisions to normalize

These are mostly useful overlaps, but require canonical concept IDs or explicit aliases.

### confidence
Appears in epistemic states and metacognition.
- Canonical: epistemic confidence object.
- Metacognition should reference prospective/retrospective confidence records rather than redefine base confidence.

### trust / reliability
Appears in source provenance, hive trust calibration and social trust.
- Keep distinct namespaces:
  - source reliability;
  - node task reliability;
  - interpersonal/social trust.
- Do not collapse them to one scalar.

### authority / permission
Repeated in problem solving, planning, tools, hive, security, consent and ethics.
- Canonical governance objects should live in 39/42.
- Earlier packages should reference them once available.

### scope / boundary
Scope is epistemic/contextual in 07; boundary is also system/security/consent terminology later.
- Preserve typed boundary kinds rather than one generic `boundary`.

### dependency
Used for logical/package/task/software dependencies.
- Require typed dependency edges.

### state
Used for epistemic, software, plan and node state.
- Namespace/type state rather than one universal field.

### model
Scientific model, audience model, self-model, economic model, world model.
- `model` should be an abstract type with explicit subtype and target.

### evidence
Scientific evidence, diagnostic evidence, social evidence, performance evidence.
- Preserve evidence type/provenance; allow common evidence interface.

### consensus
Scientific consensus and hive consensus.
- Separate domain expert consensus from multi-node coordination consensus.

### fitness / utility / reward / value
Several packages intentionally distinguish these.
- Schema must not store all as one `score`.
- Reward remains learning/control signal.
- Utility is model-relative.
- biological fitness is reproductive concept.
- normative value is separate.

### ownership
Appears in economic pluralism, hive resources and governance.
- Shared compute allocation must not infer ownership from use/reward.

## 4. Cross-package guard interactions that are aligned

No direct conceptual contradiction was found in these high-risk areas; instead the packages reinforce one another:

- 06/09/18/35: confidence, source quality, freshness and calibration remain separate.
- 13/17/19: association/regression/temporality do not automatically become causation.
- 28/32/36/43: rationality/reward/resource allocation do not imply selfish competition or ownership.
- 30/31/33/39/42: capability, plan recommendation and tool access do not create authority.
- 34/35: failure and uncertainty can produce learning rather than forced certainty.
- 36/37/41/44: disagreement, perspective and trust do not require conformity.
- 26/28/45: descriptive claims do not silently become normative conclusions.

## 5. Potential semantic tensions requiring explicit precedence

### Formal contradiction vs empirical inconsistency
Package 01 disables unrestricted explosion for empirical reasoning while formal logic still recognizes contradiction.
- Runtime needs paraconsistent handling for empirical belief stores or a scoped rule-engine mode.
- Do not globally apply classical explosion to conflicting memories/evidence.

### Core immutability vs belief revision
Formal/Core inheritance is protected, while 10/18 require revision.
- Revision should change derived/empirical beliefs and package versions, not mutate accepted immutable package artifacts in place.

### Owner preference vs world truth
Owner preferences can govern owner-directed choices (32/41/42) but cannot become factual truth.
- Runtime needs separate `preference/authority` and `epistemic claim` channels.

### Consensus vs dissent
36/44 permit coordination consensus while preserving dissent.
- Shared memory must support a chosen operational decision plus unresolved minority claims.

### Privacy vs shared hive memory
36 encourages sharing; 39/42 constrain access/consent.
- Privacy/consent must gate hive propagation before merge into shared memory.

## 6. Recommended pre-coding normalization order

### P0
- [ ] Normalize dependency objects in 37-45.
- [ ] Define inheritance-class enum/semantics.
- [ ] Expand 37-45 with positive rules and domain acceptance cases.
- [ ] Declare `seeds/` canonical; resolve duplicate Package 01 path.
- [ ] Validate dependency DAG and missing package IDs.

### P1
- [ ] Define canonical typed IDs/aliases for confidence, trust, authority, scope, dependency, state, model, evidence, consensus and value/reward.
- [ ] Define rule-engine modes for formal vs empirical contradiction.
- [ ] Define immutable package artifact vs revisable belief distinction.
- [ ] Define privacy/consent gate before hive sharing.

### P2
- [ ] Map every package concept/rule to concrete Schema v3 fields/tables/classes.
- [ ] Build cross-package acceptance battery.
- [ ] Add loader rejection tests for malformed dependencies/classes/cycles.
- [ ] Add provenance checks for node/tool/source contributions.

## 7. Readiness judgment

**Conceptual curriculum:** READY for implementation planning.

**Single canonical package schema:** NOT YET READY.

**37-45 activation quality:** DESIGN-COMPLETE, NEEDS NORMALIZATION/EXPANSION.

**Schema v3 compatibility:** UNKNOWN until checked against the actual Lantern runtime repository.

The next audit should therefore inspect the Lantern codebase/Schema v3 directly and convert this requirements map into exact implementation gaps.
