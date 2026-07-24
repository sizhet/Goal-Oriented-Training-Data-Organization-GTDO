# GTDO GLOSSARY

## Goal-Oriented Training Data Organization

### From Data Segmentation to General AI Computation Organization

**Document Type:** Canonical Terminology Reference
**Status:** Active Repository Standard
**Version:** 1.0

---

# 1. Purpose

This glossary defines the canonical terminology of Goal-Oriented Training Data Organization.

GTDO connects several domains that often use overlapping words with different meanings:

* training-data processing;
* structural recognition;
* clustering and segmentation;
* dispatch and routing;
* computational responsibility;
* modular AI;
* Brain Units;
* Calling Graphs;
* local optimization;
* runtime organization;
* Hybrid AI;
* control engineering.

Without stable terminology, GTDO can easily be misunderstood as:

* ordinary data segmentation;
* topic clustering;
* mixture-of-experts routing;
* model partitioning;
* LLM-only organization;
* static data preprocessing.

This glossary establishes the meanings that should be used consistently across:

* articles;
* figures;
* algorithm descriptions;
* implementation documents;
* repository navigation;
* release notes;
* future extensions.

Where a term has a broader conventional meaning, this glossary defines its specific GTDO usage.

---

# 2. Core Conceptual Chain

The central GTDO progression is:

```text
Goal
  ↓
Structural Recognition
  ↓
Grouping
  ↓
Boundary Resolution
  ↓
Computational Responsibility
  ↓
Dispatch
  ↓
Computational Unit
  ↓
Call Path
  ↓
Localized Optimization
  ↓
Runtime Organization
  ↓
Controlled Evolution
```

Each major term in this glossary should be interpreted within this progression.

---

# 3. Foundational Terms

## Goal-Oriented Training Data Organization

**Abbreviation:** GTDO

A framework for organizing training data, context, computational responsibilities, computational units, dispatch structures, and optimization scopes according to explicit or recoverable goals.

GTDO does not organize data merely to create partitions.

It organizes data to support the formation, selection, training, invocation, validation, and evolution of computational capabilities.

Canonical progression:

```text
Training Data
    ↓
Goal-Oriented Organization
    ↓
Computational Responsibility
    ↓
Computational Architecture
```

GTDO begins with training data but extends into general AI computation organization.

---

## Goal Orientation

The principle that a grouping, dispatch, or organization process must be controlled by an intended computational objective.

Goal orientation distinguishes GTDO from unconstrained statistical clustering.

A valid GTDO process should be able to explain:

* what distinction is being sought;
* why the distinction matters;
* which responsibility it represents;
* which computational unit should receive it;
* how success will be evaluated.

---

## Goal Function

A function, rule, structural condition, objective, or control policy that defines the intended grouping or dispatch outcome.

A Goal Function may use:

* RHS outputs;
* labels;
* structural properties;
* contextual evidence;
* task requirements;
* confidence conditions;
* domain responsibility;
* runtime conditions;
* safety constraints;
* human-defined objectives.

General form:

```text
Input Data
+ Context
+ Known Evidence
+ Organizational Objective
        ↓
Goal Function
        ↓
Group / Boundary / Discard / Fallback / Multi-Path Decision
```

A Goal Function may be binary, multi-group, hierarchical, continuous, structural, contextual, or adaptive.

---

## RHS Grouping Goal

A grouping objective defined primarily by the desired or observed right-hand-side output.

Example:

```text
lhs words
    ↓
rhs group 0

lhs words
    ↓
rhs group 1
```

The RHS grouping goal determines how training inputs should be organized according to their target-output families.

RHS grouping is an important initial GTDO case, but GTDO is not limited to supervised output labels.

---

## LHS Data

The input side of a training relationship.

In language-model examples, LHS data may include:

* preceding words;
* prompt words;
* local token sequences;
* document context;
* generated context;
* metadata;
* structural features.

General form:

```text
LHS Input
    →
RHS Target
```

---

## RHS Data

The target, output, outcome, response, state transition, or responsibility indicator associated with LHS data.

RHS data may be:

* one token;
* multiple tokens;
* a class;
* a structural output;
* an action;
* a decision;
* an event;
* a runtime state;
* a computation result.

---

## Training Data Organization

The process of arranging training data according to computational goals and future responsibilities.

Training Data Organization may determine:

* which samples belong together;
* which samples should remain separate;
* which context should be preserved;
* which data should be discarded;
* which data requires fallback;
* which computational unit should be formed;
* which training scope should be used.

It is broader than data partitioning because it connects data structure to computational architecture.

---

## AI Computation Organization

The organization of computational responsibilities, capabilities, units, calls, dependencies, paths, and optimization scopes within an AI or Hybrid AI system.

AI Computation Organization is not restricted to LLMs.

It may organize:

* LLM Brain Units;
* world models;
* symbolic reasoners;
* search engines;
* planners;
* retrieval systems;
* databases;
* simulators;
* software functions;
* control units;
* agents;
* human experts;
* hybrid organizations.

GTDO is one route from training-data structure to AI Computation Organization.

---

## General AI Computation Organization

The most general interpretation of AI Computation Organization.

It refers to organization principles applicable across heterogeneous computational paradigms rather than one model family.

The term does not imply that a system possesses artificial general intelligence.

It means that the organization framework is general across AI computation types.

---

# 4. Structural Recognition Terms

## Structural Recognition

The identification of meaningful structural distinctions, relationships, invariants, boundaries, or responsibilities within data or computation.

Structural Recognition may use:

* CCC;
* Two-Way CCC;
* Runtime Invariants;
* pattern relations;
* context;
* topology;
* block structure;
* calling relationships;
* output behavior.

In GTDO, Structural Recognition precedes responsible grouping.

---

## Structural Evidence

Direct or indirect information supporting a grouping or dispatch decision.

Structural Evidence may include:

* common attributes;
* common RHS behavior;
* context similarity;
* relationship patterns;
* local continuity;
* invariant properties;
* known task roles;
* historical dispatch outcomes;
* validation results.

Structural Evidence should not be reduced automatically to metric similarity.

---

## Directly Known Grouping Data

Data whose relevance to a grouping decision is explicitly available.

Examples include:

* labels;
* RHS classes;
* known domain identifiers;
* explicit task types;
* direct human annotations.

---

## Indirectly Known Grouping Data

Data whose relevance must be inferred through context, structure, relationships, or derived properties.

Examples include:

* hidden domain membership;
* generated context;
* behavioral similarity;
* shared structural roles;
* common computational outcomes.

GTDO explicitly supports grouping from indirect evidence.

---

## Structural Similarity

Similarity defined by relationships, roles, transformations, responsibilities, or preserved structure.

Structural similarity may exist even when raw metric similarity is weak.

---

## Metric Similarity

Similarity measured by distance, angle, overlap, correlation, or another numerical proximity measure.

Metric similarity may support GTDO but should not override decisive structural distinctions.

---

## Structural Significance

The degree to which a proposed grouping corresponds to a meaningful, stable, and useful computational distinction.

Structural Significance may consider:

* separation strength;
* group stability;
* output improvement;
* responsibility clarity;
* training benefit;
* validation gain;
* generality preservation.

---

## Grouping Significance

The evidence that a proposed division creates useful organizational structure rather than artificial fragmentation.

Weak Grouping Significance may justify:

```text
No Split
```

---

## Assignment Confidence

The confidence that a particular sample, block, or context belongs to a selected group or responsibility.

Assignment Confidence is different from Grouping Significance.

A grouping may be globally significant while some individual assignments remain uncertain.

---

# 5. Segmentation, Grouping, and Assignment

## Segmentation

The division of data into regions, sections, chunks, intervals, or blocks.

Segmentation primarily answers:

> Where should the data be divided?

Segmentation may preserve continuity or locality.

It does not necessarily assign computational responsibility.

---

## Grouping

The organization of samples, blocks, or structures according to a shared criterion.

Grouping may be contiguous or non-contiguous.

In GTDO, grouping should be connected to a goal and a computational interpretation.

---

## Assignment

The act of associating a sample, block, context, task, or responsibility with a group or computational unit.

Assignment may be:

* exclusive;
* multiple;
* conditional;
* deferred;
* hierarchical;
* confidence-weighted.

---

## Data Partition

A subdivision of a dataset.

A Data Partition may be created for storage, sampling, testing, or administration.

A Data Partition becomes a GTDO organization only when it is connected to a Goal Function and computational responsibility.

---

## Data Segmentation versus Dispatch

The canonical distinction is:

```text
Segmentation
    =
Where should data be divided?

Dispatch
    =
Who should take computational responsibility?
```

Segmentation creates boundaries.

Dispatch creates responsibility assignments.

---

## Point-to-Group Assignment

A grouping mode in which individual samples may be assigned to a common group without requiring physical, temporal, textual, or spatial continuity.

Example:

```text
Sample 1  ─┐
Sample 8   ├──→ Group A
Sample 23  ┤
Sample 41 ─┘
```

The samples may be widely separated in the original dataset.

Two-Way CCC is a canonical GTDO algorithm for Point-to-Group Assignment.

---

## Point-to-Block Grouping

A grouping mode in which assigned data must preserve continuity, adjacency, order, or regional coherence.

Example:

```text
Ordered Data Stream
    ↓
[ Block A ][ Block B ][ Block C ]
```

Variable-Size Blocks Indexing and Searching is a canonical GTDO algorithm for Point-to-Block Grouping.

---

## Continuity Constraint

A requirement that members of a group occupy a connected or ordered region.

Continuity may be:

* textual;
* temporal;
* spatial;
* sequential;
* structural;
* graph-based.

---

## Non-Contiguous Group

A group whose members do not occupy one continuous region in the source data.

Non-contiguous grouping is central to distinguishing dispatch from segmentation.

---

## Variable-Size Block

A contiguous or ordered data region whose length is not fixed in advance.

A Variable-Size Block may represent:

* a context;
* an event sequence;
* a code section;
* a semantic region;
* a local training unit;
* a temporal interval.

---

## Variable-Size Blocks Indexing and Searching

A structural method for indexing, recognizing, and searching variable-length contiguous regions.

Within GTDO, it serves as the primary algorithmic foundation for Point-to-Block Grouping.

---

# 6. CCC Terms

## Common Concept Core

**Abbreviation:** CCC

A structural representation of common concepts, attributes, relationships, or invariants shared by a set of instances.

CCC can support:

* recognition;
* grouping;
* matching;
* validation;
* generation;
* dispatch.

Within GTDO, CCC may act as a Grouping Engine and responsibility-recognition mechanism.

---

## Two-Way CCC

A structural process that discovers or applies two opposing, complementary, or distinguishing Common Concept Cores.

Within GTDO, Two-Way CCC supports binary or two-direction Point-to-Group Assignment.

General output:

```text
Input Group
    ↓
Two-Way CCC
    ↓
Group A
Group B
Boundary Set
Optional Discard Set
```

---

