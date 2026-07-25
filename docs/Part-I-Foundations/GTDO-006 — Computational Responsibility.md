# GTDO-006 — Computational Responsibility

## The Missing Organizational Layer Between Training Data and Computational Units

---

## Abstract

Goal-Oriented Training Data Organization introduces **Computational Responsibility** as a first-class concept.

A training group is not yet a computational capability.

A model, function, agent, database, controller, or human expert is not meaningful merely because it exists.

What connects organized evidence to organized computation is responsibility.

Computational Responsibility defines:

* what work must be performed;
* which conditions activate that work;
* which outputs or transformations are expected;
* which computational structure should own the work;
* how the result should be validated;
* which fallback should apply;
* how the responsibility may be updated, shared, split, merged, or retired.

The central GTDO relation is:

```text
Training Evidence
        ↓
Goal-Oriented Organization
        ↓
Computational Responsibility
        ↓
Computational Unit
        ↓
Dispatch and Call Path
```

This article defines Computational Responsibility, distinguishes it from labels, topics, tasks, capabilities, and implementation mechanisms, and explains why it is the missing middle layer required for controllable AI Computation Organization.

---

#### Fig-101-GTDO-Structural-Overview.png

![Fig-101-GTDO-Structural-Overview.png](../figures/Fig-101-GTDO-Structural-Overview.png)

---

# 1. Why Responsibility Must Be Explicit

Many AI systems contain powerful computational structures.

These structures may include:

* large language models;
* specialized neural networks;
* retrieval systems;
* symbolic reasoners;
* software functions;
* planners;
* controllers;
* agents;
* human reviewers.

However, simply possessing these structures does not create an organized system.

The system must also know:

* what each structure is responsible for;
* when that responsibility begins;
* where it ends;
* how responsibilities overlap;
* which unit acts when confidence is low;
* how failures are detected;
* who validates the result;
* which path should be optimized after an error.

Without explicit responsibility, computation remains available but weakly organized.

GTDO therefore treats responsibility as an architectural object.

---

# 2. Canonical Definition

Within GTDO:

> **Computational Responsibility is the bounded task, capability, transformation, recognition role, validation duty, control function, or coordination obligation assigned to a computational structure according to a Goal Function.**

A responsibility should define at least:

```text
What must be done?

Under which conditions?

Using which evidence?

By which computational structure?

With which expected result?

Under which validation rule?

With which fallback?
```

A responsibility is not merely a label attached to a unit.

It is a control contract connecting goals, data, computation, validation, and evolution.

---

# 3. The Missing Middle Layer

A conventional pipeline may appear as:

```text
Training Data
        ↓
Model
```

GTDO inserts a necessary middle layer:

```text
Training Data
        ↓
Goal-Oriented Group
        ↓
Computational Responsibility
        ↓
Implementation
        ↓
Computational Unit
```

This layer is necessary because a group does not determine its own implementation.

For example, one training group may support:

* a separate model;
* an adapter;
* a retrieval collection;
* a symbolic rule;
* a software function;
* a human review process.

The responsibility remains conceptually stable even when the implementation changes.

---

# 4. Responsibility Is Not a Topic

A topic describes subject matter.

A responsibility describes computational work.

Example topic:

```text
Medicine
```

Possible responsibilities within that topic include:

* retrieve clinical evidence;
* summarize a medical record;
* identify a possible contradiction;
* classify a document;
* produce a patient-facing explanation;
* request human review;
* enforce a safety boundary.

One topic may contain many responsibilities.

One responsibility may also span many topics.

For example:

```text
Formal Validation
```

may apply to:

* medicine;
* finance;
* physics;
* engineering;
* law.

Therefore:

```text
Topic
    ≠
Computational Responsibility
```

---

# 5. Responsibility Is Not a Class Label

A class label may identify what an input is.

A responsibility identifies what computation should occur.

Example:

```text
Class:
Compiler Error
```

Possible responsibilities include:

* explain the error;
* locate the responsible code;
* retrieve known defects;
* test a compiler version;
* suggest a repair;
* determine release risk.

The class may support dispatch, but it does not fully define computation.

A class answers:

> What is this?

A responsibility answers:

> What must be done about it?

---

# 6. Responsibility Is Not Merely a Task Name

