# GTDO-007 — Dispatch and Organizational Semantics

## From Routing Decisions to Explicit Computational Responsibility

---

## Abstract

Dispatch is often interpreted as a routing operation:

```text
Input
    ↓
Destination
```

Goal-Oriented Training Data Organization assigns dispatch a stronger meaning.

Within GTDO, dispatch does not merely move data toward a computational endpoint. It interprets goals, context, structural evidence, confidence, runtime state, and available capabilities in order to assign computational responsibility.

The canonical GTDO relation is:

```text
Input
+
Context
+
Goal
+
Structural Evidence
+
Runtime State
        ↓
Dispatch
        ↓
Computational Responsibility
        ↓
Computational Unit or Call Path
```

This article develops the organizational semantics of dispatch. It explains why dispatch is broader than routing, classification, scheduling, load balancing, and expert selection; defines the semantic layers of a dispatch decision; describes single-path, multi-path, deferred, fallback, and boundary dispatch; and shows how dispatch becomes a central control operator for training-time organization, runtime execution, local optimization, validation, and structural evolution.

---

# 1. Why Dispatch Requires Semantics

A system may route data successfully while still assigning the wrong computational responsibility.

For example:

```text
Question
    ↓
Available Model
```

The routing operation may be technically valid.

However, it may ignore:

* the actual goal;
* the required type of computation;
* the risk level;
* the need for validation;
* the availability of specialist units;
* the need for fallback;
* the runtime state;
* the context of the request.

GTDO therefore distinguishes:

```text
Transport Decision
        from
Organizational Decision
```

Dispatch is an organizational decision.

It must carry meaning about what computation should occur and why.

---

# 2. Canonical Definition

Within GTDO:

> **Dispatch is the goal-oriented process that identifies an applicable computational responsibility and assigns that responsibility to an appropriate Computational Unit, Call Path, or Hybrid Computational Organization.**

This definition has four components:

1. **Goal orientation**
   Dispatch serves an intended outcome.

2. **Responsibility selection**
   Dispatch identifies what work must be performed.

3. **Owner selection**
   Dispatch selects the structure that should perform the work.

4. **Organizational control**
   Dispatch determines fallback, validation, path scope, and later evolution.

Dispatch is therefore more than destination selection.

---

# 3. The Semantic Layers of Dispatch

A complete dispatch decision may contain several layers.

```text
Input Interpretation
        ↓
Goal Interpretation
        ↓
Responsibility Identification
        ↓
Owner Selection
        ↓
Call-Path Construction
        ↓
Validation and Fallback Policy
```

Each layer adds organizational meaning.

A dispatch system that skips these layers may still route efficiently, but it may remain semantically weak.

---

# 4. Input Semantics

The first layer determines what the input represents.

Relevant evidence may include:

* content;
* structure;
* source;
* metadata;
* temporal position;
* surrounding context;
* previous calls;
* inferred intent;
* known RHS behavior.

Input semantics should not be reduced to surface wording.

Two inputs with similar words may require different responsibilities.

Two inputs with different wording may require the same responsibility.

---

# 5. Goal Semantics

The same input may require different dispatch under different goals.

Example:

```text
Input:
A compiler warning
```

Possible goals:

```text
Explain the warning
    → Explanation Responsibility

Determine whether it is safe
    → Validation Responsibility

Repair the source code
    → Code-Transformation Responsibility

Search for known defects
    → Retrieval Responsibility
```

Dispatch must therefore interpret the goal before selecting an owner.

---

# 6. Responsibility Semantics

The central semantic question is:

> What computation must be performed?

The answer should be expressed as a Computational Responsibility.

Examples include:

* retrieve evidence;
* generate a candidate;
* validate a result;
* control an actuator;
* resolve a boundary case;
* request human approval;
* coordinate multiple units.

A responsibility is more stable than a unit identity.

Units may change.

The responsibility remains the organizational reason for computation.

---

# 7. Ownership Semantics

Once a responsibility is identified, dispatch selects an owner.

The owner may be:

* one model;
* one Brain Unit;
* one function;
* one retrieval system;
* one symbolic engine;
* one agent;
* one human expert;
* one Call Path;
* one multi-unit organization.

Ownership semantics should specify:

* primary owner;
* alternate owner;
* validator;
* fallback;
* escalation path.

The selected owner should match the responsibility, not merely be available.

---