## Recursive Two-Way CCC

The repeated application of Two-Way CCC to a broad group or Boundary Set.

General form:

```text
Boundary Set
    ↓
Additional Context or Revised Goal
    ↓
Two-Way CCC
    ↓
Refined Groups + New Boundary Set
```

Recursive Two-Way CCC must use explicit stopping criteria.

---

## Two-Way CCC Dispatch

The use of Two-Way CCC not merely to identify structural cores, but to assign samples or computational responsibilities to two primary groups.

---

## CCC-Based Dispatch

Dispatch based on compatibility with one or more CCC structures.

CCC-Based Dispatch may be performed during:

* offline training organization;
* online task routing;
* validation;
* fallback selection.

---

## Multi-Trigger Matching

A dispatch situation in which an input may match multiple structural trigger points, CCCs, responsibilities, or candidate units.

Multi-Trigger Matching may require:

* ranking;
* confidence aggregation;
* shared dispatch;
* path selection;
* fallback.

---

## N-Comparisons-to-One Comparison

A proposed optimization direction in which multiple distances, matches, or trigger comparisons are unified into one effective comparison.

Its purpose is to reduce online dispatch cost when many potential trigger points exist.

---

# 7. Boundary Terms

## Boundary Set

A set of samples, blocks, contexts, or responsibilities that cannot be assigned confidently to dominant groups.

A Boundary Set may contain:

* weak-evidence cases;
* mixed-domain cases;
* transitional cases;
* emerging domains;
* noise;
* invalid data;
* multi-responsibility cases.

A Boundary Set is a first-class computational object.

It is not automatically discarded.

---

## Leftover Data

An informal term for data not assigned to dominant groups.

In formal GTDO writing, `Boundary Set` is preferred because `Leftover Data` may incorrectly imply low value or processing failure.

---

## Noise Boundary

Boundary data that is corrupted, irrelevant, malformed, duplicated, or structurally invalid.

A Noise Boundary may justify controlled discard.

---

## Weak-Evidence Boundary

Data that may belong to a group but lacks sufficient evidence for confident assignment.

Possible responses include:

* additional context;
* deferred assignment;
* recursive CCC;
* fallback;
* human review.

---

## Mixed-Domain Boundary

Data legitimately associated with more than one domain or responsibility.

Mixed-Domain Boundary data may require:

* multi-path dispatch;
* shared units;
* cross-domain units;
* Boundary Brain Units.

---

## Transitional Boundary

Data lying between established groups, stages, domains, or structural states.

A Transitional Boundary may be important for migration, evolution, or cross-domain reasoning.

---

## Emerging-Domain Boundary

A recurring unresolved set that may represent a new domain or computational responsibility.

An Emerging-Domain Boundary may eventually be promoted to:

* a new group;
* a new branch;
* a new Brain Unit;
* a new Call Path.

---

## Boundary Resolution

The controlled process for determining how a Boundary Set should be handled.

Boundary Resolution options may include:

```text
Recursive Grouping
Boundary Unit
General Fallback
Pre-Grouping Fallback
Multi-Path Dispatch
Deferred Assignment
Human Review
Controlled Discard
```

---

## Boundary Evolution

The change of a Boundary Set over time.

Boundary Evolution may involve:

* shrinking through improved recognition;
* becoming a new group;
* becoming a Brain Unit;
* merging with an existing group;
* being reclassified as noise;
* becoming a shared responsibility.

---

## Boundary Brain Unit

A computational unit designed to handle mixed, transitional, cross-domain, weakly separated, or unresolved cases.

A Boundary Brain Unit is not necessarily inferior to specialist units.

It may provide valuable cross-domain intelligence.

---

## Discard Set

Data explicitly rejected from further organization or training.

Discard should be controlled by clear criteria such as:

* invalidity;
* corruption;
* duplication;
* irrelevance;
* harmful contamination;
* negligible computational value.

Uncertainty alone should not automatically cause discard.

---

## Deferred Set

Data retained for later organization because current evidence, context, or computational value is insufficient.

---

## Multi-Path Set

Data assigned to more than one candidate computational path.

A Multi-Path Set may be processed by:

* parallel units;
* staged units;
* voting;
* validation;
* fusion;
* fallback comparison.

---

# 8. Dispatch Terms

## Dispatch

The process of assigning data, context, tasks, computational responsibility, or runtime work to an appropriate computational structure.

Canonical definition:

> Dispatch is the organization process that assigns computational responsibility to appropriate computational structures according to a Goal Function.

Dispatch may occur:

* before training;
* during training;
* during inference;
* during runtime coordination;
* during optimization;
* during fallback.

---

## Training-Time Dispatch

Dispatch used to organize training data and assign future computational responsibility.

Training-Time Dispatch may determine which unit should be trained on which data.

---

## Runtime Dispatch

Dispatch performed during actual system operation.

General form:

```text
Input
+ Context
+ Goal
+ Runtime State
+ Available Units
        ↓
Runtime Dispatch
        ↓
Selected Call Path
```

---

## Dispatch Decision

The result of evaluating a Goal Function, structural evidence, context, confidence, and system state.

A Dispatch Decision may be:

* single-group;
* multi-group;
* boundary;
* fallback;
* discard;
* deferred;
* hierarchical.

---

## Dispatch Rule

A rule specifying how inputs, contexts, or responsibilities are mapped to computational units or paths.

Dispatch Rules may be:

* static;
* learned;
* structural;
* probabilistic;
* hierarchical;
* context-dependent;
* runtime-adaptive.

---

## Dispatch Policy