A task name may be broad or underspecified.

Example:

```text
Analyze Document
```

This may hide several responsibilities:

* extract facts;
* detect inconsistency;
* compare against policy;
* generate summary;
* classify risk;
* escalate uncertain cases.

A Computational Responsibility should be bounded enough to support:

* assignment;
* validation;
* dispatch;
* ownership;
* local improvement.

The more ambiguous the responsibility, the weaker the control architecture.

---

# 7. Responsibility Is Not the Same as Capability

Capability means that a unit can perform some work.

Responsibility means that the system expects the unit to perform that work under defined conditions.

A general LLM may be capable of translation, coding, summarization, and explanation.

But a GTDO architecture may assign it responsibility only for:

```text
General-Language Fallback
```

A specialized translator may hold the primary translation responsibility.

Thus:

```text
Capability
    =
What a unit can do

Responsibility
    =
What the system assigns it to do
```

This distinction is essential for control.

---

# 8. Responsibility Is Not the Same as Implementation

A responsibility may survive an implementation change.

Example:

```text
Validation Responsibility
```

Version 1 implementation:

```text
LLM Validator
```

Version 2 implementation:

```text
Symbolic Validator
```

Version 3 implementation:

```text
Symbolic Validator
+
Human Review
```

The responsibility remains stable while the implementation evolves.

This separation supports:

* replacement;
* migration;
* certification;
* local testing;
* rollback.

---

# 9. Responsibility Is Not the Same as a Computational Unit

A Computational Unit is an implementation artifact.

A Computational Responsibility is an organizational role.

Possible relationships include:

```text
One Responsibility
    →
One Unit
```

```text
One Responsibility
    →
Multiple Cooperative Units
```

```text
Multiple Responsibilities
    →
One Shared Unit
```

```text
One Responsibility
    →
Human–AI Call Path
```

Therefore, responsibility and unit must not be treated as one-to-one by default.

---

# 10. The Core Responsibility Contract

A practical Computational Responsibility should define a contract.

## Responsibility Name

A stable identifier.

## Purpose

Why the responsibility exists.

## Activation Conditions

When the responsibility applies.

## Input Scope

Which data, contexts, tasks, or states are accepted.

## Output Obligation

What result must be produced.

## Computational Owner

Which unit, path, or organization performs the work.

## Confidence Conditions

When the owner may act directly.

## Boundary Policy

What happens when evidence is ambiguous.

## Validation Rule

How success is measured.

## Fallback Policy

What happens after uncertainty or failure.

## Version

Which responsibility definition is active.

This contract makes responsibility inspectable and enforceable.

---

# 11. Responsibility Emerges from Goal-Oriented Organization

A responsibility should arise from an explicit Goal Function.

The progression is:

```text
Goal Function
        ↓
Meaningful Distinction
        ↓
Training Group
        ↓
Responsibility Candidate
        ↓
Validated Responsibility
```

A group becomes a Responsibility Candidate when its structure suggests a distinct computational role.

It becomes a formal responsibility only after the role is:

* understandable;
* useful;
* stable enough;
* implementable;
* verifiable.

---

# 12. Responsibility Candidates

Not every detected group deserves a permanent responsibility.

A Responsibility Candidate may be rejected when:

* separation is weak;
* the group is too small;
* the computational benefit is unclear;
* the role duplicates an existing responsibility;
* the required unit is too expensive;
* fallback already handles the cases well;
* local specialization damages general capability.

Possible outcomes include:

```text
Promote to Responsibility

Merge with Existing Responsibility

Retain as Boundary Set

Defer

Discard

No Split
```

GTDO therefore separates structural discovery from architectural commitment.

---

# 13. Responsibility Boundaries

Every responsibility should have a boundary.

A Responsibility Boundary defines:

* which cases belong;
* which cases do not;
* which cases are ambiguous;
* which neighboring responsibilities overlap;
* when fallback is required.

A boundary may be:

* semantic;
* structural;
* temporal;
* contextual;
* operational;
* risk-based;
* confidence-based.

Clear boundaries support local control.

Unclear boundaries produce dispatch instability and duplicated computation.

---

# 14. Hard and Soft Responsibility Boundaries

## Hard Boundary

A strict rule.

Example:

```text
Only certified symbolic proofs may be accepted.
```