# 8. Path Semantics

Some responsibilities cannot be performed by one unit.

They require an ordered sequence.

Example:

```text
Retrieve Evidence
        ↓
Validate Evidence
        ↓
Reason over Evidence
        ↓
Generate Explanation
```

Dispatch therefore may select a Call Path rather than a single destination.

The path carries semantic meaning:

* what role each unit performs;
* why the order matters;
* where validation occurs;
* where fallback may activate;
* which segment may later be optimized.

---

# 9. Validation Semantics

Dispatch should specify how the result will be checked.

Possible validation semantics include:

* self-validation;
* independent validator;
* symbolic verification;
* multi-model agreement;
* human approval;
* runtime observation.

A dispatch decision without validation semantics may assign work but fail to define accountability.

---

# 10. Fallback Semantics

Fallback is not merely a backup destination.

It expresses what should happen when the preferred responsibility path cannot complete safely or confidently.

Fallback semantics may define:

```text
Low Confidence
    → General Unit

Validation Failure
    → Alternate Specialist

High Risk
    → Human Review

Unavailable Unit
    → Previous Stable Path

Unrecognized Responsibility
    → Boundary Process
```

Fallback should be attached to the responsibility and path, not improvised after failure.

---

# 11. Dispatch as an Organizational Operator

GTDO treats dispatch as a reusable Organization Operator.

Its general form is:

```text
Dispatch(
    Input,
    Context,
    Goal,
    Responsibility Candidates,
    Available Units,
    Confidence,
    Constraints
)
        ↓
Dispatch Decision
```

The output may contain:

```text
Selected Responsibility

Selected Owner

Selected Call Path

Confidence

Boundary Status

Fallback

Validation Rule

Version
```

This makes dispatch an inspectable engineering artifact.

---

# 12. Dispatch Is Not Routing

Routing usually answers:

> Where should the input go?

Dispatch answers:

> Which responsibility applies, who owns it, and under what control conditions?

Routing may be one internal mechanism of dispatch.

However:

```text
Routing
    =
Movement

Dispatch
    =
Organizational Assignment
```

A route may exist without responsibility semantics.

A GTDO dispatch decision should not.

---

# 13. Dispatch Is Not Classification

Classification answers:

> What category does the input belong to?

Dispatch answers:

> What computation should be performed?

Example:

```text
Class:
Financial Report
```

Possible responsibilities:

* extract numbers;
* detect fraud;
* summarize performance;
* check compliance;
* forecast risk;
* request human approval.

Classification can support dispatch.

It does not define the full decision.

---

# 14. Dispatch Is Not Scheduling

Scheduling determines when and with which resources computation should run.

Dispatch determines who is responsible.

The relationship is:

```text
Dispatch
    ↓
Select Responsibility and Owner

Scheduling
    ↓
Allocate Time and Resources
```

A complete system needs both.

They should remain separate control layers.

---

# 15. Dispatch Is Not Load Balancing

Load balancing chooses among equivalent or near-equivalent resources.

Dispatch may choose among structurally different capabilities.

Example:

```text
Load Balancing:
Choose Server A or Server B

GTDO Dispatch:
Choose Retrieval, Reasoning,
Validation, Control, or Human Review
```

Load balancing optimizes distribution.

Dispatch organizes computation.

---

# 16. Dispatch Is Not Merely Expert Selection

Mixture-of-Experts systems select among predefined experts.

GTDO dispatch is broader because it may determine:

* which responsibility exists;
* whether an expert should be created;
* whether the case belongs to a Boundary Set;
* whether several units should cooperate;
* whether a non-model unit is preferable;
* whether fallback is required;
* which path should later receive reinforcement.

Expert selection can implement part of dispatch.

It does not exhaust the concept.

---

# 17. Dispatch Is Not Static Function Mapping

A static map may take the form:

```text
Input Type
    →
Unit
```

GTDO dispatch is generally richer:

```text
Input
+
Context
+
Goal
+
Runtime State
+
Confidence
+
Available Capabilities
        ↓
Dispatch Decision
```

The same input may produce different valid dispatches under different conditions.

---

# 18. Training-Time Dispatch

Training-time dispatch organizes evidence according to future computational responsibility.

Example:

```text
Training Sample
        ↓
Goal Function
        ↓
Responsibility Group
        ↓
Training Scope
```

Training-time dispatch may determine:

* which unit receives the sample;
* which Boundary Set retains it;
* which fallback group preserves coverage;
* which Call Path the sample supports;
* which validation set should include it.

This is not runtime execution.

It is architecture formation.

---

# 19. Runtime Dispatch

Runtime dispatch activates existing computational responsibilities.

General form:

```text
Runtime Input
        ↓
Goal and Context Interpretation
        ↓
Responsibility Selection
        ↓
Call Path Activation
```

Runtime dispatch may also generate feedback for future GTDO reorganization.

Thus, training-time and runtime dispatch form a loop.

---

# 20. Offline Dispatch Semantics

Offline dispatch may use:

* training labels;
* RHS outputs;
* source relationships;
* document structure;
* historical outcomes;
* generated context;
* known responsibilities.

Its objective is to organize training data and architecture before runtime.

---

# 21. Online Dispatch Semantics

Online dispatch may use:

* current user intent;
* runtime state;
* available units;
* cost;
* latency;
* confidence;
* risk;
* previous Call Paths;
* recent failures.

Its objective is to select the appropriate responsibility and execution path under current conditions.

---

# 22. Single-Unit Dispatch

The simplest case assigns one responsibility to one unit.

```text
Input
    ↓
Responsibility
    ↓
Unit
```

This is appropriate when:

* the responsibility is narrow;
* one unit is sufficient;
* validation is simple;
* fallback is clear.

Even this simple case should retain explicit semantics.

---

# 23. Sequential Multi-Unit Dispatch

Some tasks require an ordered sequence.

```text
Unit A
    ↓
Unit B
    ↓
Unit C
```

The order itself may be part of the responsibility.

Examples include:

* retrieve, validate, generate;
* detect, diagnose, repair;
* plan, simulate, execute;
* propose, review, approve.

Sequential dispatch constructs a Call Path.

---

# 24. Parallel Multi-Unit Dispatch

Several units may process the same input in parallel.

```text
Input
├── Unit A
├── Unit B
└── Unit C
```

Possible purposes include:

* voting;
* diversity;
* validation;
* uncertainty estimation;
* independent analysis;
* safety review.

Parallel dispatch requires a result-combination responsibility.

---

# 25. Cooperative Dispatch

Units may contribute different pieces to one result.

Example:

```text
Retrieval Unit
+
Symbolic Solver
+
Domain Brain Unit
+
Human Reviewer
```

The organization must define:

* contribution roles;
* sequencing;
* shared context;
* conflict resolution;
* final ownership.

Cooperation without explicit semantics can create accountability gaps.

---

# 26. Multi-Path Dispatch

A case may activate multiple Call Paths.

```text
Input
├── Path A
└── Path B
```

Multi-Path Dispatch may be used when:

* the case is cross-domain;
* confidence is low;
* validation requires independence;
* several responsibilities apply;
* a Boundary Set is being resolved.

The paths may later:

* vote;
* merge;
* validate;
* defer;
* escalate.

---

# 27. Deferred Dispatch

A valid decision may be:

```text
Do Not Assign Yet
```

Deferred dispatch is appropriate when:

* context is incomplete;
* evidence is insufficient;
* required units are unavailable;
* the responsibility is not represented;
* human input is pending.

Deferral is not failure.

It is a controlled organizational state.

---

# 28. Boundary Dispatch

Boundary dispatch handles unresolved or mixed cases.

Possible actions include:

```text
Request More Context

Invoke Multiple Candidates

Use Boundary Unit

Use General Fallback

Escalate to Human

Create New Responsibility Candidate
```

Boundary dispatch converts uncertainty into explicit process.

---

# 29. Fallback Dispatch

Fallback dispatch activates an alternate owner or path after:

* low confidence;
* unit failure;
* validation failure;
* policy restriction;
* unsupported input;
* excessive cost or latency.

Fallback should preserve traceability.

The system should know:

* why fallback occurred;
* which primary path failed;
* which fallback version acted;
* whether the case should enter future training.

---

# 30. No-Dispatch Decision

A No-Dispatch decision means that no computational responsibility should currently be assigned.

Possible reasons include:

* invalid request;
* insufficient evidence;
* prohibited action;
* unavailable approval;
* unresolved goal;
* unsupported system scope.

No-Dispatch differs from fallback.

Fallback still assigns responsibility.

No-Dispatch may stop or defer the process.

---