A coordinated set of Dispatch Rules, thresholds, priorities, fallback conditions, and conflict-resolution procedures.

---

## Dispatch Confidence

The confidence that a dispatch decision selects an appropriate computational responsibility or unit.

Low Dispatch Confidence may activate:

* fallback;
* multi-path processing;
* Boundary Units;
* human review;
* deferred organization.

---

## Dispatch Stability

The degree to which dispatch decisions remain consistent under small changes in input, context, data distribution, or system state.

---

## Dispatch Drift

A gradual change in dispatch behavior caused by:

* data evolution;
* context evolution;
* model updates;
* changed goals;
* altered unit capabilities;
* feedback loops.

Dispatch Drift may require reorganization.

---

## Dispatch Conflict

A situation in which multiple units or responsibilities compete for the same input without a clear priority.

---

## Dispatch Latency

The time or computational cost required to determine a dispatch destination.

---

## Fallback Dispatch

Dispatch to a general, safe, previous, or alternative computational unit when primary specialized dispatch is uncertain or unsuccessful.

---

## Multi-Path Dispatch

Dispatch to multiple computational units or Call Paths.

Multi-Path Dispatch may support:

* comparison;
* cooperation;
* validation;
* voting;
* fusion;
* uncertainty management.

---

# 9. Responsibility Terms

## Computational Responsibility

A task, capability, recognition role, transformation, validation duty, control function, or coordination obligation assigned to a computational unit.

Examples include:

* produce a target output;
* answer a domain-specific question;
* verify another unit;
* retrieve evidence;
* simulate an outcome;
* handle a boundary case;
* control a process;
* coordinate multiple units.

Computational Responsibility is a first-class GTDO concept.

---

## Responsibility Candidate

A possible computational responsibility inferred from an organized data group.

A Responsibility Candidate becomes formal only after validation and architectural assignment.

---

## Responsibility Assignment

The process of associating a responsibility with a computational unit, group, path, or organization.

---

## Responsibility Boundary

The limit of a computational unit's intended role.

A clear Responsibility Boundary supports:

* local training;
* local validation;
* failure isolation;
* versioning;
* controlled dispatch.

---

## Responsibility Decomposition

The division of a broad responsibility into narrower sub-responsibilities.

Example:

```text
Engineering
    ↓
Software Engineering
    ↓
Compiler Engineering
    ↓
Optimization
```

Responsibility Decomposition may create a Dispatch Tree.

---

## Shared Responsibility

A responsibility performed jointly or redundantly by multiple computational units.

---

## Boundary Responsibility

A responsibility specifically associated with uncertain, mixed, or transitional cases.

---

## Fallback Responsibility

The responsibility of handling cases not safely processed by specialized units.

---

## Validation Responsibility

The responsibility of evaluating, checking, comparing, or certifying another computation.

---

## Coordination Responsibility

The responsibility of selecting, sequencing, combining, or supervising other computational units.

---

## Computational Responsibility Graph

A graph representing relationships among computational responsibilities.

Possible edges include:

* parent–child;
* dependency;
* shared responsibility;
* validation;
* fallback;
* coordination;
* conflict;
* replacement.

A Computational Responsibility Graph may precede the construction of an executable Dispatch Graph.

---

# 10. Computational Unit Terms

## Computational Unit

Any bounded computational structure capable of accepting responsibility.

A Computational Unit may be:

* a model;
* a Brain Unit;
* a function;
* an algorithm;
* a tool;
* a database;
* a retrieval system;
* a simulator;
* an agent;
* a human expert;
* a hybrid organization.

---

## Brain Unit

A computational unit with a bounded or recognizable AI responsibility that can be trained, invoked, evaluated, versioned, and improved with some degree of independence.

A Brain Unit need not correspond to a biologically inspired structure.

It is an engineering abstraction.

---

## LLM Brain Unit

A Brain Unit implemented using an LLM or LLM-derived structure.

An LLM Brain Unit may be:

* a specialized model;
* a fine-tuned model;
* an adapter;
* a prompt-conditioned unit;
* a shared model with a bounded responsibility;
* a retrieval-enhanced unit.

---

## Domain Brain Unit

A Brain Unit responsible for a knowledge or application domain.

Examples:

* law;
* medicine;
* physics;
* software engineering.

---

## Task Brain Unit

A Brain Unit responsible for a task family.

Examples:

* summarization;
* diagnosis;
* planning;
* translation;
* verification.

---

## Context Brain Unit

A Brain Unit specialized for a particular context family or operational condition.

---

## Validation Brain Unit

A Brain Unit responsible for verifying, comparing, scoring, or certifying outputs.

---

## Coordination Brain Unit

A Brain Unit responsible for dispatch, sequencing, arbitration, or organization among other units.

---

## General Brain Unit

A broadly capable computational unit used for general processing or fallback.

---

## Fallback Brain Unit

A computational unit activated when specialized dispatch fails, lacks confidence, or encounters unsupported input.

---

## Shared Brain Unit

A Brain Unit used by multiple branches or Call Paths.

Shared Brain Units require careful update control because local optimization may affect multiple responsibilities.

---

## Specialized Computational Unit

A unit optimized for a narrow responsibility, domain, context, or task.

---

## Heterogeneous Computational Unit

A computational unit drawn from a different computational paradigm than neighboring units.

Examples include:

* LLM plus symbolic solver;
* world model plus planner;
* retrieval system plus human expert;
* simulator plus controller.

---

## Human Computational Unit

A human participant represented as an explicit responsibility-bearing node within a Hybrid AI organization.