## Soft Boundary

A preference controlled by confidence or context.

Example:

```text
Use specialist when confidence is high;
otherwise use general fallback.
```

GTDO should represent both kinds explicitly.

---

# 15. Responsibility Ownership

Responsibility ownership identifies the computational structure accountable for performing or coordinating the work.

Possible owners include:

* one model;
* one Brain Unit;
* one function;
* one agent;
* one team of units;
* one human expert;
* one Call Path;
* one hybrid organization.

Ownership does not necessarily imply exclusivity.

A responsibility may have:

* primary owner;
* secondary owner;
* validator;
* fallback owner;
* escalation owner.

---

# 16. Primary and Secondary Responsibility

## Primary Responsibility

The preferred computational owner under normal conditions.

## Secondary Responsibility

An alternative owner used when:

* the primary unit is unavailable;
* confidence is low;
* validation fails;
* cost or latency conditions change;
* multi-path processing is required.

This structure increases resilience.

---

# 17. Shared Responsibility

A responsibility may be shared across units.

Example:

```text
High-Risk Decision
├── Retrieval Unit
├── Reasoning Unit
├── Validation Unit
└── Human Reviewer
```

The responsibility belongs to the Call Path rather than one node.

Shared responsibility requires explicit coordination.

Otherwise, failures may be attributed incorrectly.

---

# 18. Composite Responsibility

A Composite Responsibility contains several ordered sub-responsibilities.

Example:

```text
Produce Verified Answer
        ↓
Retrieve Evidence
        ↓
Generate Candidate
        ↓
Validate Candidate
        ↓
Compose Final Output
```

A Composite Responsibility naturally maps to a Call Path.

The full path owns the overall result.

Individual units own local obligations.

---

# 19. Hierarchical Responsibility

Responsibilities may be hierarchical.

Example:

```text
Engineering Responsibility
    ↓
Software Responsibility
    ↓
Compiler Responsibility
    ↓
Optimization Responsibility
```

Each level narrows the scope.

This hierarchy can generate a Dispatch Tree.

At runtime, the selected hierarchy becomes a Call Path.

---

# 20. Responsibility Decomposition

Responsibility Decomposition divides a broad obligation into smaller obligations.

Example:

```text
Analyze Code
```

may decompose into:

```text
Parse Code
Detect Defect
Explain Defect
Recommend Repair
Validate Repair
```

Decomposition is useful when sub-responsibilities require:

* different data;
* different units;
* different validation;
* different risk controls;
* independent optimization.

However, decomposition should not be performed without sufficient benefit.

---

# 21. Responsibility Composition

Separate responsibilities may be combined into a larger capability.

Example:

```text
Retrieval
+
Reasoning
+
Validation
        ↓
Evidence-Grounded Decision
```

Composition supports Hybrid AI.

It also prevents the mistaken belief that specialization must produce isolated units.

---

# 22. Responsibility Split

A responsibility may need to split when:

* the task range becomes too broad;
* performance differs across subdomains;
* one subgroup requires different validation;
* one subgroup has different risk;
* Boundary Sets become persistent;
* local optimization is repeatedly needed.

Split should produce distinct and meaningful obligations.

---

# 23. Responsibility Merge

Responsibilities may need to merge when:

* boundaries are unstable;
* capabilities overlap heavily;
* units duplicate work;
* routing cost is excessive;
* separate groups are too small;
* one shared unit performs better.

Merge preserves Operator Economy.

---

# 24. Responsibility Promotion

A Boundary Set or recurring task pattern may be promoted to a formal responsibility.

Promotion requires evidence such as:

* sufficient sample volume;
* stable structure;
* repeated runtime demand;
* clear validation criteria;
* meaningful performance gain;
* justified implementation cost.

The transition is:

```text
Boundary Set
        ↓
Responsibility Candidate
        ↓
Validated Responsibility
        ↓
Computational Unit or Call Path
```

---

# 25. Responsibility Retirement

A responsibility may be retired when:

* it is obsolete;
* another responsibility subsumes it;
* its unit is no longer used;
* its data no longer reflects current goals;
* its cost exceeds its value;
* its function is replaced.

Retirement should preserve:

* history;
* version references;
* fallback;
* migration records;
* dependent-path updates.

