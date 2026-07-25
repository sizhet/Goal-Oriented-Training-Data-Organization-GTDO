# GTDO-003 — Goal Functions and RHS-Driven Training Organization

## How Output Goals Transform Training Data into Computational Responsibilities

---

## Abstract

Goal-Oriented Training Data Organization begins with a principle that is simple but structurally decisive:

> Training data should not be grouped merely because samples are similar. It should be organized according to the computational distinction that the future system is intended to learn, perform, or control.

The mechanism that expresses this distinction is the **Goal Function**.

In one important GTDO case, the Goal Function is derived from the right-hand side of a training relationship:

```text
LHS Input
    →
RHS Output
```

The RHS may identify an output token, output family, state transition, action, class, structural result, or computational responsibility. By using this output-side information, directly or indirectly, GTDO can reorganize LHS training samples into groups that support distinct future computational capabilities.

This article develops the concept of RHS-driven organization, distinguishes Goal Functions from labels and loss functions, defines their possible inputs and outputs, and explains how they govern grouping, Boundary Sets, discard decisions, fallback, recursion, and future Dispatch Trees.

---

#### Fig-101-GTDO-Structural-Overview.png

![Fig-101-GTDO-Structural-Overview.png](../figures/Fig-101-GTDO-Structural-Overview.png)

---

# 1. Why GTDO Begins with a Goal

A dataset can be divided in many different ways.

The same samples may be grouped according to:

* topic;
* source;
* language;
* length;
* date;
* embedding similarity;
* output type;
* task;
* risk;
* computational cost;
* runtime role.

None of these groupings is automatically correct.

A grouping becomes meaningful only relative to an intended purpose.

GTDO therefore begins with:

```text
Goal
    ↓
Organization
```

rather than:

```text
Similarity
    ↓
Cluster
```

The Goal Function determines which differences matter and which similarities may be ignored.

It converts raw variation into an organizational decision.

---

# 2. Canonical Training Relation

A simplified training relation may be written as:

```text
{ LHS words }
        →
{ RHS word or words }
```

With additional context:

```text
{ LHS words }
+
{ LHS extra-context words }
        →
{ RHS word or words }
```

In a more general form:

```text
Input
+
Context
+
Known Structure
        →
Target Outcome
```

The RHS may represent:

* the next token;
* a sequence of tokens;
* a label;
* an action;
* a state;
* a transformation result;
* a decision;
* a success or failure condition;
* a structural category;
* a responsibility indicator.

GTDO uses this relationship to ask:

> Which distinctions among LHS inputs are relevant to the RHS outcome or to the future computation responsible for producing it?

---

# 3. RHS-Driven Training Organization

RHS-driven organization uses output-side evidence to organize input-side data.

The basic form is:

```text
LHS Training Samples
        +
RHS Outcomes
        +
Goal Function
        ↓
Goal-Oriented Training Groups
```

For a simple binary case:

```text
RHS Goal
├── Group 0
├── Group 1
├── Boundary
└── Optional Discard
```

The resulting LHS data may then be organized as:

```text
LHS samples associated with RHS Group 0
        ↓
Training Group 0

LHS samples associated with RHS Group 1
        ↓
Training Group 1
```

The significance of this operation is not merely that two datasets are created.

The deeper result is that two candidate computational responsibilities become visible.

---

# 4. The Goal Function

A Goal Function is a function, rule, structural criterion, or control policy that maps available evidence to an organizational outcome.

A general GTDO form is:

```text
Goal Function(
    LHS Data,
    RHS Data,
    Context,
    Structural Evidence,
    Runtime or Engineering Constraints
)
        ↓
Organization Decision
```

Possible decisions include:

```text
Assign to Group A
Assign to Group B
Assign to Boundary Set
Assign to Multiple Groups
Assign to Fallback
Discard
Defer
Retain Original Group
Create New Group
```

The Goal Function therefore governs more than classification.

It governs the structure of the future computational organization.

---

# 5. Goal Function Is Not Merely a Label

A label is one possible input to a Goal Function.

But a Goal Function may be broader.

A label may state:

```text
Sample → Class A
```

A Goal Function may additionally ask:

* Is this distinction structurally meaningful?
* Is the separation sufficiently significant?
* Should this sample belong to multiple groups?
* Does continuity need to be preserved?
* Should the sample remain in a Boundary Set?
* Would separation improve future computation?
* Is the resulting group large enough to justify a computational unit?
* Should a general fallback retain coverage?

Therefore:

> A label describes an outcome; a Goal Function controls an organization.

---

# 6. Goal Function Is Not the Same as a Loss Function

A loss function measures optimization error.

A Goal Function defines the intended organization.

The distinction is:

```text
Goal Function
    ↓
What organization should exist?

Loss Function
    ↓
How far is training from a target?
```

A Goal Function may determine:

* which samples are trained together;
* which unit owns a responsibility;
* which path receives an update;
* which data remain unresolved;
* which model acts as fallback.

A loss function may then optimize the selected unit or scope.

Thus, the preferred sequence is:

```text
Goal Function
        ↓
Organization
        ↓
Optimization Scope
        ↓
Loss Function
        ↓
Training
```

Without this distinction, optimization may begin before computational responsibility is understood.

---

# 7. Direct RHS Goals

The simplest GTDO case uses directly known RHS information.

Examples include:

* binary labels;
* success versus failure;
* safe versus unsafe;
* positive versus negative outcome;
* action A versus action B;
* output family 0 versus output family 1.

Example:

```text
LHS Context A
    →
RHS 0

LHS Context B
    →
RHS 1
```

The Goal Function can directly organize the LHS examples according to the RHS distinction.

This is especially useful when the desired future system must distinguish the same responsibilities during runtime.

---

# 8. Indirect RHS Goals

In many systems, the relevant RHS organization is not directly labeled.

It may need to be inferred from:

* output structure;
* downstream consequences;
* repeated behavior;
* success patterns;
* validation outcomes;
* context;
* human review;
* Runtime Invariants;
* shared CCCs.

For example, several different RHS outputs may belong to one broader responsibility.

```text
RHS outputs:
compile
optimize
inline
vectorize
        ↓
Compiler Optimization Responsibility
```

The grouping evidence is indirect because no single RHS label names the responsibility.

GTDO may use structural recognition to discover the common output-side organization.

---

# 9. Binary Goal Functions

The simplest Goal Function separates data into two dominant groups.

```text
Input Data
    ↓
Binary Goal Function
    ↓
Group 0 / Group 1
```

An engineering-quality binary Goal Function should usually permit additional outcomes:

```text
Group 0
Group 1
Boundary Set
Discard Set
No-Split Decision
```

This prevents the algorithm from forcing every sample into a false binary structure.

The binary case is important because it maps naturally to Two-Way CCC.

However, binary organization is only the starting point.

---

# 10. Multi-Group Goal Functions

A Goal Function may produce more than two groups.

Example:

```text
Input
    ↓
Goal Function
    ↓
Reasoning
Retrieval
Generation
Validation
Control
Boundary
Fallback
```

Multi-group organization may be implemented through:

* direct multi-class assignment;
* recursive binary decomposition;
* hierarchical Goal Functions;
* staged dispatch;
* graph-based responsibility assignment.

The selected method should preserve structural meaning.

---

# 11. Hierarchical Goal Functions

Many computational responsibilities are naturally hierarchical.

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

A hierarchical Goal Function may operate in stages:

```text
Stage 1:
Engineering or Non-Engineering?

Stage 2:
Software or Control?

Stage 3:
Compiler or Application?

Stage 4:
Optimization or Verification?
```

The result is a Dispatch Tree.

Each stage narrows computational responsibility.

This hierarchical structure can later become a runtime Call Path.

---

# 12. Context-Dependent Goal Functions

The same input may deserve different organization under different contexts.

Example:

```text
Input:
"bank"

Context A:
finance
        ↓
Financial Responsibility

Context B:
river
        ↓
Geographic Responsibility
```

The general relation becomes:

```text
LHS
+
RHS
+
Context
+
Goal
        ↓
Organization Decision
```

Context may be:

* offline;
* online;
* supplied;
* retrieved;
* generated;
* inferred;
* historical.

A context-dependent Goal Function is therefore more general than a static label map.

---

# 13. Offline Context

Offline context is available before runtime.

Examples include:

* neighboring words;
* document section;
* metadata;
* source identity;
* historical outcome;
* known domain;
* generated structural summary;
* previous training relationship;
* Calling Graph position.

Offline context can improve organization by revealing distinctions invisible in isolated samples.

---

# 14. Online Context

Online context becomes available during actual use.

Examples include:

* current user intention;
* active task;
* available computational units;
* previous Call Path;
* runtime state;
* system load;
* safety condition;
* confidence;
* latency constraint.

Online context may alter dispatch even when training-time grouping remains unchanged.

This creates a two-stage relationship:

```text
Offline GTDO
    ↓
Forms responsibilities and units

Online GTDO-informed Dispatch
    ↓
Selects responsibility and Call Path
```

---

# 15. Generated Context

Context can also be generated.

A system may produce:

* summaries;
* inferred domains;
* structural attributes;
* candidate explanations;
* causal hints;
* Runtime Invariant descriptions;
* Calling Graph relations.

Generated context may improve grouping, especially for indirectly known data.

However, generated context introduces risk.

If the generated context is incorrect, the Goal Function may organize data around a false distinction.

Therefore, generated context should be:

* traceable;
* confidence-scored;
* independently validated when important;
* separated from directly observed evidence.

---

# 16. Goal Functions and Point-to-Group Assignment

For Point-to-Group Assignment, the Goal Function determines group membership without requiring continuity.

```text
Distributed Samples
        ↓
Goal Function
        ↓
Group A / Group B / Boundary
```

The relevant evidence may include:

* RHS behavior;
* CCC compatibility;
* domain responsibility;
* structural features;
* contextual role.

Two-Way CCC can serve as the grouping engine.

The Goal Function determines what the two CCC directions are intended to represent.

---

# 17. Goal Functions and Point-to-Block Grouping

For Point-to-Block Grouping, the Goal Function must include a continuity requirement.

```text
Ordered Data
        ↓
Goal Function
        +
Continuity Constraint
        ↓
Variable-Size Blocks
```

The Goal Function determines:

* what kind of region is sought;
* what starts the block;
* what preserves membership;
* what ends the block;
* whether nested blocks are allowed;
* which computational responsibility owns the block.

Variable-Size Blocks Indexing and Searching provides the structural mechanism.

---

# 18. Goal Functions and Boundary Sets

Boundary Sets arise when the Goal Function cannot produce a confident assignment.

This may happen because:

* evidence is weak;
* the sample is mixed;
* the distinction is unstable;
* the context is incomplete;
* the data belongs to multiple responsibilities;
* the proposed split lacks significance.

The Goal Function should explicitly define boundary policy.

```text
Low Confidence
    ↓
Boundary Set

Conflicting Responsibilities
    ↓
Multi-Path Set

Invalid Data
    ↓
Discard Set

Insufficient Evidence
    ↓
Deferred Set
```

Boundary behavior should not be left to an accidental implementation default.

---

# 19. Goal Functions and the No-Split Decision

A Goal Function may determine that no meaningful division exists.

```text
Candidate Split
        ↓
Significance Evaluation
        ↓
Insufficient Structural Gain
        ↓
No Split
```

This is a successful organizational outcome.

It indicates that the system has refused to create a false computational distinction.

No-Split may be preferred when:

* groups are unstable;
* validation gain is negligible;
* separation damages generality;
* one group is too small;
* computational cost exceeds expected benefit;
* the Goal Function is poorly specified.

---

# 20. Goal Functions and Recursive Organization

A broad group or Boundary Set may be processed again under a revised Goal Function.

```text
Boundary Set
        ↓
Additional Context
        ↓
Revised Goal Function
        ↓
Secondary Grouping
```

The revised Goal Function may differ from the original in:

* target distinction;
* context;
* resolution;
* confidence threshold;
* continuity requirement;
* computational objective.

Recursive organization should not merely repeat the same failed split.

It should introduce new evidence or a more appropriate goal.

---

# 21. Goal Functions and Discard

Discard must be an explicit organizational decision.

A Goal Function may identify data as:

* corrupted;
* irrelevant;
* duplicated;
* harmful;
* structurally invalid;
* outside the intended scope.

Discard should not be used merely because assignment confidence is low.

The distinction is:

```text
Uncertain
    →
Boundary or Defer

Invalid or Low-Value
    →
Discard
```

This preserves potentially valuable emerging or cross-domain data.

---

# 22. Goal Functions and Fallback

A Goal Function should define when specialized organization is insufficient.

Fallback options include:

* general model;
* pre-grouping model;
* Boundary Brain Unit;
* human review;
* multi-path evaluation;
* previous stable version.

Example:

```text
Primary Dispatch Confidence
        ↓
Below Threshold
        ↓
General Fallback Unit
```

Fallback should be designed with the Goal Function, not appended after failure.

---

# 23. Goal Functions and Computational Responsibility

The ultimate output of a Goal Function is not merely a group identifier.

It is a responsibility interpretation.

Example:

```text
Group 0
    =
Generate candidate answer

Group 1
    =
Validate candidate answer

Boundary
    =
Require joint processing
```

This converts grouping into architecture.

A stable GTDO design should document:

* group meaning;
* responsibility;
* intended computational unit;
* validation criteria;
* fallback relation;
* runtime dispatch rule.

---

# 24. Goal Functions and Computational Units

Once a responsibility is stable, the system can decide how it should be implemented.

Possible implementations include:

* separate model;
* Brain Unit;
* adapter;
* retrieval collection;
* symbolic rule;
* software function;
* planner;
* validator;
* controller;
* human review node.

The Goal Function defines the need.

The implementation architecture defines the mechanism.

This separation preserves GTDO generality beyond LLMs.

---

# 25. Goal Functions and Dispatch Trees

A sequence of Goal Functions can form a Dispatch Tree.

```text
Goal 1
    ↓
Domain

Goal 2
    ↓
Subdomain

Goal 3
    ↓
Task

Goal 4
    ↓
Operator
```

Example:

```text
General
├── Engineering
│   ├── Software
│   │   ├── Compiler
│   │   │   ├── Optimization
│   │   │   └── Verification
```

Each branch corresponds to a chain of responsibility decisions.

At runtime, the same chain may become a Call Path.

---

# 26. Goal Functions and Call-Path Optimization

A Goal Function may also define the target of optimization.

Instead of:

```text
Improve the entire model
```

the Goal Function may specify:

```text
Improve compiler optimization outputs
without changing unrelated capabilities
```

The organization then identifies:

```text
Responsible Call Path
        ↓
Valid Call Path Segment
        ↓
Local Training Scope
```

Thus, Goal Functions govern not only data grouping, but also later system evolution.

---

# 27. Static and Adaptive Goal Functions

## Static Goal Function

Defined before organization and kept fixed.

Useful when:

* responsibilities are stable;
* labels are reliable;
* safety requires predictable boundaries;
* reproducibility is important.

## Adaptive Goal Function

Updated using feedback, runtime evidence, or changing system needs.

Useful when:

* domains evolve;
* Boundary Sets grow;
* dispatch drift appears;
* new computational units emerge;
* goals change.

Adaptive Goal Functions require:

* versioning;
* validation;
* rollback;
* change approval;
* comparison against previous organization.

---

# 28. Single-Goal and Multi-Goal Organization

A GTDO system may have multiple goals.

Examples include:

* output quality;
* safety;
* latency;
* cost;
* specialization;
* general coverage;
* interpretability.

These goals may conflict.

For example:

```text
More Specialization
        ↔
More General Coverage
```

A multi-goal function may use:

* priority ordering;
* constraints;
* weighted objectives;
* Pareto selection;
* hierarchical decisions;
* human approval.

GTDO should make these tradeoffs explicit.

---

# 29. Hard Constraints and Soft Objectives

A Goal Function may include hard constraints.

Examples:

* legal prohibition;
* safety rule;
* continuity requirement;
* mandatory human review;
* maximum latency.

It may also include soft objectives.

Examples:

* improve quality;
* reduce cost;
* reduce Boundary Set size;
* increase specialization;
* reduce interference.

The distinction is important:

```text
Hard Constraint
    =
Must be satisfied

Soft Objective
    =
Should be improved
```

---

# 30. Goal Function Validation

A Goal Function must itself be validated.

Questions include:

* Does it create meaningful groups?
* Are assignments stable?
* Does output quality improve?
* Does the Boundary Set become manageable?
* Is general capability preserved?
* Are responsibilities understandable?
* Does the architecture reduce training or runtime cost?
* Can the resulting units be verified independently?
* Does fallback remain adequate?

A poorly designed Goal Function can produce a structurally elegant but operationally harmful organization.

---

# 31. Goal Function Drift

A Goal Function may become outdated.

Causes include:

* changed data;
* changed user goals;
* new computational units;
* new risks;
* new domains;
* changed runtime conditions;
* improved structural recognition.

Goal Function Drift may appear as:

* increasing Boundary Sets;
* unstable assignments;
* frequent fallback;
* path overload;
* declining output quality;
* duplicated responsibilities.

Drift should trigger review, not silent adaptation.

---

# 32. Goal Function Versioning

Each major Goal Function should have:

* identifier;
* definition;
* inputs;
* outputs;
* thresholds;
* constraints;
* validation results;
* activation date;
* superseded version;
* rollback reference.

This makes changes to computational organization traceable.

---

# 33. Minimal Goal Function Specification

A practical GTDO Goal Function specification should include:

```text
Goal Name

Purpose

Input Evidence

Target Distinction

Allowed Outputs

Boundary Policy

Discard Policy

Fallback Policy

Continuity Requirement

Significance Threshold

Confidence Threshold

Stopping Conditions

Validation Measures

Version
```

This specification turns an abstract research idea into an engineering artifact.

---

# 34. Example: Binary RHS Dispatch

Suppose training data contains:

```text
{ LHS words } → { RHS 0 or 1 }
```

The Goal Function may be:

```text
Goal:
Separate LHS structures that produce RHS 0
from LHS structures that produce RHS 1.
```

Allowed outputs:

```text
Group 0
Group 1
Boundary Set
Discard Set
No Split
```

Processing:

```text
Training Samples
        ↓
RHS Goal Function
        ↓
Two-Way CCC
        ↓
Group 0 / Group 1 / Boundary
```

The resulting groups may train two specialized units, one shared model with separate adapters, or another responsibility-bearing architecture.

---

# 35. Example: Heterogeneous Computational Dispatch

Suppose the output goal is not merely a word prediction.

The desired computation may be:

```text
Question
    ↓
Retrieve Evidence
    ↓
Perform Symbolic Check
    ↓
Generate Explanation
```

The Goal Function may organize training data into:

```text
Retrieval Responsibility
Symbolic Validation Responsibility
Language Generation Responsibility
Boundary or Human Review Responsibility
```

The resulting computational units may include:

* retrieval engine;
* symbolic solver;
* LLM;
* human expert.

This demonstrates why GTDO is a general computation-organization framework.

---

# 36. Example: Continuity-Preserving Organization

Suppose a long sequence contains variable-length operational episodes.

The Goal Function may seek blocks associated with:

* normal operation;
* transition;
* failure;
* recovery.

```text
Time Series
        ↓
Goal Function
+
Continuity Constraint
        ↓
Variable-Size Blocks
```

Each block may then support a different:

* predictor;
* controller;
* validator;
* recovery policy.

This is GTDO outside the LLM domain.

---

# 37. Example: Call-Path Improvement Goal

Suppose a Hybrid AI system performs poorly on compiler optimization.

The Goal Function may be:

```text
Improve compiler optimization quality
while preserving unrelated branches.
```

The organization process identifies:

```text
Engineering
    ↓
Software
    ↓
Compiler
    ↓
Optimization
```

The optimization target becomes:

* one Brain Unit;
* one Call Path Segment;
* one dispatch rule;
* one specialized training group.

The Goal Function therefore controls both the original training organization and later local improvement.

---

# 38. Engineering Properties of a Good Goal Function

A useful GTDO Goal Function should be:

## Explicit

Its intended distinction should be understandable.

## Structurally Relevant

Its outputs should correspond to meaningful responsibilities.

## Measurable

Success and failure should be testable.

## Boundary-Aware

It should allow unresolved outcomes.

## Fallback-Aware

It should preserve coverage.

## Context-Aware

It should use relevant context where necessary.

## Stable

Small irrelevant changes should not cause arbitrary reassignment.

## Revisable

It should support controlled evolution.

## Implementation-Neutral