Human Computational Units may perform:

* approval;
* review;
* expert judgment;
* exception handling;
* policy decisions;
* creative contribution.

---

## Hybrid Computational Organization

An organized system containing multiple types of computational units.

A Hybrid Computational Organization may include AI models, algorithms, tools, software services, and humans.

---

# 11. Tree, Graph, and Calling Terms

## Dispatch Tree

A hierarchical structure of dispatch decisions and computational responsibilities.

Each branch represents increasing specialization or responsibility decomposition.

Example:

```text
General Dispatcher
├── Engineering
│   ├── Software
│   └── Control
└── Science
    ├── Physics
    └── Biology
```

---

## Dispatch Branch

A branch of a Dispatch Tree representing one sequence of responsibility choices.

---

## Dispatch Node

A decision point or computational unit within a Dispatch Tree or Dispatch Graph.

---

## Dispatch Edge

A relationship indicating possible dispatch from one node to another.

---

## Dispatch Graph

A generalized dispatch structure that permits:

* shared units;
* multiple parents;
* converging paths;
* cross-domain calls;
* validation edges;
* fallback edges.

---

## Hybrid Computation Dispatch Graph

A Dispatch Graph containing heterogeneous computational units.

---

## Directed Acyclic Dispatch Graph

A Dispatch Graph without cycles.

It is useful when units are shared across branches but recursive runtime calls are not required.

---

## Calling Graph

A graph representing computational calls, dependencies, and execution relationships.

Calling Graphs organize how computation is executed.

---

## Calling Graph Node

A callable computational element within a Calling Graph.

It may be a function, service, Brain Unit, tool, or human review node.

---

## Call Path

An ordered sequence of dispatch decisions or computational-unit invocations used to process a task.

A Call Path may be:

* root-to-leaf;
* root-to-node;
* internal;
* multi-domain;
* fallback;
* validation-oriented.

---

## Call Path Segment

A contiguous portion of a Call Path.

Examples include:

* path prefix;
* path suffix;
* internal sequence;
* shared subpath;
* single unit.

---

## Call Path Prefix

The initial section of a Call Path.

---

## Call Path Suffix

The final section of a Call Path.

---

## Shared Call Path Segment

A Call Path Segment used by multiple complete Call Paths.

---

## Fallback Path

A Call Path used when a primary path cannot process a case safely or confidently.

---

## Validation Path

A Call Path dedicated to checking or certifying another path's result.

---

## Path Selection

The process of selecting a Call Path according to input, context, goal, confidence, and runtime state.

---

## Path Inventory

A catalog of available Call Paths and their responsibilities, dependencies, versions, and validation status.

---

## Path Attribution

The identification of which Call Path or Call Path Segment contributed to an outcome, error, reward, or failure.

---

# 12. Optimization Terms

## Structural Scope

A bounded part of the computational organization selected for analysis, training, validation, or modification.

Possible Structural Scopes include:

```text
Whole System
Dispatch Graph
Subgraph
Call Path
Call Path Segment
Computational Unit
Operator
Dispatch Rule
```

---

## Optimization Scope

The Structural Scope selected for an optimization operation.

---

## Local Optimization

Optimization restricted to a specific valid Structural Scope.

Local Optimization may target:

* one Brain Unit;
* one Call Path;
* one Call Path Segment;
* one dispatch rule;
* one shared subgraph;
* one adapter;
* one boundary policy.

---

## Whole-Model Optimization

Optimization applied broadly across a single model.

GTDO does not reject Whole-Model Optimization, but it does not treat it as the only available scope.

---

## Call-Path Optimization

Optimization applied to a selected Call Path.

---

## Call-Path-Segment Optimization

Optimization applied to a selected Call Path Segment.

---

## Call-Path Reinforcement Learning

**Abbreviation:** CPRL

A proposed reinforcement-learning approach in which reward or error signals are attributed to a responsible Call Path or Call Path Segment.

General process:

```text
Outcome
    ↓
Reward / Error
    ↓
Path Attribution
    ↓
Scope Selection
    ↓
Local Update
    ↓
Path Validation
```

CPRL is a proposed GTDO extension and should be described as such until experimentally validated.

---

## Focused Reinforcement Learning

Reinforcement learning limited to a structurally selected part of the system.

---

## Reward Propagation

The distribution of a reward or error signal to responsible computational units, paths, or dispatch rules.

---

## Reward-to-Path Attribution

The process of identifying which Call Path should receive an optimization signal.

---

## Selective Freezing

Preventing selected units or parameters from changing during an optimization operation.

---

## Shared-Unit Protection

Controls preventing an update to a shared unit from unintentionally damaging unrelated Call Paths.

---

## Local Fine-Tuning

Fine-tuning applied to a local Structural Scope.

---

## Local Retraining

Retraining one computational unit, path, or subgraph without retraining the entire organization.

---

## Local Validation

Validation restricted to the modified Structural Scope and its dependencies.

---

## Global Validation

Validation of the whole system after a local or global change.

---

## Local Versioning

Independent version management for a computational unit, Call Path, rule, or subgraph.

---

## Local Rollback

Reversion of one local Structural Scope to a previous stable version.

---

## Failure Isolation

The containment of a failure within a bounded Structural Scope.

---

## Cross-Path Interference

Unintended impact of an update on other Call Paths.

---

## Catastrophic Forgetting

Loss of previously learned capability caused by later training.

GTDO seeks to reduce this risk through structural specialization, selective freezing, and local optimization.

---

# 13. Context Terms

## Context