---

# 26. Responsibility Versioning

Responsibilities themselves should be versioned.

A change in definition can be as consequential as a model update.

Versioned fields may include:

* scope;
* Goal Function;
* activation conditions;
* owner;
* validation rule;
* fallback;
* risk constraints.

Example:

```text
Compiler Optimization Responsibility v1.2
```

This supports traceability between organizational change and performance change.

---

# 27. Responsibility Invariants

A responsibility may preserve invariants during implementation change.

Examples include:

* required output type;
* safety constraint;
* validation obligation;
* fallback availability;
* latency limit;
* provenance requirement.

An implementation is acceptable only if these invariants remain satisfied.

---

# 28. Responsibility and Dispatch

Dispatch answers:

> Which responsibility applies, and which structure should own it now?

The general relation is:

```text
Input
+
Context
+
Goal
+
Runtime State
        ↓
Responsibility Selection
        ↓
Owner Selection
        ↓
Call Path
```

Responsibility selection should conceptually precede unit selection.

Otherwise, dispatch may become shallow routing without organizational meaning.

---

# 29. Responsibility-First Dispatch

A responsibility-first dispatch process is:

```text
Step 1:
Identify required computation

Step 2:
Identify responsible role

Step 3:
Select an implementation

Step 4:
Construct or activate the Call Path
```

This differs from unit-first routing:

```text
Which model appears most likely?
```

Responsibility-first dispatch is more stable when implementations change.

---

# 30. Responsibility and Context

The same input may activate different responsibilities under different contexts.

Example:

```text
Input:
"Check this result."
```

Possible contexts:

```text
Mathematics Context
    → Formal Validation Responsibility

Medical Context
    → Safety Review Responsibility

Software Context
    → Test Verification Responsibility
```

Therefore:

```text
Input Alone
    ≠
Complete Responsibility
```

Context is part of responsibility selection.

---

# 31. Responsibility and Confidence

A unit may hold responsibility only above a confidence threshold.

Example:

```text
High Confidence
    → Specialist acts directly

Medium Confidence
    → Specialist + Validator

Low Confidence
    → General Fallback or Human Review
```

Confidence changes the responsibility path.

It should not necessarily change the conceptual responsibility itself.

---

# 32. Responsibility and Boundary Sets

Boundary Sets often indicate unresolved responsibility.

A Boundary Set may contain cases where:

* two responsibilities compete;
* no responsibility exists;
* the input belongs to a composite responsibility;
* more context is required;
* a new responsibility is emerging.

Boundary resolution is therefore partly responsibility resolution.

---

# 33. Boundary Responsibility

Some systems should define an explicit Boundary Responsibility.

Its purpose may be to:

* gather more context;
* invoke multiple units;
* compare candidate outputs;
* escalate to a human;
* defer action;
* create a new training record.

A Boundary Responsibility transforms uncertainty into controlled computation.

---

# 34. Fallback Responsibility

Fallback is itself a responsibility.

A general model does not become a fallback merely because it is available.

Its responsibility should specify:

* which cases it accepts;
* which specialist failures trigger it;
* what confidence it may claim;
* whether human review follows;
* how outcomes feed back into GTDO.

Fallback should be explicit, measurable, and versioned.

---

# 35. Validation Responsibility

Validation should be assigned as a responsibility rather than assumed to happen implicitly.

Possible validation responsibilities include:

* factual validation;
* structural validation;
* formal proof checking;
* policy compliance;
* safety review;
* cross-model comparison;
* human approval.

A validation unit may be independent from the unit producing the candidate output.

---

# 36. Coordination Responsibility

A Hybrid AI system requires units that coordinate other units.

Coordination responsibilities may include:

* dispatch;
* sequencing;
* resource selection;
* conflict resolution;
* output fusion;
* fallback activation;
* version compatibility checks.

The dispatcher is therefore not merely a router.

It owns a coordination responsibility.

---

# 37. Computational Responsibility Graph

Responsibilities can be represented as a graph before executable units are chosen.

Possible nodes:

```text
Retrieve Evidence

Generate Candidate

Validate Candidate

Approve Action

Handle Boundary
```

Possible edges:

* dependency;
* sequence;
* fallback;
* validation;
* shared ownership;
* conflict;
* escalation.

