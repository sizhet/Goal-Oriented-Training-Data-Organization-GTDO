# GTDO-004 — Dispatch Is Not Segmentation

## Why Computational Responsibility Cannot Be Reduced to Data Boundaries

---

## Abstract

The terms **dispatch** and **segmentation** are often used near one another because both may divide a larger problem into smaller parts.

However, they solve fundamentally different problems.

Segmentation identifies or creates data boundaries.

Dispatch assigns computational responsibility.

A segment may have no dedicated computational owner. A computational responsibility may draw from many non-contiguous samples. One segment may require multiple computational units, while one computational unit may serve many distant segments, domains, or Call Paths.

Goal-Oriented Training Data Organization therefore makes the following distinction constitutional:

> **Segmentation determines where data is divided. Dispatch determines which computational structure is responsible.**

This article develops that distinction, explains why Point-to-Group Assignment cannot be described adequately as segmentation, shows how Point-to-Block Grouping combines boundaries with responsibility, and establishes dispatch as a general operator for AI Computation Organization.

---

# 1. The Source of the Confusion

Segmentation and dispatch frequently appear in the same workflow.

For example:

```text
Document
    ↓
Divide into Sections
    ↓
Send Each Section to a Processor
```

Because the two operations occur consecutively, they may appear to be one process.

They are not.

The first operation determines boundaries.

The second determines responsibility.

A clearer representation is:

```text
Document
    ↓
Segmentation
    ↓
Sections
    ↓
Dispatch
    ↓
Computational Units
```

The distinction becomes especially important when segmentation and dispatch do not align one-to-one.

---

# 2. Canonical Definitions

## Segmentation

Segmentation is the process of dividing data into regions, blocks, intervals, chunks, or sections.

It answers:

> **Where should one data region end and another begin?**

Typical segmentation outputs include:

* tokens;
* sentences;
* paragraphs;
* image regions;
* temporal intervals;
* code blocks;
* context windows;
* database partitions.

---

## Dispatch

Dispatch is the process of assigning data, context, tasks, or computational responsibilities to appropriate computational structures according to a Goal Function.

It answers:

> **Which computational structure should take responsibility?**

Typical dispatch outputs include:

* a Computational Unit;
* an LLM Brain Unit;
* a symbolic reasoner;
* a retrieval engine;
* a controller;
* a Call Path;
* a fallback path;
* multiple cooperating units;
* a human review node.

The canonical GTDO definition is:

> **Dispatch is the organization process that assigns computational responsibility to appropriate computational structures according to a Goal Function.**

---

# 3. Boundary versus Responsibility

The deepest distinction is:

```text
Segmentation
    ↓
Boundary

Dispatch
    ↓
Responsibility
```

A boundary is a statement about the structure or location of data.

A responsibility is a statement about the organization of computation.

These statements may correlate, but neither implies the other.

A boundary may be useful for storage or context management without creating a new computational responsibility.

A computational responsibility may exist across many disconnected data locations without producing a contiguous segment.

---

# 4. A Segment Does Not Automatically Have an Owner

Suppose a document is divided into five sections:

```text
[ Section 1 ]
[ Section 2 ]
[ Section 3 ]
[ Section 4 ]
[ Section 5 ]
```

This tells us where the data was divided.

It does not tell us:

* which model should process each section;
* whether all sections use the same model;
* whether one section requires retrieval;
* whether another requires symbolic verification;
* whether a section should be discarded;
* whether a human should review one section;
* whether multiple sections form one responsibility.

Segmentation creates addressable regions.

Dispatch creates computational ownership.

---

# 5. One Segment May Require Multiple Units

A single contiguous segment may contain several computational needs.

For example:

```text
One Technical Paragraph
├── Retrieve a standard
├── Check a formula
├── Interpret a requirement
└── Generate an explanation
```

The paragraph is one segment.

Its computation may require:

```text
Retrieval Unit
    ↓
Symbolic Validator
    ↓
Domain Brain Unit
    ↓
Language Generation Unit
```

Therefore:

```text
One Segment
    ≠
One Computational Unit
```

A segment may generate an entire Call Path.

---

# 6. One Computational Unit May Own Many Segments

The reverse relation is equally common.

A symbolic validator may process expressions found in:

* a physics document;
* a financial report;
* a control-system design;
* a compiler optimization explanation;
* a medical study.

These regions may be separated across documents, domains, and datasets.

Yet they share one computational responsibility:

```text
Validate Formal Expression
```

Therefore:

```text
Many Segments
    →
One Computational Responsibility
```

This relationship cannot be represented adequately by segmentation alone.

---

# 7. Dispatch Without Segmentation

Point-to-Group Assignment demonstrates that dispatch may occur without any contiguous data division.

Example:

```text
Sample 3   ─┐
Sample 11   │
Sample 28   ├──→ Responsibility A
Sample 47   │
Sample 92  ─┘
```

These samples may be widely separated in the original corpus.

No continuous region has been identified.

Nevertheless, they may share:

* the same RHS outcome;
* the same CCC;
* the same structural role;
* the same future computational responsibility.

This is a valid dispatch structure without segmentation.

---

# 8. Segmentation Without Dispatch

Segmentation may also occur without meaningful dispatch.

Example:

```text
Corpus
    ↓
Fixed 2,000-Token Chunks
    ↓
Chunk 1
Chunk 2
Chunk 3
```

The chunks may exist only because of:

* context-window limits;
* storage constraints;
* indexing convenience;
* parallel-processing requirements.

They may not correspond to distinct computational responsibilities.

This is segmentation without GTDO dispatch.

---

# 9. Four Possible Relationships

Segmentation and dispatch can relate in four different ways.

## 9.1 Segmentation Only

```text
Data
    ↓
Segments
```

No computational responsibility is assigned.

---

## 9.2 Dispatch Only

```text
Distributed Samples
    ↓
Responsibility Groups
```

No continuity is required.

---

## 9.3 Segmentation Followed by Dispatch

```text
Data
    ↓
Segments
    ↓
Computational Units
```

Boundaries are created first, then responsibilities are assigned.

---

## 9.4 Dispatch-Driven Segmentation

```text
Goal Function
    ↓
Desired Responsibility
    ↓
Find the Supporting Continuous Region
```

Here, the computational goal helps determine where the boundary should be placed.

Point-to-Block Grouping often follows this pattern.

---

# 10. Point-to-Group Assignment

Point-to-Group Assignment is the clearest proof that dispatch is broader than segmentation.

Its defining property is:

> Members of the same group are not required to occupy one continuous region.

The process may be represented as:

```text
Training Samples
        ↓
Goal Function
        ↓
Structural Recognition
        ↓
Group A / Group B / Boundary
```

The grouping criterion may use:

* RHS outcomes;
* direct labels;
* indirect context;
* CCC compatibility;
* structural invariants;
* computational roles.

Two-Way CCC is the principal GTDO algorithm for this mode.

---

# 11. Why “Point-to-Group” Is Not Merely Clustering

Point-to-Group Assignment may resemble clustering, but the organizing principle differs.

Conventional clustering often asks:

> Which samples are statistically close?

GTDO asks:

> Which samples should support the same computational responsibility under the Goal Function?

Two samples may be metrically dissimilar yet functionally equivalent.

Two samples may be metrically similar yet require different computational actions.

Therefore, Point-to-Group Assignment is goal-oriented responsibility construction, not merely proximity grouping.

---

# 12. Point-to-Block Grouping

Point-to-Block Grouping applies when continuity itself matters.

Examples include:

* a complete argument;
* a temporal episode;
* a code function;
* a failure interval;
* a document section;
* a local context window.

Its canonical structure is:

```text
Ordered Data
        ↓
Goal Function
+
Continuity Constraint
        ↓
Variable-Size Block
        ↓
Computational Responsibility
```

Variable-Size Blocks Indexing and Searching provides the principal structural mechanism.

The critical point is that the block is not the final result.

The block becomes meaningful when it is linked to responsibility.

---

# 13. Point-to-Block Grouping Is More Than Segmentation

A conventional segmentation process may stop after identifying a block.

GTDO continues:

```text
Recognized Block
        ↓
Responsibility Interpretation
        ↓
Dispatch Rule
        ↓
Computational Unit
        ↓
Validation and Optimization Scope
```

Thus, Point-to-Block Grouping contains segmentation-like mechanics but belongs to a larger computation-organization process.

The boundary serves the responsibility.

The responsibility does not exist merely to justify the boundary.

---

# 14. Dispatch Assigns Responsibility, Not Merely Destination

The word routing often emphasizes movement:

```text
Input
    ↓
Destination
```

GTDO dispatch has stronger semantics:

```text
Input
    ↓
Goal and Context Evaluation
    ↓
Responsibility Assignment
    ↓
Computational Structure
```

The selected structure becomes accountable for:

* producing an output;
* performing a transformation;
* validating another unit;
* retrieving evidence;
* controlling a process;
* handling uncertainty;
* coordinating other units.

Dispatch therefore establishes an organizational relationship, not only a transport relationship.

---

# 15. Dispatch Is Goal-Dependent

The same input may be dispatched differently under different goals.

Example input:

```text
A compiler error report
```

Possible Goal Functions may produce:

```text
Goal: Explain the error
    → Language Brain Unit

Goal: Find the failing code
    → Code Analysis Unit

Goal: Verify compiler behavior
    → Compiler Validation Unit

Goal: Search known defects
    → Retrieval Unit

Goal: Approve production release
    → Human Review Path
```

The data has not changed.

The computational responsibility has.

This is why dispatch cannot be defined by segmentation alone.

---

# 16. Dispatch Is Context-Dependent

Context can also alter responsibility.

Example:

```text
Input:
"Optimize this."
```

Possible contexts:

```text
Compiler Context
    → Compiler Optimization Unit

Database Context
    → Query Optimization Unit

Control Context
    → Controller-Tuning Unit

Business Context
    → Operations Planning Unit
```

The general dispatch relation is:

```text
Input
+
Context
+
Goal
+
Runtime State
        ↓
Dispatch Decision
```

No boundary-only operation can express this full relation.

---

# 17. Dispatch May Be Exclusive or Multiple

Segmentation often assigns each data point to one region.

Dispatch need not be exclusive.

A task may require:

```text
LLM Brain Unit
+
Retrieval Unit
+
Symbolic Validator
```

Possible dispatch modes include:

* single-unit dispatch;
* sequential multi-unit dispatch;
* parallel multi-unit dispatch;
* voting;
* validation;
* fallback;
* human escalation.

Therefore, dispatch may construct a computation graph rather than choose one destination.

---

# 18. Dispatch May Be Deferred

A valid GTDO decision may be:

```text
Do Not Dispatch Yet
```

Deferral may be appropriate when:

* context is incomplete;
* confidence is low;
* candidate units are unavailable;
* the responsibility is not yet represented;
* human approval is required;
* more evidence is expected.

Segmentation usually creates a boundary immediately.

Dispatch may deliberately postpone responsibility assignment.

---

# 19. Dispatch May Produce a Boundary Set

When no unit or group can accept responsibility confidently, GTDO may assign the case to a Boundary Set.

```text
Input
    ↓
Competing or Weak Evidence
    ↓
Boundary Set
```

The Boundary Set may later trigger:

* recursive Two-Way CCC;
* additional context generation;
* Boundary Brain Unit formation;
* multi-path dispatch;
* general fallback;
* human review;
* new responsibility discovery.

The Boundary Set is an organizational state, not merely a geometric boundary.

---

# 20. A Boundary Set Is Not the Boundary Between Segments

This distinction is important.

A segmentation boundary is usually a location:

```text
Segment A | Segment B
```

A GTDO Boundary Set is a collection of unresolved cases:

```text
{ Sample 7, Sample 19, Sample 44, Sample 105 }
```

These cases may be distributed across the dataset.

They may be mixed, transitional, weakly separated, or multi-responsibility.

Therefore:

```text
Segmentation Boundary
    ≠
GTDO Boundary Set
```

---

# 21. No-Split and No-Dispatch Are Different

A No-Split decision means:

> The current data should not be divided under this Goal Function.

A No-Dispatch decision means:

> Computational responsibility should not yet be assigned.

These outcomes may coincide, but they are distinct.

Example:

```text
No Split
+
Dispatch Entire Group to General Unit
```

or:

```text
No Split
+
Defer Responsibility Assignment
```

GTDO benefits from keeping these decisions explicit.

---

# 22. Dispatch Trees Are Not Segmentation Trees

A segmentation tree recursively divides data regions.

A Dispatch Tree recursively narrows computational responsibility.

Segmentation tree:

```text
Document
├── Section A
│   ├── Paragraph A1
│   └── Paragraph A2
└── Section B
```

Dispatch Tree:

```text
Engineering
├── Software
│   ├── Compiler
│   │   ├── Optimization
│   │   └── Verification
└── Control
```

The first tree describes where information is located.

The second describes who is responsible.

The structures may align in some applications, but their meanings remain different.

---

# 23. A Dispatch Tree Can Become a Calling Graph

Each path in a Dispatch Tree may correspond to a sequence of computational calls.

Example:

```text
General Dispatcher
        ↓
Engineering Unit
        ↓
Software Unit
        ↓
Compiler Unit
        ↓
Optimization Unit
```

