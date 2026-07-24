# GTDO-301 — Dispatch Trees as Calling Graphs

## From Hierarchical Responsibility Assignment to Executable Call-Path Organization

---

## Abstract

A Dispatch Tree is commonly interpreted as a hierarchical routing structure.

An input enters at the root, passes through a sequence of decisions, and eventually reaches a specialized Computational Unit.

Goal-Oriented Training Data Organization gives this structure a deeper interpretation.

Each branch of a Dispatch Tree represents a progressive narrowing of Computational Responsibility. Once the selected nodes become callable computational structures, the branch becomes an executable **Call Path**.

The Dispatch Tree is therefore not merely a classifier, taxonomy, router, or training-data hierarchy.

It is a potential **Calling Graph of Computational Units**.

The transformation is:

```text
Goal-Oriented Training Groups
        ↓
Computational Responsibilities
        ↓
Dispatch Tree
        ↓
Callable Computational Units
        ↓
Calling Graph
        ↓
Runtime Call Paths
```

This interpretation has major consequences.

Training data can be organized according to the paths that future computation will execute. Runtime results can be attributed to particular branches, nodes, and Call Path Segments. Reinforcement, fine-tuning, validation, versioning, rollback, and failure isolation can then operate on structurally bounded parts of the system instead of indiscriminately updating one monolithic model.

This article defines the relationship among Dispatch Trees, Calling Graphs, Call Paths, and Call Path Segments. It explains the transition from tree to graph, the semantics of nodes and edges, shared Computational Units, fallback and validation paths, path-specific training, and the general applicability of the framework beyond LLM Brain Units.

---

# 1. The Central Observation

Consider a Dispatch Tree of Computational Units:

```text
General Dispatcher
        ↓
Engineering
        ↓
Software
        ↓
Compiler
        ↓
Optimization
```

This structure may initially be interpreted as a sequence of classifications:

```text
Is the task engineering-related?

Is it software-related?

Is it compiler-related?

Is optimization required?
```

But if the nodes correspond to active computational responsibilities and callable units, the same structure becomes:

```text
General Dispatcher
        calls
Engineering Unit
        calls
Software Unit
        calls
Compiler Unit
        calls
Optimization Unit
```

The dispatch branch has become a Call Path.

This is the foundational observation of GTDO Part IV.

---

# 2. Canonical Proposition

The central proposition is:

> **A Dispatch Tree of Computational Units is a Calling Graph whose branches define responsibility-aware Call Paths.**

More precisely:

```text
Dispatch Tree
    defines which responsibility applies.

Calling Graph
    defines how that responsibility executes.

Call Path
    is the selected executable realization
    of the dispatch decision.
```

The structures are related but not identical.

A Dispatch Tree becomes a Calling Graph when its organizational nodes and edges acquire executable semantics.

---

# 3. From Training Groups to Call Paths

GTDO begins with organized training evidence.

```text
Training Data
        ↓
Goal-Oriented Groups
        ↓
Computational Responsibilities
        ↓
Computational Units
        ↓
Dispatch Structure
```

The next transformation is:

```text
Dispatch Structure
        ↓
Execution Relationships
        ↓
Calling Graph
```

The full chain is:

```text
Training Evidence
        ↓
Responsibility Formation
        ↓
Computational Unit Formation
        ↓
Dispatch Tree or Graph
        ↓
Call Paths
        ↓
Runtime Computation
```

Training organization and runtime execution are therefore structurally connected.

---

# 4. Dispatch Tree

Within GTDO:

> **A Dispatch Tree is a hierarchical organization of Goal Functions, Computational Responsibilities, dispatch decisions, and Computational Units.**

A Dispatch Tree may represent:

* responsibility decomposition;
* specialization;
* context narrowing;
* unit selection;
* fallback inheritance;
* training-group hierarchy;
* validation structure.

Example:

```text
General Computation
├── Engineering
│   ├── Software
│   │   ├── Compiler
│   │   │   ├── Optimization
│   │   │   └── Verification
│   │   └── Application Development
│   └── Control Engineering
└── Science
    ├── Physics
    └── Biology
```

This is not merely a subject taxonomy.

Each node may correspond to a responsibility-bearing computational structure.

---

# 5. Calling Graph

Within GTDO:

> **A Calling Graph is a graph of callable Computational Units and the typed execution relationships among them.**

A Calling Graph identifies:

* which unit may call another;
* under which conditions;
* which inputs and contexts are transferred;
* which output is expected;
* which validation follows;
* which fallback is available.

The graph may contain:

* models;
* Brain Units;
* functions;
* retrieval systems;
* symbolic operators;
* controllers;
* agents;
* human review nodes.

---

# 6. Dispatch Tree versus Calling Graph

A Dispatch Tree and a Calling Graph answer different questions.