This Computational Responsibility Graph is a logical architecture.

It can later be mapped to a Dispatch Graph or Calling Graph.

---

# 38. Responsibility Graph versus Dispatch Graph

A Responsibility Graph describes what roles exist and how they relate.

A Dispatch Graph describes how concrete computational structures are selected and connected.

```text
Responsibility Graph
        ↓
Implementation Mapping
        ↓
Dispatch Graph
```

Keeping these levels separate supports implementation flexibility.

---

# 39. Responsibility Graph versus Calling Graph

A Calling Graph describes execution calls.

A Responsibility Graph describes organizational obligations.

One responsibility may require several calls.

One call may support several responsibilities.

The relationship is:

```text
Responsibility
    defines why computation exists.

Calling Graph
    defines how computation executes.
```

---

# 40. Responsibility and Call Paths

A Call Path is an executable realization of one or more responsibilities.

Example:

```text
Responsibility:
Produce Verified Technical Answer
```

Call Path:

```text
Retrieval Unit
    ↓
Domain Brain Unit
    ↓
Symbolic Validator
    ↓
Language Generator
```

The responsibility defines the obligation.

The Call Path defines the execution structure.

---

# 41. Responsibility Attribution

When an outcome is poor, the system should determine which responsibility or sub-responsibility failed.

Possible failure locations include:

* incorrect responsibility selection;
* incorrect owner selection;
* inadequate training data;
* unit failure;
* validation failure;
* coordination failure;
* fallback failure.

Responsibility attribution is broader than parameter attribution.

It supports structural diagnosis.

---

# 42. Reward-to-Responsibility Attribution

In reinforcement or feedback-driven optimization, reward should be assigned to the responsible scope.

The sequence is:

```text
Observed Outcome
        ↓
Identify Active Responsibility
        ↓
Identify Responsible Call Path
        ↓
Locate Failing or Successful Segment
        ↓
Apply Local Update
```

This prevents reward from being spread indiscriminately across unrelated computation.

---

# 43. Responsibility as an Optimization Scope

A responsibility can define an optimization scope even when it spans multiple units.

Example:

```text
Responsibility:
Compiler Optimization
```

Possible scope:

```text
Compiler Dispatcher
+
Optimization Brain Unit
+
Validation Unit
```

The system may optimize the responsibility path rather than one model.

---

# 44. Responsibility and Local Training

Local training becomes possible when a responsibility has:

* supporting training data;
* bounded scope;
* known dependencies;
* validation criteria;
* fallback coverage.

The update process is:

```text
Responsibility Defect
        ↓
Select Supporting Data
        ↓
Select Unit or Path
        ↓
Local Training
        ↓
Responsibility Validation
```

---

# 45. Responsibility and Local Rollback

If an update harms the responsibility, the associated unit or path can be rolled back.

A responsibility-level rollback may restore:

* previous training group;
* previous Goal Function;
* previous unit version;
* previous dispatch rule;
* previous validation policy.

This is more complete than reverting model parameters alone.

---

# 46. Responsibility and Shared Units

A shared unit may serve several responsibilities.

Example:

```text
Optimization Unit
├── Compiler Optimization Responsibility
├── Control Optimization Responsibility
└── Planning Optimization Responsibility
```

Updating the unit for one responsibility may affect the others.

GTDO must therefore track:

* which responsibilities depend on the unit;
* which paths use it;
* which regression tests are required;
* whether a local adapter is safer;
* whether the responsibility should split.

---

# 47. Responsibility and General Capability

Specialized responsibilities should not destroy broad system capability.

A balanced architecture may include:

```text
Specialized Responsibilities
+
Shared Responsibilities
+
General Fallback Responsibility
```

General capability is itself an organizational responsibility.

It should not be treated as the unstructured remainder.

---

# 48. General Responsibility

A General Responsibility covers broad cases that do not justify or satisfy specialized dispatch.

It may include:

* ordinary language understanding;
* low-risk general questions;
* unsupported combinations;
* new domains;
* fallback explanation.

General responsibility preserves coverage and reduces over-fragmentation.

---

# 49. Responsibility and Human–AI Organization

Humans may hold explicit responsibilities within GTDO.

Examples include:

* approve high-risk actions;
* resolve ambiguous boundaries;
* define or revise Goal Functions;
* validate emerging responsibilities;
* arbitrate conflicts;
* certify releases.

The human node should not be represented only as failure fallback.

It may own primary responsibility where human judgment is structurally required.

---

# 50. Responsibility and Governance

Computational responsibilities may carry governance obligations.

Examples include:

* privacy protection;
* legal compliance;
* provenance tracking;
* safety review;
* audit retention;
* expert approval.

A responsibility contract may therefore include both computational and governance requirements.

---

# 51. Responsibility and Risk

Responsibilities differ in risk.

A low-risk responsibility may allow direct automated output.

A high-risk responsibility may require:

* independent validation;
* multi-path agreement;
* human approval;
* stricter fallback;
* certified data;
* narrower scope.

Risk is therefore an organizational property of responsibility, not only a property of the model.

---

# 52. Responsibility and Resource Control

Responsibilities may have different:

* latency budgets;
* hardware requirements;
* context lengths;
* cost limits;
* precision requirements;
* availability guarantees.

A responsibility contract can guide resource allocation.

This connects logical computation organization with physical systems engineering.

---

# 53. Responsibility and Training Data Provenance

Each responsibility should be linked to the training evidence supporting it.

A provenance chain may be:

```text
Runtime Outcome
        ↓
Call Path
        ↓
Computational Responsibility
        ↓
Computational Units
        ↓
Training Groups
        ↓
Source Data
```

This supports auditing, debugging, certification, and retraining.

---

# 54. Responsibility Drift

A responsibility may drift over time.

Causes include:

* changed goals;
* new data;
* changed user expectations;
* new regulations;
* expanded unit capability;
* new neighboring responsibilities;
* runtime dispatch drift.

Symptoms include:

* growing Boundary Sets;
* duplicated work;
* unstable dispatch;
* repeated fallback;
* declining validation performance.

Responsibility drift should trigger organizational review.

---

# 55. Responsibility Conflict

Two responsibilities may conflict.

Examples include:

```text
Maximize Helpfulness
        versus
Require Strict Safety Review
```

```text
Minimize Latency
        versus
Require Multi-Unit Validation
```

Conflicts may be resolved through:

* priority;
* hard constraints;
* arbitration responsibility;
* human approval;
* multi-stage processing.

Conflict resolution should be explicit.

---

# 56. Responsibility Coverage

Responsibility Coverage measures whether the system has an appropriate computational owner for valid cases.

Coverage should consider:

* specialist coverage;
* boundary coverage;
* fallback coverage;
* human escalation coverage;
* new-domain coverage.

A system with many specialists but weak fallback may have poor total coverage.

---

# 57. Responsibility Completeness

A responsibility definition is complete when it specifies enough information for controlled operation.

Minimum dimensions include:

* purpose;
* activation;
* scope;
* owner;
* output;
* validation;
* boundary;
* fallback;
* version.

Incomplete responsibility definitions create hidden control gaps.

---

# 58. Responsibility Coherence

Responsibility Coherence measures whether the cases assigned to a responsibility genuinely require related computation.

A coherent responsibility should not be based only on superficial similarity.

It should have a stable computational interpretation.

---

# 59. Responsibility Granularity

Responsibility Granularity refers to the breadth of a responsibility.

Broad responsibility:

```text
Software Engineering
```

Narrow responsibility:

```text
Optimize LLVM Loop Vectorization
```

The correct granularity depends on:

* data volume;
* performance variation;
* validation needs;
* update frequency;
* cost;
* reuse;
* risk.

GTDO should prefer the smallest useful granularity, not the smallest detectable granularity.

---

# 60. Responsibility Complexity

Responsibility Complexity may depend on:

* number of sub-responsibilities;
* number of owners;
* number of dependencies;
* boundary ambiguity;
* validation depth;
* fallback depth;
* runtime variability.

Complex responsibilities may require a graph rather than one unit.

---

# 61. Responsibility Economy

Responsibility Economy applies Operator Economy to organizational roles.

The framework should avoid:

* duplicate responsibilities;
* unnecessarily narrow roles;
* excessive coordination;
* unstable micro-responsibilities.

A small set of clear responsibilities is preferable to a large set of weakly differentiated ones.

---

# 62. Responsibility-Preserving Transformation