This path is simultaneously:

* a responsibility hierarchy;
* a dispatch route;
* a runtime Call Path;
* a local optimization scope.

A segmentation tree alone does not imply these execution semantics.

---

# 24. Shared Units Turn Trees into Graphs

A computational unit may serve multiple branches.

Example:

```text
Mathematics ────┐
                ├──→ Optimization Unit
Software ───────┘
```

The resulting organization is no longer a simple tree.

It becomes a Dispatch Graph or Calling Graph.

This is another reason why dispatch should not be understood as data partitioning.

Data partitions generally emphasize separation.

Computation graphs often emphasize reuse, convergence, and cooperation.

---

# 25. Dispatch Creates Optimization Scope

One of the most important consequences of dispatch is that it identifies where optimization should occur.

Suppose a system underperforms on compiler optimization.

A Dispatch Tree may identify:

```text
Engineering
    ↓
Software
    ↓
Compiler
    ↓
Optimization
```

The system can then optimize:

* the full Call Path;
* the Compiler-to-Optimization segment;
* one Brain Unit;
* one dispatch rule;
* one training group.

Segmentation by itself does not establish this causal or organizational scope.

---

# 26. Dispatch Creates Validation Scope

Dispatch also determines where validation should be applied.

Possible scopes include:

* one assignment;
* one responsibility group;
* one Computational Unit;
* one Call Path;
* one shared subgraph;
* one fallback path.

This supports:

* local testing;
* local certification;
* version comparison;
* failure isolation;
* rollback.

The value of dispatch is therefore not limited to selection.

It creates the structure needed for controlled engineering.

---

# 27. Dispatch Creates Versioning Boundaries

When responsibilities are explicit, they can evolve independently.

Example:

```text
Compiler Optimization Unit
Version 1.2
    ↓
Local Update
    ↓
Version 1.3
```

Other branches may remain unchanged.

This enables:

* unit-level versioning;
* path-level release;
* branch-level rollback;
* shared-unit dependency checks.

A data segment may be versioned as content, but dispatch creates versioning boundaries for computation.

---

# 28. Dispatch Supports Fallback

A dispatch architecture can define alternative responsibility paths.

Example:

```text
Primary Specialist
        ↓
Low Confidence
        ↓
Boundary Unit
        ↓
Still Unresolved
        ↓
General Fallback
        ↓
Human Review
```

Fallback is a computation-organization property.

Segmentation does not normally define who acts when the first computational choice fails.

---

# 29. Dispatch Supports Responsibility Discovery

Dispatch structures may reveal missing capabilities.

Repeated unresolved cases may indicate:

* a missing Brain Unit;
* an overloaded general model;
* an emerging domain;
* an incorrect responsibility boundary;
* an inadequate Goal Function.

The system may then create a new branch.

Thus, dispatch is not only assignment.

It is also a discovery mechanism for future computation organization.

---

# 30. Dispatch Beyond LLMs

The distinction between segmentation and dispatch applies broadly.

## Vision

```text
Image Segmentation
    → Identifies regions

Dispatch
    → Sends regions to detection, measurement,
      diagnosis, control, or human review units
```

## Time Series

```text
Temporal Segmentation
    → Identifies episodes

Dispatch
    → Sends episodes to prediction,
      anomaly, control, or recovery units
```

## Software

```text
Code Segmentation
    → Identifies functions or blocks

Dispatch
    → Assigns compilation, security,
      testing, optimization, or review responsibilities
```

## Human–AI Systems

```text
Task Decomposition
    → Identifies work packages

Dispatch
    → Assigns work to AI agents,
      software services, or human experts
```

GTDO therefore concerns general computation organization.

---

# 31. Dispatch and Mixture of Experts

Mixture-of-Experts systems route inputs to selected expert components.

This is related to GTDO, but the concepts are not identical.

MoE routing usually operates within a predetermined model architecture.

GTDO may additionally determine:

* how training data should be organized;
* which responsibilities should exist;
* whether a unit should be a model at all;
* how Boundary Sets should be handled;
* how fallback should operate;
* how Call Paths should be optimized;
* how human or symbolic units should participate.

MoE may serve as one implementation mechanism inside a GTDO architecture.

It does not define the full GTDO problem.

---

# 32. Dispatch and Classification

Classification assigns a class.

Dispatch assigns responsibility.

A class may support dispatch, but the mapping is not always one-to-one.

Example:

```text
Class: Financial Document
```