# 31. Dispatch Confidence

Dispatch Confidence measures confidence in the responsibility and owner selection.

It may reflect:

* structural match;
* context quality;
* Goal Function clarity;
* unit suitability;
* historical success;
* path stability.

Low confidence may trigger:

* multi-path dispatch;
* fallback;
* Boundary Set handling;
* human review;
* deferral.

---

# 32. Confidence Is Not Responsibility

Confidence modifies how a responsibility is executed.

It does not necessarily define the responsibility itself.

Example:

```text
Responsibility:
Medical Safety Review
```

High confidence:

```text
Specialist + Validator
```

Low confidence:

```text
Specialist + Human Review
```

The responsibility remains the same.

The path changes.

---

# 33. Dispatch Thresholds

A dispatch policy may use thresholds.

Examples include:

* specialist activation threshold;
* multi-path threshold;
* fallback threshold;
* human-review threshold;
* no-dispatch threshold.

Thresholds should be:

* versioned;
* validated;
* context-aware;
* responsibility-specific where necessary.

One global threshold may be inappropriate across heterogeneous responsibilities.

---

# 34. Dispatch Constraints

Dispatch may be constrained by:

* safety;
* law;
* privacy;
* latency;
* cost;
* hardware;
* availability;
* human approval;
* provenance;
* certification.

Constraints may override preference.

Example:

```text
Preferred Unit
    unavailable under policy
        ↓
Approved Alternate Path
```

---

# 35. Hard and Soft Dispatch Rules

## Hard Rule

Must be followed.

Example:

```text
High-risk output requires human approval.
```

## Soft Rule

Preferred under normal conditions.

Example:

```text
Use specialist when latency budget permits.
```

The distinction should be explicit.

---

# 36. Dispatch Priority

Multiple responsibilities may apply.

A priority system may use:

* safety first;
* legal obligation;
* primary user goal;
* confidence;
* resource cost;
* latency;
* expected quality.

Priority is part of organizational semantics.

Without it, dispatch conflicts remain unresolved.

---

# 37. Dispatch Conflict

A Dispatch Conflict occurs when:

* multiple responsibilities claim the case;
* units disagree;
* goals conflict;
* path constraints are incompatible;
* cost and quality objectives compete.

Resolution mechanisms include:

* priority rules;
* arbitration unit;
* human review;
* multi-path comparison;
* deferred dispatch.

---

# 38. Arbitration Responsibility

An Arbitration Responsibility decides among competing dispatch candidates.

It may consider:

* confidence;
* risk;
* expected value;
* policy;
* runtime state;
* prior performance.

The arbitrator may be:

* a rule system;
* a model;
* a coordinator;
* a human.

Arbitration should itself be explicit and validated.

---

# 39. Dispatch Trees

A Dispatch Tree organizes hierarchical responsibility selection.

Example:

```text
General
├── Engineering
│   ├── Software
│   │   ├── Compiler
│   │   │   ├── Optimization
│   │   │   └── Verification
└── Science
```

Each level narrows organizational meaning.

The path from root to node represents a sequence of responsibility decisions.

---

# 40. Dispatch Graphs

A Dispatch Graph generalizes a tree.

It supports:

* shared units;
* multiple parents;
* converging paths;
* validation edges;
* fallback edges;
* cross-domain cooperation.

A graph is required when computation organization emphasizes reuse and cooperation rather than strict partitioning.

---

# 41. Dispatch Semantics of Tree Nodes

A node may represent:

* a responsibility;
* a decision;
* a Computational Unit;
* a boundary process;
* a validator;
* a fallback;
* a coordinator.

These meanings should not be mixed accidentally.

A well-designed tree documents the semantic role of each node.

---

# 42. Dispatch Semantics of Edges

An edge may mean:

* specialization;
* dependency;
* call;
* fallback;
* validation;
* escalation;
* data transfer;
* responsibility delegation.

Edges should therefore have explicit types.

A graph with unlabeled edges may be computationally connected but organizationally ambiguous.

---

# 43. Dispatch and Call Paths

A Call Path is the runtime realization of dispatch semantics.

Example:

```text
General Dispatcher
        ↓
Engineering Responsibility
        ↓
Compiler Responsibility
        ↓
Optimization Unit
        ↓
Validation Unit
```

The path represents:

* selected goals;
* selected responsibilities;
* selected owners;
* execution order;
* validation structure.