Information that changes the interpretation, grouping, responsibility, or dispatch of an input.

Context may be explicit or generated.

---

## Extra Context

Additional information associated with an LHS input.

Example:

```text
lhs words
    →
lhs extra-context words
```

Extra Context may improve grouping and dispatch quality.

---

## Offline Context

Context available before runtime.

Examples include:

* neighboring data;
* metadata;
* document structure;
* source relationships;
* historical results;
* generated summaries;
* known labels;
* training provenance.

---

## Online Context

Context available during runtime.

Examples include:

* current task;
* user intent;
* previous calls;
* runtime state;
* available units;
* confidence;
* resource constraints;
* environmental conditions.

---

## Generated Context

Context produced automatically by a model, algorithm, structural recognizer, or runtime process.

Generated Context must be validated because incorrect context can distort grouping and dispatch.

---

## Context Enrichment

The addition of useful contextual information to improve organization or dispatch.

---

## Context Generator

A computational unit responsible for producing context.

---

## Context-Sensitive Dispatch

Dispatch whose result may change when context changes, even if the nominal input remains the same.

General form:

```text
Input + Context
        ↓
Dispatch
```

---

## Context Drift

A change in the contextual environment that affects grouping or dispatch behavior.

---

# 14. Fallback Terms

## Fallback

A controlled alternative used when a primary assignment, unit, or path is unavailable, uncertain, or unsuccessful.

---

## General Fallback

Fallback to a broadly capable computational unit.

---

## Pre-Grouping Fallback

Fallback to a model or system trained on the original data before GTDO grouping.

This preserves broad coverage when specialization fails.

---

## Previous-Version Fallback

Fallback to a prior stable system, unit, or path version.

---

## Human Fallback

Escalation to a human expert, reviewer, or decision-maker.

---

## Fallback Policy

A set of conditions and priorities controlling fallback behavior.

---

## Fallback Trigger

A condition that activates fallback.

Examples include:

* low confidence;
* unavailable unit;
* validation failure;
* unsupported context;
* excessive latency;
* detected risk.

---

## Fallback Coverage

The range of cases that can be handled by fallback structures.

---

# 15. Runtime and Evolution Terms

## Runtime Organization

The organization of computational units, responsibilities, contexts, and calls during system operation.

---

## Runtime State

The current operational condition of a system.

Runtime State may include:

* active tasks;
* available resources;
* current paths;
* model versions;
* system load;
* confidence;
* failure status.

---

## Runtime Computational Responsibility

A computational responsibility assigned dynamically during runtime.

---

## Runtime Call Path

The actual sequence of units invoked during runtime.

---

## Runtime Structural Optimization

Optimization of runtime dispatch structures, paths, or responsibilities.

---

## Organizational Evolution

Controlled change in the computational organization.

Organizational Evolution may involve:

* adding a unit;
* removing a unit;
* splitting a responsibility;
* merging branches;
* promoting a Boundary Set;
* replacing a path;
* revising fallback;
* changing dispatch rules.

---

## Local Evolution

Organizational Evolution restricted to a local Structural Scope.

---

## Self-Organizing Hybrid AI

A Hybrid AI system capable of proposing or performing changes to its own computational organization.

Self-organization must remain subject to validation, constraints, and rollback.

---

## Computational Organization Lifecycle

The lifecycle of a unit, path, or responsibility:

```text
Proposed
    ↓
Trained
    ↓
Validated
    ↓
Released
    ↓
Observed
    ↓
Updated / Replaced / Rolled Back / Retired
```

---

## Dispatch-Training Feedback Loop

A loop in which runtime dispatch outcomes improve future training organization.

```text
Training Organization
        ↓
Runtime Dispatch
        ↓
Observed Outcomes
        ↓
Organization Revision
        ↓
Improved Training
```

---

# 16. Control Engineering Terms

## Control Engineering Architecture

An architecture that exposes measurable states, decision conditions, thresholds, feedback, failure modes, and recovery procedures.

GTDO should be implemented as a control-engineering framework rather than an informal routing metaphor.

---

## Control Variable

A variable that can be adjusted to influence organization.

Examples include:

* significance threshold;
* confidence threshold;
* recursion depth;
* fallback priority;
* group size;
* path selection;
* training schedule.

---

## Observed Variable

A measured property used to evaluate or control GTDO.

Examples include:

* output quality;
* assignment stability;
* boundary size;
* latency;
* fallback frequency;
* dispatch accuracy;
* interference.

---

## Threshold

A value or condition controlling a decision.

---

## Grouping Threshold

A threshold controlling whether grouping is significant enough to proceed.

---

## Dispatch Threshold

A threshold controlling whether a dispatch assignment is confident enough.

---

## Recursion Stopping Condition

A condition that terminates recursive grouping.

Possible conditions include:

* weak significance;
* small group size;
* unstable membership;
* low expected benefit;
* excessive cost;
* maximum depth.

---

## Release Gate

A validation condition that must be satisfied before a unit, path, or organization is released.

---

## Rollback Point

A preserved stable state to which a local or global system may return.

---

## Failure Mode

A known way in which grouping, dispatch, training, or runtime organization may fail.

---

## Recovery Policy

A defined procedure for responding to a failure.

---

# 17. Validation Terms

## Validation

The process of evaluating whether a GTDO structure, decision, or update satisfies its intended goal.

---

## Sample-Level Validation

Validation of individual assignments.

---

## Group-Level Validation

Validation of group coherence, value, and responsibility.

---

## Block-Level Validation

Validation of a contiguous grouped region.

---

## Unit-Level Validation

