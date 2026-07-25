# GTDO-302 — Call Paths

## The Fundamental Execution Unit of Goal-Oriented AI Computation Organization

---

# Abstract

Traditional AI systems often describe computation as the execution of a model.

GTDO proposes a different abstraction.

The true computational object is frequently **not an individual model**, but the **ordered sequence of computational responsibilities executed to accomplish a goal**.

This ordered sequence is called a **Call Path**.

A Call Path begins when a Goal Function activates a Dispatch Tree and ends when the required Computational Responsibility has been successfully completed, validated, and returned to the requester.

The path may traverse:

* Dispatchers
* Brain Units
* Retrieval Systems
* Symbolic Operators
* Runtime Invariant Processors
* Validation Units
* Boundary Units
* Human Experts
* General Fallback Units

The individual components are important.

However, **the computation emerges from the organization of the entire path rather than from any single node.**

Consequently, GTDO regards the Call Path—not the isolated model—as the primary runtime object for execution, optimization, validation, evolution, and engineering control.

---

#### Fig-103-Runtime-Execution-Flow.png

![Fig-103-Runtime-Execution-Flow.png](../figures/Fig-103-Runtime-Execution-Flow.png)

---

#### Fig-106-Call-Path-Segment-Structure.png

![Fig-106-Call-Path-Segment-Structure.png](../figures/Fig-106-Call-Path-Segment-Structure.png)

---

#### Fig-107-Calling-Graph-vs-Call-Path.png

![Fig-107-Calling-Graph-vs-Call-Path.png](../figures/Fig-107-Calling-Graph-vs-Call-Path.png)

---

# 1. Motivation

Suppose a user asks:

> Optimize this compiler.

A monolithic LLM simply produces tokens.

A Hybrid AI organization may instead execute:

```text
Task Understanding
        ↓
Repository Retrieval
        ↓
Calling Graph Analysis
        ↓
Compiler Optimization
        ↓
Correctness Verification
        ↓
Performance Estimation
        ↓
Human Approval
```

Which object solved the problem?

Not one model.

The entire ordered execution sequence.

That sequence is the Call Path.

---

# 2. Canonical Definition

Within GTDO:

> **A Call Path is the ordered execution sequence of Computational Responsibilities activated to accomplish one Goal Function.**

A Call Path therefore includes:

* responsibility selection;
* computational execution;
* context propagation;
* validation;
* fallback;
* completion.

It is an organizational object rather than merely an execution trace.

---

# 3. Goal-Oriented Nature

Every Call Path begins with a Goal Function.

Without an explicit computational goal, there is no principled reason to select one path over another.

Conceptually:

```text
Goal Function
        ↓
Dispatch
        ↓
Call Path
        ↓
Result
```

The Goal Function gives semantic meaning to the entire execution.

---

# 4. Call Paths versus Pipelines

Pipelines usually describe fixed processing stages.

Call Paths describe **responsibility-aware execution**.

Pipelines answer:

> What stages exist?

Call Paths answer:

> Which responsibilities should execute for this particular goal under this particular context?

A Call Path may therefore change dynamically even when the underlying pipeline remains unchanged.

---

# 5. Call Paths versus Workflows

Workflows organize activities.

Call Paths organize computational responsibilities.

A workflow may include:

* approvals;
* scheduling;
* notifications.

A Call Path specifically describes:

* computational ownership;
* execution order;
* responsibility transfer;
* validation;
* fallback.

---

# 6. Call Paths versus Function Calls

A software call stack records:

```text
Function A
    calls
Function B
```

A GTDO Call Path is broader.

Each node represents an explicit Computational Responsibility rather than simply a software function.

Several software functions may implement one responsibility.

Likewise, one function may participate in several Call Paths.

---

# 7. Call Path Formation

The canonical formation process is:

```text
Training Groups
        ↓
Computational Responsibilities
        ↓
Computational Units
        ↓
Dispatch Tree
        ↓
Selected Branch
        ↓
Call Path
```

Thus, the Call Path is rooted in training organization.

---

# 8. Minimum Structure

A minimal Call Path contains:

```text
Goal

Responsibilities

Ordered Nodes

Typed Edges

Completion Criteria
```

Additional information may include:

* Context
* Confidence
* Validation
* Runtime State
* Version
* Provenance

---

# 9. Root

Every Call Path begins from a root responsibility.

Usually this corresponds to:

```text
General Dispatcher
```

The root determines the initial direction of specialization.

---

# 10. Internal Nodes

Internal nodes progressively narrow computational responsibility.

Example:

```text
Engineering
        ↓
Software
        ↓
Compiler
```

Each node reduces uncertainty while increasing specialization.

---

# 11. Leaf Node

The leaf is normally the most specialized primary responsibility.

Example:

```text
LLVM Loop Optimization
```

The leaf performs only one part of the total computation.

Completion still requires validation and possible fallback.

---

# 12. Validation Stage

Every important Call Path should contain validation.

Validation may be:

```text
Structural

Mathematical

Runtime

Policy

Human
```

Validation is a first-class responsibility rather than an afterthought.

---

# 13. Completion

A Call Path completes only when:

* required responsibility is fulfilled;
* validation succeeds;
* output contract is satisfied.

Reaching the final computational node alone does not imply successful completion.

---

# 14. Call Path Example

```text
Goal:
Compiler Optimization

↓

Dispatch

↓

Repository Retrieval

↓

Calling Graph Analysis

↓

Optimization Brain Unit

↓

Correctness Validator

↓

Performance Validator

↓

Output
```

Every stage contributes distinct computational responsibility.

---

# 15. Context Propagation

Context flows through the path.

Examples:

* retrieved code;
* runtime state;
* previous decisions;
* user constraints.

Context should remain explicit.

Hidden context reduces explainability.

---

# 16. Responsibility Propagation

Responsibility also propagates.

Example:

```text
Dispatcher

↓

Compiler Unit

↓

Validator
```

Each stage owns only part of the total responsibility.

The path owns the complete responsibility.

---

# 17. Confidence Propagation

Confidence evolves throughout execution.

Dispatcher confidence may differ from:

* retrieval confidence;
* optimization confidence;
* validation confidence.

The final confidence should reflect the entire path.

---

# 18. Provenance Propagation

Every result should preserve provenance.

Ideally:

```text
Output

↓

Call Path

↓

Nodes

↓

Training Groups
```

This enables traceability.

---

# 19. Static Call Paths

Some paths are predetermined.

Example:

```text
Retrieve

↓

Reason

↓

Generate
```

These are simple and predictable.

---

# 20. Dynamic Call Paths

More advanced systems construct paths dynamically.

Dispatch decisions depend upon:

* Goal Function;
* Context;
* Runtime State;
* Confidence;
* Availability.

Different inputs may activate different branches.

---

# 21. Adaptive Call Paths

An adaptive path changes during execution.

Example:

```text
Validation Failed

↓

Activate Alternative Unit

↓

Continue Execution
```

Adaptation occurs without restarting the entire computation.

---

# 22. Hierarchical Call Paths

Paths naturally inherit hierarchy from Dispatch Trees.

```text
General

↓

Engineering

↓

Software

↓

Compiler
```

Hierarchy improves explainability.

---

# 23. Shared Segments

Several paths may share:

```text
Retrieval

↓

Validation
```

These become reusable computational assets.

---

# 24. Boundary Paths

Boundary Sets may activate dedicated paths.

Example:

```text
Boundary Detection

↓

Context Expansion

↓

Recursive Dispatch

↓

General Fallback
```

Boundary processing is therefore explicit.

---

# 25. Fallback Paths

Fallback is simply another Call Path.

Example:

```text
Specialist Failed

↓

General Unit

↓

Validation

↓

Output
```

Fallback should not be hidden.

---

# 26. Human Call Paths

Humans may appear naturally.

Example:

```text
AI Analysis

↓

Human Decision

↓

AI Execution
```

The human becomes one Computational Unit.

---

# 27. Heterogeneous Call Paths

A path may include:

* LLM
* Symbolic Solver
* Database
* Controller
* Human

No assumption of homogeneous models is required.

---

# 28. Multi-Branch Execution

Some paths split.

```text
Retrieve

├── Policy

├── Mathematics

└── Safety

↓

Aggregation
```

Parallel execution is naturally supported.

---

# 29. Aggregation

Parallel branches require aggregation.

Possible methods:

* voting;
* ranking;
* confidence fusion;
* structural consistency.

Aggregation is itself a Computational Responsibility.

---

# 30. Call Path Lifetime

A Call Path exists only while executing.

However:

* templates;
* histories;
* statistics;
* versions

may persist.

---

# 31. Runtime Logging

Every path should log:

* activated nodes;
* contexts;
* outputs;
* validation;
* fallback events;
* execution time.

Logging enables optimization.

---

# 32. Path Complexity

Complexity may be measured by:

* node count;
* edge count;
* branching factor;
* validation depth;
* fallback depth.

Operator Economy seeks lower complexity without losing capability.

---

# 33. Latency

Latency equals the cumulative cost of the path.

Reducing latency often means improving:

* dispatch;
* context reuse;
* path length;
* specialization.

---

# 34. Cost

Different paths incur different computational costs.

Expensive specialists should only activate when justified.

GTDO therefore naturally supports cost-aware dispatch.

---

# 35. Reliability

Reliability belongs to the path.

Even perfect nodes cannot guarantee reliable execution if:

* dispatch fails;
* context is lost;
* validation is missing.

---

# 36. Explainability

Call Paths naturally explain decisions.

Instead of:

> The model answered.

We obtain:

```text
Dispatcher

↓

Retrieval

↓

Compiler Unit

↓

Validator

↓

Output
```

This provides engineering transparency.

---

# 37. Path Validation

Validation occurs at multiple levels:

* node;
* segment;
* entire path.

All three matter.

---

# 38. Path Metrics