---

# 44. Dispatch and Call Path Segments

A Call Path Segment is a local organizational scope.

Example:

```text
Compiler
    ↓
Optimization
    ↓
Validation
```

This segment may be:

* retrained;
* reinforced;
* versioned;
* validated;
* rolled back.

Dispatch semantics make the segment meaningful.

Without responsibility semantics, it is only a sequence of calls.

---

# 45. Dispatch and Optimization Scope

A dispatch decision can determine where optimization should occur.

Example:

```text
Observed Failure
        ↓
Active Dispatch Path
        ↓
Responsible Segment
        ↓
Local Optimization
```

Possible targets include:

* dispatch rule;
* responsibility definition;
* unit;
* path segment;
* validator;
* fallback policy.

The correct target may not be the model itself.

---

# 46. Dispatch and Reward Attribution

In Call-Path Reinforcement Learning, dispatch records provide the structure needed for reward attribution.

```text
Outcome
    ↓
Active Responsibility
    ↓
Active Call Path
    ↓
Responsible Segment
    ↓
Reward or Error Update
```

This can reduce indiscriminate global updates.

---

# 47. Dispatch and Validation Scope

The dispatch record determines what should be validated.

Possible scopes include:

* assignment;
* responsibility;
* owner;
* path;
* fallback;
* graph interaction.

Validation should test both:

* whether the computation succeeded;
* whether the correct responsibility and path were selected.

---

# 48. Dispatch and Versioning

A dispatch system should version:

* Goal Function;
* responsibility definitions;
* routing rules;
* thresholds;
* unit mappings;
* fallback policy;
* path definitions.

A runtime result should ideally record which dispatch version produced it.

---

# 49. Dispatch and Rollback

A dispatch change may be rolled back independently from a model change.

Example:

```text
New Dispatch Rule
        ↓
Path Quality Declines
        ↓
Restore Previous Rule
```

Likewise, a unit may be rolled back while preserving the responsibility definition.

This separation improves control.

---

# 50. Dispatch and Drift

Dispatch Drift occurs when behavior changes over time.

Causes include:

* new data;
* new contexts;
* updated units;
* changed goals;
* new responsibilities;
* shifting confidence distributions.

Symptoms include:

* growing fallback frequency;
* unstable path selection;
* overloaded branches;
* increasing Boundary Sets;
* declining responsibility accuracy.

Drift should trigger organizational review.

---

# 51. Dispatch Stability

Dispatch Stability measures whether equivalent cases receive consistent organizational treatment.

Stability should be evaluated against:

* small input changes;
* equivalent paraphrases;
* context variation;
* version updates;
* unit availability changes.

Perfect stability is not always desirable.

Relevant context changes should alter dispatch.

The objective is structurally justified stability.

---

# 52. Dispatch Coverage

Dispatch Coverage measures whether valid cases receive an appropriate responsible path.

Coverage includes:

* specialist coverage;
* general coverage;
* boundary coverage;
* fallback coverage;
* human escalation coverage.

A system may have accurate specialist dispatch but poor total coverage.

---

# 53. Dispatch Economy

Dispatch Economy seeks the simplest organization that provides adequate responsibility coverage.

Excessive dispatch complexity can cause:

* latency;
* unstable routing;
* duplicated units;
* difficult debugging;
* high validation cost.

The objective is not maximum branching.

It is sufficient organizational distinction.

---

# 54. Dispatch Granularity

Dispatch Granularity determines how narrow a dispatch decision is.

Broad:

```text
Engineering
```

Narrow:

```text
LLVM Loop Vectorization Optimization
```

The correct granularity depends on:

* data support;
* unit availability;
* validation benefit;
* update frequency;
* latency;
* risk;
* reuse.

GTDO should prefer the smallest useful granularity.

---

# 55. Dispatch Invariants

Possible dispatch invariants include:

* every accepted task has a responsible path;
* every specialist has a fallback;
* low-confidence cases are not forced into specialists;
* high-risk paths include validation;
* shared units expose dependencies;
* dispatch changes are versioned;
* unresolved cases remain traceable.

These invariants support system-level trust.

---

# 56. Dispatch Failure Modes

## Semantic Misdispatch

The system selects a technically available but structurally inappropriate unit.

## Goal Misinterpretation

The dispatch system identifies the wrong intended outcome.

## Responsibility Collapse