```text
Dispatch Tree:
Which responsibility and specialization path applies?

Calling Graph:
Which computational calls execute that responsibility?
```

The Dispatch Tree is primarily organizational.

The Calling Graph is primarily executable.

A mature GTDO architecture connects them explicitly.

---

# 7. The Tree-to-Graph Transformation

The transformation may be represented as:

```text
Responsibility Node
        ↓
Assign Computational Owner
        ↓
Callable Node

Responsibility Relation
        ↓
Assign Execution Semantics
        ↓
Call Edge
```

After all relevant nodes and edges are mapped:

```text
Dispatch Tree
        ↓
Executable Calling Graph
```

This transformation should preserve responsibility semantics.

---

# 8. Node Semantics

A Dispatch Tree node may represent different organizational objects.

Possible node types include:

* Goal-Function node;
* responsibility node;
* dispatcher node;
* Computational Unit;
* Boundary processor;
* validator;
* fallback unit;
* human approval node;
* coordination unit.

The node type must be explicit.

Otherwise, the tree may mix conceptual categories and executable components without control.

---

# 9. Responsibility Node

A Responsibility Node represents work that must be performed.

Example:

```text
Compiler Optimization Responsibility
```

It does not yet specify whether the work is performed by:

* an LLM Brain Unit;
* an optimization algorithm;
* a symbolic engine;
* a human expert;
* a multi-unit Call Path.

Responsibility remains logical.

---

# 10. Computational-Unit Node

A Computational-Unit Node identifies a concrete implementation.

Example:

```text
LLVM Optimization Brain Unit v1.3
```

It should expose:

* input contract;
* context contract;
* output contract;
* confidence;
* validation hook;
* fallback hook;
* version.

---

# 11. Dispatcher Node

A Dispatcher Node evaluates:

* input;
* Goal Function;
* context;
* responsibility candidates;
* confidence;
* runtime state;
* available units.

It may select:

* one child;
* several children;
* Boundary handling;
* parent fallback;
* human review;
* No Dispatch.

The dispatcher itself holds a Coordination Responsibility.

---

# 12. Boundary Node

A Boundary Node handles unresolved or multi-responsibility cases.

Possible operations include:

* request more context;
* invoke several branches;
* call a Boundary Brain Unit;
* use general fallback;
* escalate to a human;
* create a future Responsibility Candidate.

Boundary handling must be represented explicitly in the graph.

---

# 13. Validation Node

A Validation Node checks the output of another node or path.

Validation may include:

* factual checking;
* symbolic verification;
* structural validation;
* policy compliance;
* safety review;
* human approval.

A validation node may be shared across several branches.

---

# 14. Fallback Node

A Fallback Node accepts responsibility when the primary specialist or path cannot operate reliably.

Fallback may occur because of:

* low dispatch confidence;
* missing context;
* unit failure;
* unsupported input;
* validation failure;
* version incompatibility.

Fallback is part of the Calling Graph rather than an external patch.

---

# 15. Human Node

A Human Computational Unit may hold:

* primary responsibility;
* approval responsibility;
* arbitration responsibility;
* Boundary Resolution responsibility;
* validation responsibility.

The human should be modeled as an explicit graph node with defined inputs, outputs, and authority.

---

# 16. Edge Semantics

An edge should not merely mean:

```text
Node A is connected to Node B.
```

It should specify the organizational and execution relation.

Possible edge types include:

* specialization;
* delegation;
* call;
* context propagation;
* data transfer;
* validation;
* fallback;
* escalation;
* retry;
* aggregation;
* synchronization.

Typed edges make the graph interpretable and controllable.

---

# 17. Specialization Edge

A Specialization Edge narrows responsibility.

```text
Software Engineering
        ↓
Compiler Engineering
```

It may be used during dispatch before runtime execution begins.

---

# 18. Call Edge

A Call Edge activates another Computational Unit.

```text
Compiler Unit
        calls
Optimization Unit
```

The edge should define:

* input mapping;
* required context;
* expected output;
* timeout;
* failure behavior.

---

# 19. Context-Propagation Edge

A Context-Propagation Edge transfers contextual information.

Example:

```text
Repository Retrieval Unit
        ↓
Retrieved Source Context
        ↓
Compiler Analysis Unit
```

Context provenance should remain visible.

---

# 20. Validation Edge

A Validation Edge connects a producer with a validator.

```text
Optimization Unit
        ↓
Correctness Validator
```

The validation result may:

* approve;
* reject;
* request revision;
* activate fallback;
* escalate.

---

# 21. Fallback Edge

A Fallback Edge identifies an alternate path.

```text
Specialist
        ↓
Low Confidence or Failure
        ↓
Parent Unit or General Unit
```

Fallback edges may be local, hierarchical, or system-wide.

---

# 22. Escalation Edge

An Escalation Edge transfers responsibility to a higher-authority unit.

Example:

```text
AI Risk Analyzer
        ↓
High-Risk Condition
        ↓
Human Approver
```

Escalation is not identical to failure.

It may be required by design.

---

# 23. Aggregation Edge

An Aggregation Edge combines several results.

Example:

```text
Path A ─┐
Path B ─┼──→ Result Aggregator
Path C ─┘
```

The aggregator holds responsibility for:

* comparison;
* voting;
* fusion;
* conflict resolution;
* final output selection.

---

# 24. Dispatch Branch

A Dispatch Branch is a sequence of responsibility decisions from one node toward a more specialized node.

Example:

```text
General
    ↓
Engineering
    ↓
Software
    ↓
Compiler
```

A branch becomes a Call Path when its selected nodes participate in execution.

---

# 25. Call Path

Within GTDO:

> **A Call Path is an ordered sequence of responsibility-bearing Computational Units and typed execution edges activated to fulfill a goal.**

A Call Path may be:

* root-to-leaf;
* root-to-intermediate node;
* internal;
* fallback;
* validation-oriented;
* multi-domain;
* human–AI.

---

# 26. Root-to-Leaf Call Path

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

The leaf provides the narrowest primary responsibility.

Ancestor nodes may still contribute:

* shared context;
* base capability;
* coordination;
* fallback.

---

# 27. Root-to-Intermediate Call Path

Not every task requires the deepest specialist.

Example:

```text
General
    ↓
Engineering
    ↓
Software
```

The Software Unit may handle the task directly.

The valid path depth depends on the Goal Function and dispatch confidence.

---

# 28. Internal Call Path

A Call Path may begin and end inside the graph.

Example:

```text
Compiler Unit
        ↓
Optimization Unit
        ↓
Correctness Validator
```

This internal path may become a local optimization scope.

---

# 29. Composite Call Path

A Composite Call Path combines several distinct responsibilities.

Example:

```text
Retrieval
    ↓
Reasoning
    ↓
Validation
    ↓
Generation
```

The overall responsibility belongs to the path.

Local responsibilities belong to individual nodes.

---

# 30. Multi-Path Computation

Some goals require several Call Paths.

```text
Input
├── Legal Path
├── Financial Path
└── Risk Validation Path
```

The paths may:

* run in parallel;
* exchange context;
* converge;
* vote;
* require human arbitration.

The structure is a graph rather than a single tree branch.

---

# 31. Call Path Segment

Within GTDO:

> **A Call Path Segment is a contiguous sequence of one or more nodes and edges within a Call Path that forms a valid local unit of responsibility, validation, optimization, versioning, or rollback.**

Examples include:

* path prefix;
* path suffix;
* internal sequence;
* shared subpath;
* single unit.

---

# 32. Path Prefix

Example:

```text
General
    ↓
Engineering
    ↓
Software
```

A prefix may define broad context and general responsibility.

---

# 33. Path Suffix

Example:

```text
Compiler
    ↓
Optimization
    ↓
Validation
```

A suffix may define a specialized execution stage.

---

# 34. Internal Segment

Example:

```text
Retrieval
    ↓
Evidence Validation
```

This segment may be shared by several larger paths.

---

# 35. Single-Node Segment

One Computational Unit may be treated as a minimal Call Path Segment when its responsibility and interface are sufficiently bounded.

---

# 36. Shared Call Path Segment

Several Call Paths may use the same segment.

Example:

```text
Compiler Path ──────┐
Control Path ───────┼──→ Optimization → Validation
Planning Path ──────┘
```

The shared segment requires dependency tracking and update protection.

---

# 37. From Tree to Directed Acyclic Graph

A strict tree requires each node to have one parent.

This becomes inefficient when units are reusable.

Example:

```text
Mathematics ─────┐
                 ├──→ Optimization Unit
Software ────────┘
```

The shared node has multiple parents.

The architecture becomes a Directed Acyclic Graph.

This is a natural evolution, not a violation of GTDO.

---

# 38. From Directed Acyclic Graph to General Calling Graph

Some runtime systems may require:

* feedback;
* retry;
* iterative reasoning;
* recursive calls;
* monitoring loops.

These introduce cycles.

The architecture may then become a general Calling Graph.

Cycles should be controlled by:

* stopping conditions;
* budgets;
* state transitions;
* validation;
* timeout;
* rollback.

---

# 39. Why the Dispatch Tree Remains Useful

Even when runtime execution uses a graph, the Dispatch Tree remains valuable as:

* a responsibility hierarchy;
* a training-data organization;
* a reading path;
* a fallback hierarchy;
* a conceptual control structure.

The tree and graph may coexist.

```text
Tree:
Primary responsibility organization

Graph:
Actual cooperative execution
```

---

# 40. Training Groups and Dispatch Nodes

A GTDO Training Group may support one Dispatch Node.

Example:

```text
Compiler-Optimization Training Group
        ↓
Compiler-Optimization Responsibility
        ↓
Compiler-Optimization Node
```

The node retains provenance to the group.

---

# 41. Training Blocks and Path Segments

A Variable-Size Block family may support one Call Path Segment.

Example:

```text
Failure-and-Recovery Training Blocks
        ↓
Diagnosis → Recovery-Control Segment
```

This connects Point-to-Block Grouping with Calling Graph construction.

---

# 42. Recursive Two-Way CCC and Tree Construction

Recursive Two-Way CCC may construct responsibility branches.

```text
Root Group
        ↓
Two-Way CCC
        ↓
A / B
        ↓
Recursive Two-Way CCC
        ↓
A1 / A2 / B1 / B2
```

After unit formation, the responsibility tree becomes a Dispatch Tree.

---

# 43. Boundary Sets and Boundary Paths

Boundary Sets may produce dedicated Call Paths.

Example:

```text
Boundary Detection
        ↓
Context Generator
        ↓
Candidate Specialists
        ↓
Validator
        ↓
General Fallback or Human Review
```

Boundary Resolution becomes an executable organizational subsystem.

---

# 44. General Fallback as the Root Safety Net

The root or broad parent may act as fallback for descendants.

```text
Leaf Specialist
        ↓
Parent Specialist
        ↓
General Root Unit
```

This creates hierarchical fallback.

Specialization does not eliminate general coverage.

---

# 45. Parent Fallback

A child unit may fail back to its parent responsibility.

Example:

```text
LLVM Optimization Unit
        ↓
Compiler Engineering Unit
```

The parent has broader but less specialized capability.

---

# 46. Sibling Fallback

A sibling may serve as fallback when responsibilities are closely related.

This should be used cautiously because sibling responsibilities may not be substitutable.

---

# 47. Cross-Graph Fallback

A path may fall back to a different computational paradigm.

Example:

```text
LLM Reasoning Path
        ↓
Low Confidence
        ↓
Symbolic Solver
```

Fallback may therefore increase heterogeneity.

---

# 48. Validation Paths

Validation may be represented as a separate path.

Example:

```text
Primary Output Path
        ↓
Validation Dispatcher
        ↓
Symbolic Validator
        ↓
Policy Validator
        ↓
Human Approval if Required
```

The validation path may have its own training data and local optimization.

---

# 49. Training-Time Calling Graph

A Calling Graph may also organize training operations.

Example:

```text
Training Group Selector
        ↓
Context Enricher
        ↓
Brain Unit Trainer
        ↓
Validator
        ↓
Version Manager
```

GTDO is therefore relevant to both capability formation and runtime execution.

---

# 50. Runtime Calling Graph

The runtime graph executes task responsibilities.

It may use:

* dynamic context;
* current unit availability;
* latency constraints;
* confidence;
* risk;
* runtime state.

The runtime graph may choose a different path from the nominal training hierarchy when current conditions require it.

---

# 51. Offline–Online Structural Symmetry

GTDO seeks structural correspondence between:

```text
Offline Training Group
        and
Online Dispatch Responsibility
```

and between:

```text
Offline Responsibility Sequence
        and
Online Call Path
```

This symmetry enables:

* data-to-path provenance;
* targeted retraining;
* path-level evaluation;
* responsibility-aware feedback.

---

# 52. Data-to-Path Provenance

A runtime result should ideally be traceable through:

```text
Runtime Output
        ↓
Call Path
        ↓
Computational Units
        ↓
Computational Responsibilities
        ↓
Training Groups or Blocks
        ↓
Source Evidence
```

This creates organizational provenance.

---

# 53. Path Inventory

A GTDO system should maintain a Path Inventory.

A path record may include:

```text
Path ID

Goal

Responsibilities

Ordered Nodes

Typed Edges

Required Context

Fallback Path

Validation Path

Training Evidence

Version

Status
```

The inventory makes the computational organization inspectable.

---

# 54. Path Activation Conditions

A Call Path should define when it applies.

Conditions may include:

* Goal Function;
* context;
* responsibility match;
* risk;
* confidence;
* unit availability;
* resource budget.

---

# 55. Path Completion Conditions

A path completes when:

* required output is produced;
* validation succeeds;
* responsibility contract is fulfilled;
* no unresolved state remains.

Completion is not merely reaching the last node.

---

# 56. Path Failure Conditions

A path may fail because of:

* misdispatch;
* missing context;
* unit failure;
* invalid intermediate output;
* validation failure;
* timeout;
* incompatible versions;
* unsatisfied responsibility.

Failure type should guide fallback and optimization.

---

# 57. Path Confidence

Path Confidence may combine:

* dispatch confidence;
* unit confidence;
* context confidence;
* validation status;
* dependency reliability.

A single confidence number may be insufficient.

The underlying dimensions should remain inspectable.