A Responsibility-Preserving Transformation changes implementation while preserving the responsibility contract.

Examples include:

* replace an LLM with a smaller model;
* replace a model validator with a symbolic checker;
* change hardware;
* update training data;
* reorganize internal functions.

The transformation is valid when responsibility invariants remain satisfied.

---

# 63. Responsibility-Changing Transformation

A transformation changes the responsibility itself.

Examples include:

* expand scope;
* narrow scope;
* add mandatory validation;
* change fallback;
* split into sub-responsibilities;
* merge with another role.

Responsibility-changing transformations require architectural review and versioning.

---

# 64. Responsibility Lifecycle

A responsibility may follow this lifecycle:

```text
Observed Need
        ↓
Responsibility Candidate
        ↓
Defined
        ↓
Validated
        ↓
Assigned
        ↓
Released
        ↓
Observed
        ↓
Updated / Split / Merged / Retired
```

This lifecycle should be independent from, but linked to, the lifecycle of its implementation.

---

# 65. Minimal Responsibility Record

A repository or implementation may represent a responsibility using:

```text
Responsibility ID

Name

Purpose

Goal Function

Input Scope

Context Requirements

Output Obligation

Primary Owner

Secondary Owner

Validation Owner

Boundary Policy

Fallback Policy

Risk Level

Dependencies

Training Groups

Call Paths

Version

Status
```

This record can become a core GTDO engineering artifact.

---

# 66. Example — Compiler Optimization Responsibility

## Name

Compiler Optimization

## Purpose

Improve generated or transformed code while preserving correctness.

## Activation

Compiler-related optimization task.

## Input Scope

* intermediate representation;
* optimization goal;
* platform constraints;
* relevant compiler context.

## Output Obligation

An optimized transformation or recommendation.

## Primary Owner

Compiler Optimization Brain Unit.

## Validator

Compiler Correctness Validator.

## Fallback

General Software Engineering Unit.

## Boundary Policy

Multi-path evaluation for unsupported optimization contexts.

## Validation

* semantic equivalence;
* performance improvement;
* target compatibility.

This responsibility may correspond to a complete Call Path.

---

# 67. Example — Boundary Resolution Responsibility

## Purpose

Handle cases that cannot be assigned confidently to dominant responsibilities.

## Possible Actions

* request more context;
* invoke multiple candidate units;
* use general fallback;
* defer;
* escalate to human review;
* create a new Responsibility Candidate.

This example shows that uncertainty itself can be organized as responsibility.

---

# 68. Example — Human Approval Responsibility

## Purpose

Approve or reject high-risk outputs.

## Activation

Risk threshold exceeded.

## Owner

Qualified human reviewer.

## Inputs

* candidate output;
* evidence;
* validation record;
* system confidence;
* policy context.

## Output

Approved, rejected, or returned for revision.

The human is a first-class computational participant within the organization.

---

# 69. Common Failure Modes

## Responsibility-Free Grouping

Groups exist without clear computational roles.

## Unit-First Design

A unit is created before its responsibility is defined.

## Topic–Responsibility Confusion

A subject label is mistaken for a computational obligation.

## Overlapping Ownership

Multiple units claim the same responsibility without coordination.

## Missing Ownership

A valid case has no responsible unit or path.

## Hidden Fallback

Fallback exists informally but is not defined or validated.

## Responsibility Creep

A unit gradually accepts work outside its original role.

## Responsibility Fragmentation

Too many narrow responsibilities create excessive routing and coordination.

## Responsibility Drift Without Versioning

The role changes silently.

## Validation Without Ownership

No unit or human is explicitly responsible for checking the result.

---

# 70. Evaluation of Computational Responsibility

A responsibility should be evaluated through:

* scope clarity;
* activation correctness;
* owner suitability;
* output quality;
* validation success;
* boundary handling;
* fallback success;
* assignment stability;
* coverage;
* local update effectiveness;
* cross-responsibility interference;
* resource cost;
* governance compliance.

The quality of the responsibility structure can be as important as the quality of individual units.

---

# 71. Canonical Comparison