Distinct responsibilities are routed to one undifferentiated unit.

## Over-Specialization

Too many narrow paths reduce coverage and stability.

## Boundary Suppression

Ambiguous cases are forced into dominant branches.

## Missing Fallback

No valid alternate path exists.

## Path Explosion

The dispatch graph becomes unnecessarily complex.

## Shared-Unit Interference

A local update damages several dispatch paths.

## Silent Drift

Dispatch behavior changes without versioning or review.

---

# 57. Dispatch Evaluation

Dispatch should be evaluated using:

* responsibility-selection accuracy;
* owner suitability;
* path success;
* confidence calibration;
* fallback frequency;
* fallback success;
* Boundary Set quality;
* latency;
* stability;
* coverage;
* cross-path interference;
* local optimization success;
* human escalation quality;
* rollback success.

No single metric is sufficient.

---

# 58. Minimal Dispatch Record

A practical dispatch record may include:

```text
Dispatch ID

Input Reference

Goal

Context

Selected Responsibility

Primary Owner

Selected Call Path

Confidence

Boundary Status

Fallback

Validation Rule

Dispatch Policy Version

Outcome

Feedback
```

This record supports audit, debugging, optimization, and future reorganization.

---

# 59. Minimal Dispatch Policy

A dispatch policy should define:

```text
Policy Name

Applicable Goals

Input Evidence

Context Requirements

Responsibility Candidates

Owner Candidates

Priority Rules

Confidence Thresholds

Boundary Policy

Multi-Path Policy

Fallback Policy

No-Dispatch Policy

Validation Rules

Version
```

---

# 60. Example — Compiler Analysis

Input:

```text
Compiler optimization regression
```

Goal:

```text
Identify cause and recommend repair
```

Dispatch semantics:

```text
Responsibility 1:
Retrieve recent compiler changes

Responsibility 2:
Analyze optimization behavior

Responsibility 3:
Validate semantic correctness

Responsibility 4:
Recommend repair
```

Call Path:

```text
Repository Retrieval Unit
        ↓
Compiler Analysis Brain Unit
        ↓
Symbolic or Test Validator
        ↓
Repair Recommendation Unit
```

Fallback:

```text
General Software Engineering Unit
```

Escalation:

```text
Human Compiler Expert
```

The result is an organizational plan, not merely a destination.

---

# 61. Example — Boundary Case

Input matches both:

```text
Legal Analysis
and
Financial Risk
```

Possible dispatch:

```text
Legal Path
        +
Financial Path
        ↓
Joint Validation
        ↓
Human Approval
```

The case should not be forced into one branch if the responsibility is genuinely composite.

---

# 62. Example — Control System

Input:

```text
Unexpected temperature rise
```

Goal:

```text
Maintain safe operation
```

Dispatch may select:

```text
Anomaly Detection
        ↓
State Estimation
        ↓
Control Adjustment
        ↓
Safety Validation
```

If confidence is low:

```text
Safe Shutdown
or
Human Operator
```

This demonstrates GTDO dispatch beyond LLMs.

---

# 63. Example — Human–AI Organization

Goal:

```text
Approve a high-impact decision
```

Dispatch may assign:

```text
AI Evidence Collection
        ↓
AI Risk Analysis
        ↓
Human Decision Responsibility
```

The human is not merely fallback.

The human may own the final responsibility by design.

---

# 64. Dispatch and General AI Computation Organization

Dispatch is general because responsibility is general.

The same semantics apply to:

* language models;
* vision systems;
* world models;
* planners;
* retrieval systems;
* symbolic solvers;
* controllers;
* software functions;
* agents;
* humans.

The implementation differs.

The organizational principle remains:

```text
Goal
    ↓
Responsibility
    ↓
Owner
    ↓
Path
```

---

# 65. Dispatch and Structural Runtime AI

GTDO dispatch and SRAI Runtime Organization connect through:

```text
Recognition
    ↓
Responsibility
    ↓
Dispatch
    ↓
Runtime Organization
    ↓
Observed Outcome
    ↓
Local Evolution
```

GTDO emphasizes how responsibilities and paths are formed from training evidence.

SRAI emphasizes how structural computation operates and evolves at runtime.

---

# 66. Dispatch and Calling Graphs

The relationship is:

```text
Dispatch
    selects and assigns responsibility.

Calling Graph
    realizes execution relationships.
```