Possible responsibilities include:

* extract values;
* check compliance;
* detect fraud;
* summarize;
* forecast;
* request human approval.

Classification describes what the input is.

Dispatch determines what computation should happen.

---

# 33. Dispatch and Routing

Routing chooses a destination or path.

GTDO dispatch includes routing but adds:

* Goal Function;
* computational responsibility;
* confidence;
* Boundary Sets;
* fallback;
* validation scope;
* optimization scope;
* evolution.

Routing is a transport abstraction.

Dispatch is an organizational abstraction.

---

# 34. Dispatch and Scheduling

Scheduling determines when a computation executes.

Dispatch determines who is responsible.

The two may cooperate:

```text
Dispatch
    ↓
Select Responsible Unit

Scheduling
    ↓
Determine Execution Time and Resources
```

GTDO should not collapse these control layers.

---

# 35. Dispatch and Load Balancing

Load balancing distributes work to manage utilization.

Dispatch chooses computational responsibility.

A load balancer may select among equivalent replicas.

GTDO dispatch may select among structurally different units.

Example:

```text
Load Balancing:
Which copy of the same service?

GTDO Dispatch:
Which capability should handle the task?
```

---

# 36. Dispatch and Access Control

Access control determines whether an operation is permitted.

Dispatch determines which structure is responsible.

A GTDO dispatch decision may be constrained by access control, safety, policy, or legal requirements.

The control layers remain distinct.

---

# 37. A Minimal Dispatch Specification

A practical GTDO Dispatch specification should include:

```text
Dispatch Name

Goal Function

Input Evidence

Required Context

Candidate Responsibilities

Candidate Computational Units

Confidence Rule

Boundary Policy

Multi-Path Policy

Fallback Policy

No-Dispatch Policy

Validation Rule

Version
```

This specification turns dispatch into an inspectable engineering artifact.

---

# 38. Dispatch Invariants

A mature dispatch system may preserve several invariants.

Examples include:

* every accepted task has a responsible path;
* every specialist has a fallback;
* low-confidence tasks are not forced into specialists;
* shared units are protected during local updates;
* high-risk cases include a validation path;
* dispatch changes are versioned;
* unresolved cases remain traceable.

These invariants make computation organization controllable.

---

# 39. Dispatch Failure Modes

## False Responsibility Assignment

A task is sent to a structurally inappropriate unit.

## Over-Segmentation Bias

Too many data boundaries are interpreted as separate responsibilities.

## Under-Organization

Distinct responsibilities remain inside one undifferentiated unit.

## Boundary Suppression

Uncertain cases are forced into dominant groups.

## Missing Fallback

No alternative path exists after failure.

## Responsibility Duplication

Multiple units unknowingly implement the same responsibility.

## Shared-Unit Damage

Local tuning harms other paths using a shared unit.

## Goal–Dispatch Mismatch

The dispatch policy no longer serves the current Goal Function.

---

# 40. Dispatch Evaluation

Dispatch should be evaluated using more than assignment accuracy.

Relevant measures include:

* responsibility correctness;
* output quality;
* confidence calibration;
* Boundary Set quality;
* fallback frequency;
* fallback success;
* dispatch latency;
* path stability;
* unit load;
* cross-path interference;
* local improvement;
* general coverage;
* rollback success.

The correct dispatch architecture may not be the one with the fewest Boundary cases.

It is the one that produces the most reliable computation organization.

---

# 41. Segmentation Metrics Are Not Enough

Segmentation may be evaluated using:

* boundary precision;
* region overlap;
* block coherence;
* intersection-over-union;
* continuity.

These metrics do not measure:

* whether the correct unit received responsibility;
* whether the Call Path succeeded;
* whether fallback worked;
* whether local tuning remained isolated;
* whether general capability was preserved.

GTDO therefore requires organization-level evaluation.

---

# 42. The Organizational Ladder

The transition from raw data to controlled computation can be expressed as:

```text
Data
    ↓
Segments or Samples
    ↓
Goal-Oriented Groups
    ↓
Computational Responsibilities
    ↓
Computational Units
    ↓
Dispatch Trees and Graphs
    ↓
Call Paths
    ↓
Localized Optimization
    ↓
Runtime Hybrid AI Organization
```

Segmentation may appear near the beginning.

Dispatch connects the entire ladder.

---

# 43. Canonical Comparison