Validation of a computational unit.

---

## Path-Level Validation

Validation of a Call Path.

---

## Graph-Level Validation

Validation of a Dispatch Graph or Calling Graph.

---

## System-Level Validation

Validation of the full Hybrid AI organization.

---

## Assignment Stability

The degree to which sample assignments remain consistent under small perturbations or repeated evaluation.

---

## Group Coherence

The degree to which members of a group share a meaningful responsibility or structure.

---

## Coverage

The proportion or range of valid cases handled by the system.

---

## General Capability Preservation

The degree to which specialization and local optimization preserve broad system capability.

---

## Rollback Success

The ability to restore a prior stable state after an unsuccessful update.

---

## Validation Scope

The Structural Scope over which validation is applied.

---

# 18. Organization Operators

## Organization Operator

A reusable operation that transforms computational organization.

---

## Goal Definition Operator

Defines or updates the Goal Function.

---

## Recognition Operator

Identifies relevant structure.

---

## Group Operator

Creates a group according to a Goal Function.

---

## Point Assignment Operator

Assigns a non-contiguous sample to a group.

---

## Block Grouping Operator

Creates a contiguous variable-size block.

---

## Boundary Assignment Operator

Assigns unresolved data to a Boundary Set.

---

## Dispatch Operator

Assigns computational responsibility.

---

## Split Operator

Divides a group, responsibility, unit, or branch.

---

## Merge Operator

Combines groups, responsibilities, units, or branches.

---

## Promote Operator

Promotes a Boundary Set or candidate responsibility to a formal group or computational unit.

---

## Freeze Operator

Prevents a Structural Scope from being modified.

---

## Replace Operator

Replaces one unit, path, rule, or subgraph with another.

---

## Validate Operator

Evaluates a Structural Scope.

---

## Rollback Operator

Restores a previous stable state.

---

## Retire Operator

Removes an obsolete computational unit or responsibility from active service.

---

## Operator Economy

The principle that a small set of reusable operators should provide broad organizational capability.

---

# 19. Related Framework Terms

## Structural Runtime AI

**Abbreviation:** SRAI

A framework centered on structural recognition, structural operators, Runtime Invariants, runtime organization, and runtime intelligence.

GTDO extends computation organization into training-data organization and capability formation.

SRAI extends structural organization into runtime intelligence.

---

## Function Tunnel

**Abbreviation:** FT

A structured path through which values, events, states, or computational responsibilities are transformed while preserving relevant relationships.

---

## Runtime Invariant

**Abbreviation:** RI

A structural property preserved across admissible runtime variation or transformation.

Runtime Invariants may support GTDO recognition, grouping, dispatch, and validation.

---

## Runtime Invariant Algebra

**Abbreviation:** RIA

A framework for discovering, preserving, transforming, and organizing Runtime Invariants.

---

## Calling Graph

A graph of callable computational structures and execution dependencies.

GTDO organizes computational responsibility.

Calling Graphs organize computational execution.

---

## Hybrid AI

An AI system combining multiple computational paradigms, models, tools, agents, control structures, or human participants.

GTDO provides an organization layer for Hybrid AI.

---

## Mixture of Experts

**Abbreviation:** MoE

A model architecture that activates selected expert components.

MoE is related to GTDO through expert selection, but GTDO has a broader scope.

GTDO additionally addresses:

* training-data organization;
* computational responsibility;
* heterogeneous units;
* Boundary Sets;
* fallback;
* Call Paths;
* local evolution;
* general computation organization.

---

## Retrieval-Augmented Generation

**Abbreviation:** RAG

A method that retrieves external information to support generation.

Within GTDO, retrieval may be one computational unit or Call Path Segment.

---

## Agent

A computational unit capable of pursuing goals, selecting actions, using tools, or coordinating tasks.

Agents may be nodes within a GTDO Dispatch Graph.

---

## Human–AI Organization

A computational organization in which humans and AI systems hold explicit, complementary responsibilities.

---

# 20. Distinctions That Must Remain Clear

## Grouping versus Clustering

Clustering may discover statistical groups without an explicit computational goal.

GTDO Grouping is controlled by a Goal Function and connected to computational responsibility.

---

## Segmentation versus Organization

Segmentation divides data.

Organization assigns responsibility and constructs a computation architecture.

---

## Dispatch versus Routing

Routing often refers to movement toward a destination.

GTDO Dispatch includes responsibility assignment, fallback, context, validation, and organizational semantics.

---

## Group versus Computational Unit

A group is a data organization.

A Computational Unit is a responsibility-bearing capability.

A group may support a unit, but the two are not identical.

---

## Dispatch Tree versus Calling Graph

A Dispatch Tree represents hierarchical responsibility selection.

A Calling Graph represents computational execution relationships.

A Dispatch Tree may become or generate a Calling Graph.

---

## Call Path versus Data Path

A Call Path is a sequence of computational responsibilities or unit invocations.

A Data Path describes movement of data.

The two may overlap but are not equivalent.

---

## Boundary Set versus Discard Set

Boundary data is unresolved or mixed.

Discard data is intentionally rejected.

Boundary does not imply worthlessness.

---

## Low Confidence versus Noise

Low confidence means insufficient certainty.

Noise means low structural or computational value.

They must not be treated as equivalent.

---

## Specialization versus Fragmentation

Specialization creates useful bounded responsibility.

Fragmentation creates excessive disconnected parts without sufficient benefit.

---

## Local Optimization versus Isolated Optimization

Local Optimization uses a bounded scope while preserving system dependencies.

Isolated Optimization ignores those dependencies.