A Dispatch Tree may become a Calling Graph.

A responsibility path may become a runtime Call Path.

A dispatch edge may become a call edge.

However, the semantic reason for the call remains the responsibility.

---

# 67. Canonical Distinctions

| Concept        | Main Question                                                             |
| -------------- | ------------------------------------------------------------------------- |
| Classification | What is the input?                                                        |
| Segmentation   | Where should data be divided?                                             |
| Routing        | Where should data move?                                                   |
| Scheduling     | When should computation run?                                              |
| Load Balancing | Which equivalent resource should receive work?                            |
| Dispatch       | Which responsibility applies, who owns it, and which path should execute? |
| Calling Graph  | How do computational units invoke one another?                            |

---

# 68. Canonical GTDO Statements

> Dispatch assigns computational responsibility, not merely destination.

> Responsibility selection should precede owner selection.

> A dispatch decision may select one unit, several units, a Call Path, a Boundary process, a fallback, or no dispatch.

> Dispatch semantics include goal, context, responsibility, ownership, validation, fallback, and version.

> A Dispatch Tree is a responsibility structure before it is an execution structure.

> Dispatch records provide the basis for path-level validation, reinforcement, versioning, and rollback.

> GTDO dispatch is a general AI Computation Organization operator, not an LLM-only routing mechanism.

---

# 69. Central Transformation

The complete dispatch transformation is:

```text
Input
+
Context
+
Goal
+
Structural Evidence
+
Runtime State
        ↓
Responsibility Interpretation
        ↓
Owner Selection
        ↓
Call-Path Construction
        ↓
Validation and Fallback
        ↓
Observed Outcome
        ↓
Feedback and Reorganization
```

This is the organizational semantics of dispatch.

---

# 70. Long-Term Significance

As AI systems become heterogeneous, dispatch may become one of the primary control surfaces of intelligence.

The important engineering questions will no longer be limited to:

* Which model is largest?
* Which model has the lowest loss?
* Which model produces the highest benchmark score?

They will increasingly include:

* Which responsibility should exist?
* Which unit should own it?
* Which path should execute?
* Which fallback should protect it?
* Which segment should be improved?
* Which organizational change is justified?

Dispatch connects these questions into one control layer.

---

# Key Takeaways

* Dispatch is a semantic organizational decision, not merely routing.
* Dispatch interprets goals, context, structural evidence, confidence, runtime state, and available capabilities.
* Responsibility selection should conceptually precede owner selection.
* Dispatch may select one unit, multiple units, a Call Path, a Boundary process, fallback, deferral, or No-Dispatch.
* Routing, classification, scheduling, load balancing, and expert selection are related but narrower concepts.
* Training-time dispatch organizes data and capability formation.
* Runtime dispatch activates responsibilities and execution paths.
* Dispatch Trees organize hierarchical responsibility.
* Dispatch Graphs support shared, converging, validating, and fallback relationships.
* Dispatch semantics make Call Paths suitable for local optimization, validation, versioning, and rollback.
* Boundary and fallback behavior must be part of the dispatch policy.
* Dispatch records provide structural evidence for reward attribution and future reorganization.
* GTDO dispatch applies to heterogeneous AI and human–AI systems, not only LLMs.
* Dispatch assigns computational responsibility; Calling Graphs execute that responsibility.

---

## Further Reading

### GTDO Foundations

* GTDO-001 — *Why Goal-Oriented Training Data Organization*
* GTDO-002 — *From Data Segmentation to AI Computation Organization*
* GTDO-003 — *Goal Functions and RHS-Driven Training Organization*
* GTDO-004 — *Dispatch Is Not Segmentation*
* GTDO-005 — *Training Data Organization as Computation Organization*
* GTDO-006 — *Computational Responsibility*
* GTDO-008 — *Context as an Organizational Dimension*
* GTDO-009 — *Boundary Sets*

### GTDO Algorithms and Architecture

* GTDO-101 — *Two Modes of Goal-Oriented Grouping*
* GTDO-102 — *Point-to-Group Assignment by Two-Way CCC*
* GTDO-103 — *Point-to-Block Grouping by Variable-Size Blocks*
* GTDO-105 — *Boundary Resolution*
* GTDO-206 — *Computational Responsibility Graphs*
* GTDO-207 — *Dispatch Trees*
* GTDO-208 — *Dispatch Graphs*

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