| Concept                      | Primary Meaning                                                                     |
| ---------------------------- | ----------------------------------------------------------------------------------- |
| Topic                        | What subject area is involved                                                       |
| Class                        | What category the input belongs to                                                  |
| Task                         | What general work is requested                                                      |
| Capability                   | What a unit can do                                                                  |
| Computational Unit           | What implementation performs work                                                   |
| Computational Responsibility | What work must be owned, under which conditions, with which validation and fallback |
| Call Path                    | How one or more responsibilities execute                                            |
| Dispatch                     | How responsibility and owner are selected                                           |

---

# 72. Canonical GTDO Statements

> A training group becomes architecturally meaningful when it supports a computational responsibility.

> Computational Responsibility is the missing middle layer between training evidence and Computational Units.

> Capability describes possibility; responsibility describes assigned obligation.

> Responsibility should be defined before implementation is selected.

> A responsibility may be owned by one unit, multiple units, a Call Path, or a human–AI organization.

> Boundary handling, validation, fallback, and evolution are parts of responsibility.

> GTDO organizes computational responsibility; Calling Graphs organize the execution of that responsibility.

---

# 73. Central Transformation

The core transformation is:

```text
Training Evidence
        ↓
Goal-Oriented Group
        ↓
Responsibility Candidate
        ↓
Validated Computational Responsibility
        ↓
Computational Owner
        ↓
Dispatch and Call Path
        ↓
Local Validation and Evolution
```

This is the transition from organized data to organized computation.

---

# 74. Long-Term Significance

As AI systems become more heterogeneous, model identity alone will become an increasingly weak organizing principle.

A future system may combine:

* models;
* functions;
* tools;
* databases;
* agents;
* simulators;
* controllers;
* humans.

The stable organizing question will be:

> Which computational responsibility exists, and which structure should own it under current goals and context?

This makes Computational Responsibility a general systems concept rather than an LLM-specific abstraction.

---

# Key Takeaways

* Computational Responsibility is the organizational layer between training groups and Computational Units.
* It defines what work must be performed, under which conditions, by which owner, with which validation and fallback.
* Responsibility is different from topic, label, task, capability, and implementation.
* A responsibility may be owned by one unit, several units, a Call Path, or a human–AI organization.
* Responsibilities may be hierarchical, composite, shared, specialized, general, boundary-oriented, validating, or coordinating.
* Boundary Sets often represent unresolved responsibility rather than worthless data.
* Fallback, validation, and coordination are themselves responsibilities.
* Responsibility-first dispatch is more stable than unit-first routing.
* Responsibility graphs provide logical architecture before physical Dispatch Graphs and Calling Graphs are constructed.
* Responsibilities define valid scopes for local training, reinforcement, validation, versioning, and rollback.
* Responsibility definitions and implementations should be versioned separately.
* Specialization should preserve general responsibility and fallback coverage.
* Responsibility is a general AI Computation Organization concept, not an LLM-only concept.

---

## Further Reading

### GTDO Foundations

* GTDO-001 — *Why Goal-Oriented Training Data Organization*
* GTDO-002 — *From Data Segmentation to AI Computation Organization*
* GTDO-003 — *Goal Functions and RHS-Driven Training Organization*
* GTDO-004 — *Dispatch Is Not Segmentation*
* GTDO-005 — *Training Data Organization as Computation Organization*
* GTDO-007 — *Dispatch and Organizational Semantics*
* GTDO-008 — *Context as an Organizational Dimension*
* GTDO-009 — *Boundary Sets*

### GTDO Computational Organization

* GTDO-201 — *From Training Groups to Computational Units*
* GTDO-202 — *Heterogeneous Computational Units*
* GTDO-206 — *Computational Responsibility Graphs*
* GTDO-207 — *Dispatch Trees*
* GTDO-208 — *Dispatch Graphs*
* GTDO-209 — *Hybrid Computational Organizations*

### GTDO Call-Path Organization

* GTDO-301 — *Dispatch Trees as Calling Graphs*
* GTDO-302 — *Call Paths*
* GTDO-303 — *Call-Path Segments*
* GTDO-304 — *Call-Path Reinforcement Learning*
* GTDO-309 — *Structural Scope of Optimization*

### Related Structural Work

* **Structural Runtime AI (SRAI)**
* **Structural Recognition above Metric Similarity (SRMS)**
* **Function Tunnel and Runtime Invariant Algebra (FTRIA)**