---

# 58. Path State

A runtime path may be:

```text
Proposed

Activated

Executing

Waiting

Validating

Completed

Failed

Falling Back

Rolled Back
```

Explicit state supports control engineering.

---

# 59. Path Logging

A runtime path log may include:

```text
Path ID

Node Sequence

Versions

Inputs

Contexts

Intermediate Outputs

Confidence

Validation Results

Fallback Events

Outcome

Reward or Error
```

This record supports local diagnosis and learning.

---

# 60. Call Path as an Optimization Target

The major GTDO insight is:

> **In an organized Hybrid AI system, the fundamental optimization target may be the Call Path rather than the whole model.**

The system may optimize:

* path selection;
* one node;
* one edge;
* one path segment;
* one validator;
* one fallback rule;
* one context generator.

This creates explicit Structural Scope.

---

# 61. Why Whole-Model Optimization Is Often Too Broad

A local failure may affect only:

```text
Software
    ↓
Compiler
    ↓
Optimization
```

Updating an entire general model may disturb:

* medicine;
* law;
* writing;
* mathematics;
* unrelated software capabilities.

GTDO allows the responsible path to be isolated.

---

# 62. Path-Specific Training

A Call Path may have a dedicated training set assembled from:

* node-specific groups;
* edge-transition examples;
* complete path examples;
* Boundary cases;
* fallback examples;
* validation failures.

Training can target path-level behavior rather than only independent units.

---

# 63. Edge Training

Some failures occur in handoff rather than inside a node.

Examples include:

* missing context transfer;
* incorrect format;
* premature dispatch;
* wrong validation order.

The edge itself may require training or policy adjustment.

---

# 64. Segment-Specific Training

A repeated weakness may occur in:

```text
Compiler
    ↓
Optimization
    ↓
Validation
```

The segment can be trained and validated as one local system.

This may be more effective than training each node independently.

---

# 65. Call-Path Reinforcement Learning

A proposed Call-Path Reinforcement Learning workflow is:

```text
Observed Outcome
        ↓
Active Call Path
        ↓
Reward or Error Attribution
        ↓
Responsible Node, Edge, or Segment
        ↓
Local Update
        ↓
Path and System Validation
```

The reward follows organizational responsibility rather than spreading blindly through the whole system.

---

# 66. Path Attribution

Path Attribution determines which selected path contributed to the outcome.

This requires accurate runtime records.

It is the first stage of local reinforcement.

---

# 67. Segment Attribution

Segment Attribution narrows the responsible part of the path.

Possible questions include:

* Was the wrong branch selected?
* Did a node fail?
* Was context lost on an edge?
* Did validation fail?
* Should fallback have activated?

The answer determines the optimization target.

---

# 68. Responsibility Attribution

A poor result may arise from an incorrect responsibility definition rather than a weak unit.

Possible outcomes include:

* revise Goal Function;
* revise responsibility boundary;
* merge branches;
* split responsibility;
* create a Boundary path.

GTDO optimization therefore operates above parameter level.

---

# 69. Selective Freezing

During local optimization, unrelated nodes and paths may remain frozen.

This supports:

* stability;
* reduced cost;
* reduced catastrophic forgetting;
* easier validation.

Shared nodes require special protection.

---

# 70. Shared-Node Protection

A shared node may be used by many paths.

Before updating it, the system should identify:

* dependent paths;
* responsibility contracts;
* regression tests;
* alternative local adapters;
* rollback targets.

A local improvement for one path must not silently harm others.

---

# 71. Local Adapter for a Shared Node

Instead of modifying the shared node globally, one path may use a local adapter.

```text
Shared Optimization Unit
        +
Compiler-Specific Adapter
```

This preserves reuse while supporting specialization.

---

# 72. Local Validation

After changing a node, edge, or segment, validate:

* the target path;
* neighboring nodes;
* shared dependencies;
* fallback;
* general root coverage.

---

# 73. Global Validation

A local update may still affect global behavior.

System-level validation should check:

* unrelated paths;
* dispatch distribution;
* graph stability;
* resource cost;
* general capability;
* fallback frequency.

---

# 74. Path Versioning

Each Call Path should have a version.

A Path Version may identify:

* node versions;
* edge-policy versions;
* context-policy version;
* fallback version;
* validation version;
* responsibility version.

A path may change even when no individual model version changes.

---

# 75. Segment Versioning

A shared or critical segment may be versioned independently.

This enables:

* local release;
* local rollback;
* A/B testing;
* controlled migration.

---

# 76. Path Rollback

If a path update fails:

```text
Path v2.1
        ↓
Validation Failure
        ↓
Rollback to Path v2.0
```

Rollback may restore:

* node version;
* edge rule;
* context policy;
* fallback order;
* responsibility mapping.

---

# 77. Branch Rollback

A complete Dispatch Tree branch may be rolled back without changing unrelated branches.