---

## General Computation Organization versus AGI

General Computation Organization refers to broad applicability across computational types.

It does not assert or require AGI.

---

# 21. Preferred Repository Usage

The following terms should be preferred in formal GTDO writing.

| Prefer                            | Avoid or Qualify                              |
| --------------------------------- | --------------------------------------------- |
| Boundary Set                      | Leftover Data                                 |
| Computational Responsibility      | Topic Label only                              |
| Dispatch                          | Simple Routing                                |
| AI Computation Organization       | LLM Organization when the claim is general    |
| Computational Unit                | Model when non-model units are included       |
| Point-to-Group Assignment         | Segmentation for non-contiguous grouping      |
| Point-to-Block Grouping           | Fixed Chunking                                |
| Call Path                         | Branch when execution meaning matters         |
| Local Structural Scope            | Arbitrary partial tuning                      |
| Controlled Discard                | Automatic rejection                           |
| General Fallback Unit             | Miscellaneous Model                           |
| Weak Separation                   | Failed Split                                  |
| No-Split Decision                 | Algorithm Failure                             |
| Hybrid Computation Dispatch Graph | LLM Tree when heterogeneous units are present |

---

# 22. Canonical One-Sentence Definitions

For concise use in README files, figure captions, and indexes:

### GTDO

Goal-Oriented Training Data Organization organizes training data according to goals and future computational responsibilities.

### Goal Function

A Goal Function defines the organizational distinction that GTDO is intended to create.

### Computational Responsibility

Computational Responsibility is the bounded task, capability, validation role, or control duty assigned to a computational unit.

### Dispatch

Dispatch assigns computational responsibility to an appropriate computational structure.

### Segmentation

Segmentation divides data into regions but does not by itself assign computational responsibility.

### Point-to-Group Assignment

Point-to-Group Assignment groups non-contiguous samples according to structural or goal-based compatibility.

### Point-to-Block Grouping

Point-to-Block Grouping organizes contiguous or ordered variable-size regions.

### Boundary Set

A Boundary Set contains unresolved, mixed, transitional, or weakly separated cases.

### Computational Unit

A Computational Unit is any model, function, algorithm, tool, agent, database, or human node capable of accepting computational responsibility.

### Brain Unit

A Brain Unit is a bounded AI computational unit that can be trained, invoked, evaluated, and evolved with some independence.

### Dispatch Tree

A Dispatch Tree hierarchically organizes computational responsibilities and unit selection.

### Dispatch Graph

A Dispatch Graph generalizes a Dispatch Tree to support shared, converging, cross-domain, or fallback relationships.

### Call Path

A Call Path is an ordered sequence of dispatch decisions or computational-unit invocations.

### Call Path Segment

A Call Path Segment is a contiguous subsection of a Call Path and may serve as a local optimization scope.

### Fallback

Fallback provides an alternative computational route when primary dispatch is uncertain or unsuccessful.

### Local Optimization

Local Optimization modifies the smallest structurally valid scope sufficient to achieve an intended improvement.

### Call-Path Reinforcement Learning

Call-Path Reinforcement Learning applies reward-driven optimization to a responsible Call Path or Call Path Segment.

### AI Computation Organization

AI Computation Organization structures computational responsibilities, units, calls, paths, and evolution across heterogeneous AI systems.

---

# 23. Canonical GTDO Statements

The following statements may be reused consistently across the repository.

> GTDO organizes data to reveal computational responsibility.

> Segmentation creates boundaries; dispatch assigns computational responsibility.

> Training groups are not merely data partitions; they are candidates for computational responsibility.

> Boundary Sets represent unresolved computation organization rather than automatically worthless data.

> Weak separation must not be forced into an artificial split.

> LLM Brain Units are an important application of GTDO, not its theoretical boundary.

> GTDO organizes computational responsibility; Calling Graphs organize computational execution.

> A Dispatch Tree of computational units can be interpreted as a Calling Graph of Brain Units.

> In an organized Hybrid AI system, the optimization target may be a Call Path rather than the whole model.

> The smallest structurally valid optimization scope should be preferred.

> Specialization must preserve general capability and fallback coverage.

> GTDO begins with training data but develops toward general AI computation organization.

---

# 24. Abbreviation Index

| Abbreviation | Full Term                                |
| ------------ | ---------------------------------------- |
| GTDO         | Goal-Oriented Training Data Organization |
| AI           | Artificial Intelligence                  |
| LLM          | Large Language Model                     |
| CCC          | Common Concept Core                      |
| RI           | Runtime Invariant                        |
| RIA          | Runtime Invariant Algebra                |
| FT           | Function Tunnel                          |
| SRAI         | Structural Runtime AI                    |
| MoE          | Mixture of Experts                       |
| RAG          | Retrieval-Augmented Generation           |
| CPRL         | Call-Path Reinforcement Learning         |
| RHS          | Right-Hand Side                          |
| LHS          | Left-Hand Side                           |

---

# 25. Closing Definition

GTDO may be summarized as follows:

> Goal-Oriented Training Data Organization is a framework that uses goals, structural recognition, grouping, boundary resolution, and dispatch to transform training data into explicit computational responsibilities, computational units, Call Paths, and controllable Hybrid AI organizations.

Its central transformation is:

```text
Training Data
    ↓
Goal-Oriented Structure
    ↓
Computational Responsibility
    ↓
Dispatchable Capability
    ↓
Call Path
    ↓
Controllable Computation Organization
```

The purpose of this glossary is to keep that transformation conceptually stable as the repository expands.