Useful metrics include:

* Success Rate;
* Validation Rate;
* Fallback Frequency;
* Average Latency;
* Average Cost;
* Path Utilization.

---

# 39. Path Attribution

Every success or failure should be attributed to the active Call Path.

This enables local optimization.

---

# 40. Path Evolution

Call Paths evolve through:

* new responsibilities;
* new nodes;
* improved dispatch;
* better validation;
* better context.

Evolution should preserve responsibility semantics.

---

# 41. Path Versioning

Each path should maintain:

* Version;
* Dependencies;
* Validation Status;
* Rollback Target.

Independent versioning reduces engineering risk.

---

# 42. Path Rollback

If a path update fails:

```text
Version 2

↓

Rollback

↓

Version 1
```

Rollback should be local whenever possible.

---

# 43. Local Optimization

Instead of retraining everything:

```text
Optimize

↓

One Path

↓

Validate

↓

Deploy
```

GTDO thereby creates natural optimization boundaries.

---

# 44. Call Paths and Reinforcement Learning

Rewards should be assigned to:

* nodes;
* edges;
* segments;
* entire paths.

The correct organizational level depends upon failure attribution.

---

# 45. Path Segments

Large paths naturally decompose into segments.

Segments become reusable computational modules.

This motivates GTDO-303.

---

# 46. Call Paths and Dispatch Trees

Every Call Path corresponds to one realization of a Dispatch Tree branch.

Dispatch chooses.

The Call Path executes.

---

# 47. Call Paths and Calling Graphs

Calling Graphs contain all possible paths.

A Call Path is one activated trajectory.

Conceptually:

```text
Calling Graph

↓

Runtime Selection

↓

Call Path
```

---

# 48. General Applicability

The concept applies equally to:

* LLM Brain Units;
* Robotics;
* Software Engineering;
* Scientific Computing;
* Control Engineering;
* Human–AI Organizations.

It is a general computation organization principle.

---

# 49. Canonical GTDO Statements

> A Call Path is the ordered execution sequence of Computational Responsibilities for one Goal Function.

> The path—not the isolated model—is often the true computational object.

> Dispatch selects the path.

> Calling Graphs contain possible paths.

> Runtime activates one or more paths.

> Validation and fallback belong to the path.

> Optimization should frequently target paths instead of whole models.

---

# 50. Central Transformation

```text
Goal Function
        ↓
Dispatch
        ↓
Call Path Selection
        ↓
Context Propagation
        ↓
Responsibility Execution
        ↓
Validation
        ↓
Fallback if Necessary
        ↓
Completed Computational Responsibility
```

---

# 51. Long-Term Significance

The concept of Call Paths shifts Hybrid AI from **model-centric computation** toward **organization-centric computation**.

Traditional AI often assumes that intelligence resides primarily inside a single large model.

GTDO proposes that intelligence increasingly emerges from the **organization of computational responsibilities**, their dispatch, their coordination, and their execution paths.

Once Call Paths become explicit engineering objects, entirely new forms of optimization become possible:

* path-specific reinforcement learning;
* path-level fine-tuning;
* local validation;
* structural rollback;
* responsibility attribution;
* computational auditing;
* runtime evolution.

The engineering question therefore changes from:

> **How do we optimize the model?**

to:

> **How do we optimize the responsible Call Path?**

This change mirrors the evolution from monolithic software toward modular software engineering.

It provides a practical foundation for scalable Brain Unit organizations and heterogeneous Hybrid AI systems.

---

# Key Takeaways

* A Call Path is the ordered execution sequence of Computational Responsibilities activated by one Goal Function.
* The Call Path, rather than an isolated model, is often the true computational object.
* Dispatch selects Call Paths; Calling Graphs contain all possible paths.
* Context, responsibility, confidence, and provenance propagate along the path.
* Validation, Boundary handling, and fallback are integral parts of a Call Path.
* Call Paths may be static, dynamic, adaptive, hierarchical, parallel, or heterogeneous.
* Runtime logging enables attribution, auditing, and optimization.
* Local optimization should frequently target Call Paths instead of whole models.
* The concept applies generally across Hybrid AI, software engineering, robotics, scientific computing, control systems, and Human–AI organizations.

---

## Further Reading

### GTDO Part III

* GTDO-201 — *From Training Groups to Computational Units*

### GTDO Part IV

* GTDO-301 — *Dispatch Trees as Calling Graphs*
* GTDO-303 — *Call Path Segments*
* GTDO-304 — *Call-Path Reinforcement Learning*
* GTDO-305 — *Local Fine-Tuning*
* GTDO-306 — *Local Validation*
* GTDO-307 — *Local Versioning*
* GTDO-308 — *Local Rollback*
* GTDO-309 — *Structural Scope of Optimization*

### Related Structural Frameworks

* Structural Runtime AI (SRAI)
* Calling Graph for AI Coding
* Runtime Invariant Algebra (RIA)
* Common Concept Core (CCC)
* Function Tunnel (FT)