It should not assume every responsibility requires an independent model.

---

# 39. Common Failure Modes

## Goal-Free Clustering

Groups are created without a clear computational purpose.

## Label Equivalence

Labels are assumed to define complete responsibilities.

## Forced Binary Split

All data are assigned to two groups even when separation is weak.

## Boundary Collapse

Boundary cases are incorrectly discarded or forced into dominant groups.

## Context Neglect

Relevant context is excluded.

## Model-First Bias

The Goal Function is designed around a predetermined model rather than the responsibility.

## Goal Overload

One Goal Function attempts to optimize too many conflicting objectives.

## Goal Drift Without Versioning

The organization changes without traceability.

## No Fallback

Specialized organization is created without preserving broad coverage.

---

# 40. From RHS Goal to General Organization

RHS-driven organization provides a practical entry point.

But GTDO develops beyond direct RHS grouping.

The progression is:

```text
RHS Output Grouping
        ↓
Training Responsibility
        ↓
Computational Responsibility
        ↓
Computational Unit
        ↓
Dispatch Tree
        ↓
Call Path
        ↓
General AI Computation Organization
```

The RHS is therefore not the final destination.

It is an observable starting point for discovering and organizing future computation.

---

# 41. Canonical GTDO Formulation

The general GTDO organization relation may be summarized as:

```text
Data
+
Context
+
Known Outputs
+
Structural Evidence
+
Engineering Constraints
        ↓
Goal Function
        ↓
Group / Boundary / Discard / Fallback / Multi-Path / No-Split
        ↓
Computational Responsibility
        ↓
Computational Unit or Call Path
```

This formulation captures the transition from training examples to computational architecture.

---

# 42. Long-Term Significance

As AI systems become more heterogeneous, the Goal Function may become as important as the model architecture.

It determines:

* which capabilities should exist;
* where responsibilities should be located;
* how data should support them;
* how boundaries should be handled;
* how units should cooperate;
* where optimization should occur;
* how the system should evolve.

The deeper GTDO proposition is therefore:

> The organization of AI computation begins with the explicit organization of goals.

---

# Key Takeaways

* GTDO begins with a Goal Function rather than unguided similarity.
* RHS-driven organization uses output-side evidence to organize input-side training data.
* A Goal Function is broader than a label and different from a loss function.
* Goal Functions may be binary, multi-group, hierarchical, contextual, or adaptive.
* A valid Goal Function must support Boundary, Discard, Fallback, Deferred, Multi-Path, and No-Split outcomes where appropriate.
* Point-to-Group Assignment and Point-to-Block Grouping require different structural constraints.
* Goal Functions transform data groups into computational responsibilities.
* Computational responsibility may be implemented by models, functions, tools, planners, retrieval systems, controllers, agents, or human experts.
* Hierarchical Goal Functions can construct Dispatch Trees and future Call Paths.
* Goal Functions may also define local optimization scopes.
* Generated context can improve organization but must be validated.
* The RHS is an important starting signal, but the long-term object of GTDO is general AI computation organization.

---

## Further Reading

### GTDO Foundations

* GTDO-001 — *Why Goal-Oriented Training Data Organization*
* GTDO-002 — *From Data Segmentation to AI Computation Organization*
* GTDO-004 — *Dispatch Is Not Segmentation*
* GTDO-005 — *Training Data Organization as Computation Organization*
* GTDO-006 — *Computational Responsibility*

### GTDO Algorithms

* GTDO-101 — *Two Modes of Goal-Oriented Grouping*
* GTDO-102 — *Point-to-Group Assignment by Two-Way CCC*
* GTDO-103 — *Point-to-Block Grouping by Variable-Size Blocks*
* GTDO-104 — *Recursive Two-Way CCC*
* GTDO-105 — *Boundary Resolution*

### GTDO Organization and Optimization

* GTDO-201 — *From Training Groups to Computational Units*
* GTDO-301 — *Dispatch Trees as Calling Graphs*
* GTDO-304 — *Call-Path Reinforcement Learning*

### Related Structural Work

* **Structural Runtime AI (SRAI)**
* **Structural Recognition above Metric Similarity (SRMS)**
* **Function Tunnel and Runtime Invariant Algebra (FTRIA)**