This is a major control advantage over one-model global updates.

---

# 78. Graph Migration

A tree branch may evolve into:

* shared graph node;
* new subgraph;
* heterogeneous Call Path;
* human–AI path.

Migration should preserve responsibility contracts and fallback coverage.

---

# 79. Path Split

A path may split when:

* one segment serves distinct goals;
* runtime behavior diverges;
* risk levels differ;
* local optimization repeatedly conflicts;
* Boundary cases stabilize.

The split should return to Goal Function and responsibility analysis.

---

# 80. Path Merge

Paths may merge when:

* responsibilities overlap;
* node sequences are nearly identical;
* one shared path performs better;
* routing complexity becomes excessive.

Merge supports Operator Economy.

---

# 81. Path Promotion

A frequently used Boundary or fallback path may become a primary specialized path.

This is one form of runtime-driven architectural evolution.

---

# 82. Path Retirement

A path may be retired when:

* responsibility is obsolete;
* usage disappears;
* another path subsumes it;
* cost exceeds value;
* validation remains poor.

Dependent dispatch rules must be updated.

---

# 83. Dispatch-Graph Drift

The graph may drift because of:

* new units;
* changing goals;
* updated context;
* path promotion;
* path retirement;
* new shared nodes.

Drift should be versioned and reviewed.

---

# 84. Path Churn

Path Churn occurs when runtime tasks repeatedly switch among similar paths.

Possible causes include:

* unstable responsibility boundaries;
* poor context;
* threshold sensitivity;
* overlapping units;
* Goal Function drift.

High churn may reduce reliability and efficiency.

---

# 85. Path Load

Some paths may become overloaded.

Possible responses include:

* equivalent replicas;
* caching;
* scheduling;
* responsibility split;
* alternate path;
* improved dispatch index.

Load balancing occurs after responsibility and path selection.

---

# 86. Calling Graph as a Control Surface

The Calling Graph exposes control points:

* dispatch nodes;
* Call Paths;
* path segments;
* context edges;
* validation nodes;
* fallback edges;
* human approvals;
* versions.

These become direct engineering controls for Hybrid AI.

---

# 87. Generality Beyond LLM Brain Units

The framework applies to any responsibility-bearing Computational Unit.

A path may contain:

```text
LLM
        ↓
Retrieval System
        ↓
Symbolic Solver
        ↓
Simulator
        ↓
Controller
        ↓
Human Reviewer
```

The same dispatch and Calling Graph principles apply.

---

# 88. World-Model Example

```text
Goal Interpreter
        ↓
World-State Estimator
        ↓
World Model
        ↓
Planner
        ↓
Action Validator
```

This is a Call Path organized by responsibility.

---

# 89. Software-Engineering Example

```text
Issue Interpreter
        ↓
Repository Retrieval
        ↓
Calling-Graph Analyzer
        ↓
Code-Change Generator
        ↓
Test Validator
        ↓
Human Approval
```

The path can be optimized and versioned locally.

---

# 90. Control-Engineering Example

```text
Sensor Monitor
        ↓
State Estimator
        ↓
Fault Diagnoser
        ↓
Recovery Controller
        ↓
Safety Validator
```

Variable-Size operating blocks may support the nodes and path.

---

# 91. Scientific-Computing Example

```text
Research Goal
        ↓
Data Retriever
        ↓
Structural Analyzer
        ↓
Simulation Engine
        ↓
Result Validator
        ↓
Explanation Unit
```

The graph integrates heterogeneous computational paradigms.

---

# 92. Human–AI Example

```text
AI Evidence Collector
        ↓
AI Risk Analyzer
        ↓
Human Decision Maker
        ↓
AI Execution Monitor
```

The human holds primary decision responsibility.

---

# 93. Dispatch Trees and MoE

Mixture-of-Experts routing selects model experts.

GTDO Dispatch Trees are broader because they may organize:

* heterogeneous units;
* complete Call Paths;
* Boundary handling;
* validation;
* human participation;
* local versioning;
* structural responsibility.

MoE may implement individual nodes or internal dispatch mechanisms.

---

# 94. Dispatch Trees and Agents

Agents may appear as nodes in the Calling Graph.

However, GTDO requires their responsibilities, interfaces, fallback, and validation to remain explicit.

An agent graph without responsibility semantics may be operationally dynamic but organizationally weak.

---

# 95. Dispatch Trees and Function Tunnels

A Call Path may be interpreted as a Function Tunnel when it preserves relevant structural relationships from input to output.

A Call Path Segment may correspond to one FT segment.

This connects GTDO execution with Function Tunnel and Runtime Invariant frameworks.

---

# 96. Dispatch Trees and Runtime Invariants

A Call Path may preserve Runtime Invariants across several units.

Example:

```text
Input RI
        ↓
Transformation Unit
        ↓
Validation Unit
        ↓
Output RI Preserved
```

RI preservation may become a path-level validation responsibility.

---

# 97. Dispatch Trees and SRAI

GTDO forms responsibilities, units, and paths from training organization.

SRAI organizes structural computation at runtime.

The connection is:

```text
GTDO
    forms the computation organization.

SRAI
    operates and evolves the computation organization.
```

Dispatch Trees as Calling Graphs provide a direct bridge.

---

# 98. Minimal Node Record

```text
Node ID

Node Type

Responsibility

Computational Owner

Input Contract

Context Contract

Output Contract

Validation

Fallback

Parent Nodes

Child Nodes

Version

Status
```

---

# 99. Minimal Edge Record

```text
Edge ID

Source Node

Target Node

Edge Type

Activation Condition

Input Mapping

Context Mapping

Expected Output

Failure Policy

Version
```

---

# 100. Minimal Call Path Record

```text
Path ID

Goal Function

Composite Responsibility

Ordered Nodes

Ordered Edges

Required Context

Activation Conditions

Completion Conditions

Validation Path

Fallback Path

Training Groups

Version

Status
```

---

# 101. Minimal Dispatch-Tree Policy

```text
Root Responsibility

Node-Formation Rule

Specialization Rule

Boundary Rule

Fallback Hierarchy

Shared-Node Rule

Tree-to-Graph Rule

Path-Activation Rule

Validation Requirement

Versioning Requirement

Rollback Rule
```

---

# 102. Construction Workflow

```text
Step 1:
Organize training data into responsibility-bearing groups and blocks

Step 2:
Validate Computational Responsibilities

Step 3:
Assign Computational Units

Step 4:
Construct responsibility hierarchy

Step 5:
Define node and edge semantics

Step 6:
Create Dispatch Tree

Step 7:
Identify shared responsibilities and convert tree portions to graph structure

Step 8:
Define Call Paths, validation paths, and fallback paths

Step 9:
Connect paths to training evidence and runtime logging

Step 10:
Validate and release the Calling Graph
```

---

# 103. Runtime Workflow

```text
Step 1:
Interpret input, goal, context, and runtime state

Step 2:
Select applicable responsibility branch

Step 3:
Activate Computational Units

Step 4:
Propagate data and context along typed edges

Step 5:
Validate intermediate and final outputs

Step 6:
Activate fallback or escalation when required

Step 7:
Record the complete Call Path

Step 8:
Use outcome feedback for local optimization and organizational evolution
```

---

# 104. Common Failure Modes

## Taxonomy Without Execution

The Dispatch Tree describes subjects but does not identify callable responsibilities.

## Execution Without Responsibility

Units call one another without clear organizational purpose.

## Untyped Edges

The graph does not distinguish call, validation, fallback, and context relations.

## One Branch Equals One Model

Every branch creates unnecessary model duplication.

## Hidden Shared Units

Cross-branch dependencies are not recorded.

## Missing Boundary Path

Ambiguous cases are forced into ordinary branches.

## Missing General Fallback

Specialization creates coverage gaps.

## Path-Level Blindness

Only individual model outputs are logged, not complete Call Paths.

## Global-Only Optimization

Local path structure exists but is not used for targeted improvement.

## No Rollback

Path or branch updates cannot be reversed independently.

---

# 105. Evaluation Dimensions

Dispatch Trees as Calling Graphs should be evaluated through:

* responsibility clarity;
* node suitability;
* edge correctness;
* path success;
* dispatch accuracy;
* context preservation;
* fallback success;
* validation success;
* path latency;
* shared-node interference;
* local-update effectiveness;
* rollback success;
* general coverage;
* graph complexity;
* Operator Economy.

---

# 106. Comparison Table

| Structure                | Primary Purpose                                      | Main Artifact                  |
| ------------------------ | ---------------------------------------------------- | ------------------------------ |
| Training Group Hierarchy | Organize evidence                                    | Data groups                    |
| Responsibility Tree      | Organize computational roles                         | Logical nodes                  |
| Dispatch Tree            | Select responsibility and specialization             | Dispatch branches              |
| Calling Graph            | Execute computational relationships                  | Callable nodes and typed edges |
| Call Path                | Fulfill one goal through ordered computation         | Runtime path                   |
| Call Path Segment        | Define a local responsibility and optimization scope | Local subpath                  |

---

# 107. Canonical GTDO Statements

> A Dispatch Tree of Computational Units is a potential Calling Graph.

> A Dispatch branch becomes a Call Path when its responsibility-bearing nodes participate in execution.

> Dispatch Trees organize responsibility; Calling Graphs organize execution.

> Nodes and edges must carry explicit organizational semantics.

> Shared units naturally transform trees into graphs.

> Boundary, validation, fallback, and human-review paths are first-class parts of the Calling Graph.