| Dimension                 | Segmentation                  | Dispatch                                      |
| ------------------------- | ----------------------------- | --------------------------------------------- |
| Primary question          | Where should data be divided? | Who should take computational responsibility? |
| Primary object            | Data region                   | Responsibility-bearing computation            |
| Continuity                | Often central                 | Optional                                      |
| Non-contiguous assignment | Not usually central           | Fundamental capability                        |
| Goal dependence           | May be local or geometric     | Explicitly goal-oriented                      |
| Context dependence        | Sometimes                     | Often essential                               |
| Multiple destinations     | Not typical                   | Fully supported                               |
| Boundary Set              | Geometric boundary            | Unresolved responsibility set                 |
| Fallback                  | Outside ordinary scope        | Required                                      |
| Computational units       | Not necessarily identified    | Explicitly selected or formed                 |
| Call Paths                | Not implied                   | Natural result                                |
| Local optimization scope  | Not implied                   | Explicitly enabled                            |
| Versioning and rollback   | Data-oriented                 | Computation-oriented                          |
| Runtime evolution         | Usually outside scope         | Central long-term concern                     |

---

# 44. Canonical GTDO Statement

The main proposition of this article is:

> **Dispatch is not segmentation because computational responsibility is not equivalent to data continuity, data location, or data boundary.**

A concise version is:

```text
Segmentation divides data.

Dispatch assigns responsibility.

GTDO organizes computation.
```

---

# 45. Engineering Consequence

Once dispatch is treated as a first-class control layer, AI systems can move from:

```text
One Corpus
    ↓
One Model
    ↓
Global Optimization
```

toward:

```text
Goal-Oriented Evidence
        ↓
Explicit Responsibilities
        ↓
Appropriate Computational Units
        ↓
Inspectable Call Paths
        ↓
Localized Training and Validation
        ↓
Controlled Hybrid AI Evolution
```

This transition is not created by segmentation alone.

It requires explicit dispatch semantics.

---

# 46. Long-Term Significance

As AI systems expand beyond one-model architectures, the central engineering problem will increasingly become organizational.

The system must determine:

* which capabilities exist;
* which data support them;
* which unit is responsible;
* how units cooperate;
* when fallback is required;
* where optimization should occur;
* how updates remain local;
* how new responsibilities emerge.

Dispatch is the operator that connects these questions.

Segmentation may expose useful structure.

Dispatch turns structure into computation.

---

# Key Takeaways

* Segmentation and dispatch solve different problems.
* Segmentation creates data boundaries.
* Dispatch assigns computational responsibility.
* A segment may require multiple computational units.
* One computational unit may serve many distant segments.
* Point-to-Group Assignment provides dispatch without continuity.
* Point-to-Block Grouping combines segmentation mechanics with responsibility assignment.
* A GTDO Boundary Set is not the same as a geometric segmentation boundary.
* Dispatch may be single, multiple, deferred, fallback-based, or context-dependent.
* Dispatch Trees organize responsibility rather than merely dividing data.
* Dispatch Trees may become Calling Graphs and define Call Paths.
* Dispatch creates optimization, validation, versioning, and rollback scopes.
* MoE routing, classification, scheduling, and load balancing are related but narrower concepts.
* Segmentation divides data; dispatch turns data structure into controllable computation.

---

## Further Reading

### GTDO Foundations

* GTDO-001 — *Why Goal-Oriented Training Data Organization*
* GTDO-002 — *From Data Segmentation to AI Computation Organization*
* GTDO-003 — *Goal Functions and RHS-Driven Training Organization*
* GTDO-005 — *Training Data Organization as Computation Organization*
* GTDO-006 — *Computational Responsibility*
* GTDO-007 — *Dispatch and Organizational Semantics*

### GTDO Algorithms

* GTDO-101 — *Two Modes of Goal-Oriented Grouping*
* GTDO-102 — *Point-to-Group Assignment by Two-Way CCC*
* GTDO-103 — *Point-to-Block Grouping by Variable-Size Blocks*
* GTDO-105 — *Boundary Resolution*

### GTDO Architecture and Optimization

* GTDO-201 — *From Training Groups to Computational Units*
* GTDO-207 — *Dispatch Trees*
* GTDO-208 — *Dispatch Graphs*
* GTDO-301 — *Dispatch Trees as Calling Graphs*
* GTDO-302 — *Call Paths*
* GTDO-303 — *Call-Path Segments*

### Related Structural Work

* **Structural Runtime AI (SRAI)**
* **Structural Recognition above Metric Similarity (SRMS)**
* **Function Tunnel and Runtime Invariant Algebra (FTRIA)**