> Training groups and blocks should remain traceable to the runtime paths they support.

> The Call Path, Call Path Segment, node, edge, or responsibility may become the optimization target.

> The smallest structurally valid optimization scope should be preferred.

> The framework applies to heterogeneous AI computation rather than only LLM Brain Units.

---

# 108. Central Transformation

```text
Goal-Oriented Training Groups and Blocks
        ↓
Validated Computational Responsibilities
        ↓
Computational Units
        ↓
Responsibility Hierarchy
        ↓
Dispatch Tree
        ↓
Typed Nodes and Edges
        ↓
Calling Graph
        ↓
Runtime Call Paths
        ↓
Path-Level Validation, Reinforcement,
Versioning, Rollback, and Evolution
```

---

# 109. Long-Term Significance

The interpretation of Dispatch Trees as Calling Graphs changes the optimization object of AI systems.

In a monolithic model, responsibility is largely implicit inside one parameter space.

A local defect may trigger a global update.

In a GTDO-organized system, responsibility is represented explicitly through:

* nodes;
* edges;
* branches;
* paths;
* path segments;
* fallback structures;
* validation structures.

This allows the system to ask:

```text
Which Call Path failed?

Which responsibility was misidentified?

Which node produced the error?

Which edge lost context?

Which validator failed?

Which segment should be retrained?

Which branch should be rolled back?
```

These questions create a control-engineering layer that monolithic model optimization does not naturally expose.

The enduring GTDO proposition is therefore:

> **In a Brain-Unit-based or heterogeneous Hybrid AI system, the primary optimization target need not be the whole model. It may be the responsible Call Path.**

Dispatch Trees as Calling Graphs provide the structural foundation for that transition.

---

# Key Takeaways

* A Dispatch Tree is a hierarchy of Goal Functions, Computational Responsibilities, dispatch decisions, and Computational Units.
* A Calling Graph is the executable graph of responsibility-bearing units and typed relationships.
* A Dispatch Tree becomes a Calling Graph when its nodes and edges acquire execution semantics.
* A selected Dispatch branch becomes a Call Path.
* A Call Path Segment provides a local scope for training, validation, versioning, rollback, and reinforcement.
* Nodes may represent responsibilities, units, dispatchers, validators, Boundary processors, fallback units, coordinators, or humans.
* Edges should distinguish specialization, call, context propagation, validation, fallback, escalation, and aggregation.
* Shared units naturally transform trees into Directed Acyclic Graphs or general Calling Graphs.
* General, parent, sibling, heterogeneous, and human fallback paths may coexist.
* Training Groups and Variable-Size Blocks should remain linked to the runtime paths they support.
* Runtime path logs provide evidence for responsibility, node, edge, and segment attribution.
* Path-specific optimization can reduce cost, interference, and catastrophic forgetting.
* Local updates must protect shared nodes and preserve global fallback coverage.
* GTDO Dispatch Trees apply to LLMs, world models, symbolic systems, software functions, controllers, agents, and Human–AI organizations.
* Dispatch Trees as Calling Graphs form the bridge from training-data organization to executable, controllable, and evolvable Hybrid AI.

---

## Further Reading

### GTDO Foundations and Grouping

* GTDO-005 — *Training Data Organization as Computation Organization*
* GTDO-006 — *Computational Responsibility*
* GTDO-007 — *Dispatch and Organizational Semantics*
* GTDO-009 — *Boundary Sets*
* GTDO-102 — *Point-to-Group Assignment by Two-Way CCC*
* GTDO-103 — *Point-to-Block Grouping by Variable-Size Blocks*
* GTDO-104 — *Recursive Two-Way CCC*

### GTDO Computational Units

* GTDO-201 — *From Training Groups to Computational Units*
* GTDO-202 — *Heterogeneous Computational Units*
* GTDO-203 — *Brain Units*
* GTDO-204 — *Boundary Brain Units*
* GTDO-205 — *General Fallback Units*
* GTDO-206 — *Computational Responsibility Graphs*
* GTDO-207 — *Dispatch Trees*
* GTDO-208 — *Dispatch Graphs*
* GTDO-209 — *Hybrid Computational Organizations*

### Part IV — Call-Path Organization and Optimization

* GTDO-302 — *Call Paths*
* GTDO-303 — *Call-Path Segments*
* GTDO-304 — *Call-Path Reinforcement Learning*
* GTDO-305 — *Local Fine-Tuning*
* GTDO-306 — *Local Validation*
* GTDO-307 — *Local Versioning*
* GTDO-308 — *Local Rollback*
* GTDO-309 — *Structural Scope of Optimization*

### Related Structural Work

* **Calling Graph for AI Coding**
* **Structural Runtime AI (SRAI)**
* **Function Tunnel (FT)**
* **Runtime Invariant Algebra (RIA)**
* **Common Concept Core (CCC)**
