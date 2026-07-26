# GTDO-101 — Two Modes of Goal-Oriented Grouping

## Point-to-Group Assignment and Point-to-Block Grouping

---

#### Fig-020-Part-II-Core-Grouping-Algorithms.png

![Fig-020-Part-II-Core-Grouping-Algorithms.png](../figures/Fig-020-Part-II-Core-Grouping-Algorithms.png)

---

## Abstract

Goal-Oriented Training Data Organization requires more than one grouping mechanism.

Some organizational goals assign distributed samples to a common computational responsibility without requiring continuity. Other goals require contiguous or ordered regions to remain together because local sequence, topology, or context is part of the responsibility.

GTDO therefore defines two foundational grouping modes:

1. **Point-to-Group Assignment**
2. **Point-to-Block Grouping**

The first mode organizes potentially non-contiguous samples into responsibility-bearing groups. Its canonical structural mechanism is **Two-Way Common Concept Core**.

The second mode organizes contiguous or ordered variable-size regions while preserving continuity. Its canonical structural mechanism is **Variable-Size Blocks Indexing and Searching**.

These two modes are not competing alternatives. They solve different structural problems.

Their distinction is determined by the Goal Function:

> Does the intended Computational Responsibility depend only on sample-level structural compatibility, or does it also depend on continuity, adjacency, and regional integrity?

This article defines both modes, compares their assumptions and outputs, explains how context, Boundary Sets, significance, fallback, and recursion operate in each, and establishes them as the two algorithmic foundations of GTDO.

---

#### Fig-113-Data-and-Knowledge-Flow.png

![Fig-113-Data-and-Knowledge-Flow.png](../figures/Fig-113-Data-and-Knowledge-Flow.png)

---

# 1. Why GTDO Requires Two Grouping Modes

Training data can contain two fundamentally different forms of organizational structure.

The first is distributed structure.

Examples may appear across:

* different documents;
* distant corpus positions;
* different time intervals;
* separate code files;
* multiple domains.

Yet they may support the same Computational Responsibility.

The second is regional structure.

Examples must remain together because:

* sequence matters;
* context accumulates;
* order carries meaning;
* a region forms one event;
* a block defines one computational unit.

One algorithmic mode cannot represent both cases adequately.

GTDO therefore distinguishes:

```text
Distributed Responsibility Structure
        ↓
Point-to-Group Assignment
```

and:

```text
Continuity-Preserving Responsibility Structure
        ↓
Point-to-Block Grouping
```

---

# 2. Canonical Definition of the Two Modes

## Point-to-Group Assignment

> Point-to-Group Assignment assigns individual samples or objects to a common goal-oriented group without requiring their original locations to be contiguous.

Canonical form:

```text
Point 1   ─┐
Point 8    │
Point 21   ├──→ Group A
Point 37   │
Point 94  ─┘
```

The organizing principle is structural or responsibility compatibility.

---

## Point-to-Block Grouping

> Point-to-Block Grouping assigns samples to a contiguous or ordered variable-size region whose continuity is part of the Goal Function.

Canonical form:

```text
Ordered Data
        ↓
[ Variable-Size Block A ]
[ Variable-Size Block B ]
[ Variable-Size Block C ]
```

The organizing principle includes both structural compatibility and regional continuity.

---

# 3. The Governing Question

The choice between the two modes should be made by asking:

> Does the intended Computational Responsibility require continuity?

If no:

```text
Use Point-to-Group Assignment
```

If yes:

```text
Use Point-to-Block Grouping
```

This decision must come from the Goal Function rather than from implementation convenience.

---

# 4. Continuity Is an Organizational Constraint

Continuity may be:

* textual;
* temporal;
* spatial;
* sequential;
* graph-based;
* procedural;
* causal;
* runtime-oriented.

A continuity constraint states that the responsibility depends on preserving a connected region or ordered sequence.

Example:

```text
A complete compiler optimization episode
```

may require all events from:

```text
Trigger
    ↓
Transformation
    ↓
Validation
    ↓
Outcome
```

to remain one block.

By contrast, all examples of one optimization responsibility may be distributed across many files.

These are different organizational problems.

---

# 5. Point-to-Group Assignment

Point-to-Group Assignment is appropriate when group membership depends on structural role rather than physical location.

Examples include:

* all inputs producing RHS Group 0;
* all examples requiring symbolic validation;
* all compiler-optimization cases;
* all high-risk approval cases;
* all samples sharing one CCC;
* all examples activating one Brain Unit.

The samples may be distributed widely.

Their shared Computational Responsibility gives them organizational unity.

---

# 6. Canonical Algorithm for Point-to-Group Assignment

The canonical GTDO algorithm is:

> **Two-Way Common Concept Core**

General process:

```text
Training Samples
        ↓
Goal Function
        ↓
Two-Way CCC
        ↓
Group A
Group B
Boundary Set
Optional Discard Set
```

Two-Way CCC discovers or applies two structurally meaningful directions.

Each sample is evaluated relative to these directions.

---

# 7. Why Two-Way CCC Fits Point-to-Group Assignment

Two-Way CCC is suitable because it emphasizes:

* shared structure;
* opposing or complementary concepts;
* non-contiguous membership;
* structural compatibility;
* Boundary preservation.

It does not require samples to occupy one local region.

This makes it fundamentally different from block segmentation.

---

# 8. Point-to-Group Assignment Outputs

A mature Point-to-Group process should support:

```text
Primary Group A

Primary Group B

Boundary Set

Multi-Group Assignment

General Fallback Assignment

Discard Set

Deferred Set

No-Split Decision
```

Binary assignment alone is insufficient for real-world GTDO.

---

# 9. Direct Evidence in Point-to-Group Assignment

Direct evidence may include:

* RHS labels;
* known classes;
* domain identifiers;
* explicit task types;
* human annotations.

Example:

```text
RHS = 0
    → Group 0

RHS = 1
    → Group 1
```

The Goal Function may use these outputs to organize LHS training data.

---

# 10. Indirect Evidence in Point-to-Group Assignment

Indirect evidence may include:

* generated context;
* CCC compatibility;
* Runtime Invariants;
* shared output behavior;
* historical dispatch;
* structural relationships;
* Calling Graph roles.

Indirect evidence is essential when the responsibility is not directly labeled.

---

# 11. Context in Point-to-Group Assignment

Context may connect distant samples.

Example:

```text
Different words
Different documents
Different local structures
        ↓
Shared compiler-optimization context
        ↓
Same responsibility group
```

Context therefore acts as a distributed organizational bridge.

---

# 12. Point-to-Group Assignment and Metric Similarity

Metric similarity may support assignment.

However, the Goal Function must remain primary.

Two samples may be close in embedding space but belong to different responsibilities.

Two samples may be distant yet perform the same structural role.

Therefore:

```text
Structural Responsibility
    stands above
Metric Proximity
```

---

# 13. Boundary Sets in Point-to-Group Assignment

Boundary cases may have:

* weak match to both CCCs;
* strong match to both;
* missing context;
* new structure;
* multiple responsibilities.

Possible responses include:

```text
Recursive Two-Way CCC

Context Enrichment

Multi-Path Assignment

Boundary Unit

General Fallback

Human Review
```

---

# 14. Recursive Point-to-Group Assignment

A Boundary Set may contain further distributed structure.

Recursive process:

```text
Boundary Set
        ↓
Revised Goal or Context
        ↓
Second Two-Way CCC
        ↓
New Groups + Residual Boundary
```

Recursion should be controlled by significance and stopping conditions.

---

# 15. Weak Point-to-Group Separation

If Two-Way CCC does not produce a significant split, GTDO should permit:

```text
No Split
```

Other possible actions include:

* retain original group;
* revise the Goal Function;
* add context;
* use a multi-group method;
* assign to general fallback.

The algorithm must not force a false binary architecture.

---

# 16. Point-to-Block Grouping

Point-to-Block Grouping is appropriate when regional integrity matters.

Examples include:

* document arguments;
* code functions;
* temporal episodes;
* control regimes;
* image regions;
* runtime event sequences;
* conversation episodes;
* local context windows.

A block has both:

* internal structure;
* external boundaries.

Its continuity is part of the responsibility.

---

# 17. Canonical Algorithm for Point-to-Block Grouping

The canonical GTDO algorithm is:

> **Variable-Size Blocks Indexing and Searching**

General process:

```text
Ordered Data
        ↓
Goal Function
+
Continuity Constraint
        ↓
Variable-Size Block Recognition
        ↓
Block Indexing
        ↓
Block Search and Dispatch
```

The block length is determined structurally rather than fixed in advance.

---

# 18. Why Variable-Size Blocks Fit Point-to-Block Grouping

Fixed-size chunks often break meaningful regions.

A variable-size block can preserve:

* full context;
* complete event structure;
* function boundaries;
* local causal sequence;
* responsibility coherence.

Variable-Size Blocks Indexing and Searching supports both organization and efficient later access.

---

# 19. Point-to-Block Grouping Outputs

Possible outputs include:

```text
Recognized Block

Nested Block

Overlapping Candidate Block

Boundary Region

Unresolved Transition Region

General Block

Discarded Region

No-Block Decision
```

The result should preserve the structural meaning required by the Goal Function.

---

# 20. Block Start Conditions

A block may begin when:

* a trigger appears;
* a context changes;
* a responsibility activates;
* a state transition occurs;
* a function begins;
* an invariant regime starts.

The start condition should be explicit.

---

# 21. Block Continuation Conditions

A block continues while:

* local structure remains compatible;
* context remains stable;
* the same responsibility applies;
* continuity invariants hold;
* no termination condition appears.

Continuation is a structural decision, not merely a fixed length.

---

# 22. Block Termination Conditions

A block may end when:

* responsibility changes;
* context changes;
* a target outcome occurs;
* a new trigger appears;
* structural compatibility falls below threshold;
* the episode completes.

Termination conditions define the block boundary.

---

# 23. Nested Blocks

One block may contain smaller responsibility-bearing blocks.

Example:

```text
Software Engineering Episode
    └── Compiler Episode
         └── Optimization Episode
```

Nested blocks may support hierarchical Dispatch Trees.

---

# 24. Overlapping Blocks

Some responsibilities may overlap.

Example:

```text
Security Review Block
overlaps
Compiler Optimization Block
```

GTDO should not assume that all block organizations form a strict partition.

Overlapping blocks may require a Dispatch Graph.

---

# 25. Block Context

Point-to-Block Grouping often depends on local context.

However, Global Context may determine the meaning of the block.

Example:

```text
Local code sequence
+
Repository architecture
+
Build target
        ↓
Compiler responsibility block
```

Both local and global context may be required.

---

# 26. Boundary Regions in Point-to-Block Grouping

Transitions between blocks may be uncertain.

Example:

```text
Normal Operation
        ↓
Uncertain Transition
        ↓
Failure Regime
```

The transition may become:

* a Boundary Block;
* a separate transition responsibility;
* part of one neighboring block;
* a multi-responsibility region.

---

# 27. No-Block Decision

Not every local pattern deserves a separate block.

A No-Block decision is appropriate when:

* continuity is weak;
* the region is too short;
* boundaries are unstable;
* the computational benefit is low;
* the responsibility is better represented as Point-to-Group.

---

# 28. The Two Modes Are Complementary

Point-to-Group and Point-to-Block solve different aspects of organization.

Example:

```text
All compiler-optimization samples
        ↓
Point-to-Group Assignment
```

Within one long compiler trace:

```text
One optimization episode
        ↓
Point-to-Block Grouping
```

The same application may use both modes.

---

# 29. Group-Then-Block

One workflow is:

```text
Distributed Samples
        ↓
Point-to-Group Assignment
        ↓
Responsibility Group
        ↓
Point-to-Block Grouping within each source
```

This first identifies global responsibility, then local episodes.

---

# 30. Block-Then-Group

Another workflow is:

```text
Ordered Data
        ↓
Point-to-Block Grouping
        ↓
Recognized Blocks
        ↓
Point-to-Group Assignment across blocks
```

This first extracts coherent regions, then groups equivalent blocks across sources.

Both orders are valid.

The Goal Function determines which is preferable.

---

# 31. Hierarchical Combination

The two modes may alternate.

```text
Corpus
    ↓
Point-to-Group by Domain
    ↓
Point-to-Block by Episode
    ↓
Point-to-Group by Responsibility
    ↓
Dispatch Tree
```

This produces multi-level computation organization.

---

# 32. Point, Block, and Hierarchy

The combined GTDO ladder is:

```text
Point
    ↓
Group
    ↓
Block
    ↓
Region
    ↓
Responsibility
    ↓
Computational Unit
    ↓
Dispatch Tree or Graph
```

The exact order may vary.

The hierarchy should preserve organizational meaning.

---

# 33. Relationship to Segmentation

Point-to-Block Grouping includes segmentation-like behavior.

Point-to-Group Assignment does not require segmentation.

Therefore:

```text
Segmentation
    is one mechanism inside
GTDO Grouping
```

It is not the universal definition of grouping.

---

# 34. Relationship to Dispatch

Grouping organizes evidence.

Dispatch assigns responsibility.

The relation is:

```text
Goal-Oriented Grouping
        ↓
Responsibility Candidate
        ↓
Dispatch
        ↓
Computational Unit or Call Path
```

A group is not yet a dispatch decision.

---

# 35. Relationship to Computational Responsibility

Both modes should produce responsibility interpretations.

Point-to-Group example:

```text
Distributed validation samples
        ↓
Validation Responsibility
```

Point-to-Block example:

```text
Complete failure episode
        ↓
Recovery Responsibility
```

Without responsibility, grouping remains incomplete.

---

# 36. Relationship to Brain Units

A group or block may support:

* an LLM Brain Unit;
* a Context Generator;
* a validator;
* a retrieval collection;
* a control policy;
* a Boundary Unit.

The grouping mode does not dictate the implementation.

---

# 37. Relationship to Dispatch Trees

Point-to-Group Assignment often produces responsibility branches.

Point-to-Block Grouping may produce local path segments or episode nodes.

Combined:

```text
Responsibility Group
        ↓
Block Structure
        ↓
Dispatch Branch
        ↓
Call Path
```

---

# 38. Relationship to Dispatch Graphs

Overlapping groups, shared blocks, and reused Computational Units may create graph structure.

Examples include:

* one block belonging to two responsibilities;
* one unit serving several groups;
* one validator used across branches.

GTDO should support graphs rather than forcing a tree.

---

# 39. Relationship to Call Paths

A Point-to-Group assignment may determine which path family applies.

A Point-to-Block grouping may determine which local sequence forms one Call Path Segment.

Example:

```text
Global Responsibility:
Compiler Optimization

Local Block:
One optimization episode

Runtime Path:
Compiler → Optimization → Validation
```

---

# 40. Mode Selection Policy

A practical mode-selection policy should consider:

```text
Is continuity required?

Is order meaningful?

Are group members distributed?

Does one region form one responsibility?

Can blocks overlap?

Is local context essential?

Does the Goal Function operate on points or episodes?
```

The result may be:

```text
Point-to-Group

Point-to-Block

Combined Mode

No Grouping
```

---

# 41. Hybrid Mode

Some cases require both modes simultaneously.

Example:

```text
A complete code block
```

must remain contiguous.

But all equivalent code blocks across repositories should be assigned to one responsibility group.

This is:

```text
Point-to-Block
+
Point-to-Group
```

A Hybrid Mode should preserve both local integrity and global responsibility.

---

# 42. Goal Function Differences

For Point-to-Group Assignment, the Goal Function emphasizes:

* structural compatibility;
* RHS outcome;
* responsibility;
* distributed evidence.

For Point-to-Block Grouping, it additionally specifies:

* continuity;
* start;
* continuation;
* termination;
* block scale.

The Goal Function must encode the correct structural assumptions.

---

# 43. Confidence Differences

Point-to-Group confidence concerns:

* membership compatibility;
* CCC match;
* responsibility fit.

Point-to-Block confidence concerns:

* block start;
* block continuation;
* block end;
* regional coherence.

These confidence dimensions should not be conflated.

---

# 44. Significance Differences

Point-to-Group significance asks:

> Does this grouping reveal a useful responsibility distinction?

Point-to-Block significance asks:

> Does this region form a coherent responsibility-bearing block?

Both require computational validation.

---

# 45. Boundary Differences

Point-to-Group Boundary Set:

```text
Distributed unresolved samples
```

Point-to-Block Boundary Region:

```text
Uncertain contiguous transition or region
```

The resolution mechanisms may differ.

---

# 46. Recursion Differences

Point-to-Group recursion may split a distributed Boundary Set.

Point-to-Block recursion may subdivide a broad block or identify nested blocks.

Recursion must preserve the appropriate structural semantics.

---

# 47. Fallback Differences

Point-to-Group fallback may route uncertain samples to:

* general model;
* Boundary Unit;
* human review.

Point-to-Block fallback may:

* retain a larger block;
* use a broader context window;
* dispatch the entire sequence to a general unit;
* defer boundary determination.

---

# 48. Evaluation of Point-to-Group Assignment

Relevant measures include:

* group coherence;
* responsibility clarity;
* assignment stability;
* Boundary Set quality;
* output improvement;
* specialist performance;
* general coverage preservation.

---

# 49. Evaluation of Point-to-Block Grouping

Relevant measures include:

* block coherence;
* boundary quality;
* continuity preservation;
* context completeness;
* responsibility clarity;
* retrieval efficiency;
* path-level performance.

---

# 50. Comparison Table

| Dimension                | Point-to-Group Assignment        | Point-to-Block Grouping                     |
| ------------------------ | -------------------------------- | ------------------------------------------- |
| Core object              | Individual sample or object      | Contiguous or ordered region                |
| Continuity required      | No                               | Yes                                         |
| Canonical algorithm      | Two-Way CCC                      | Variable-Size Blocks Indexing and Searching |
| Main structural question | Which group owns this point?     | Which block contains this point?            |
| Primary output           | Distributed responsibility group | Responsibility-bearing block                |
| Typical context          | Global or distributed            | Local plus global                           |
| Boundary form            | Boundary Set                     | Boundary Region or Block                    |
| Recursion                | Re-group unresolved samples      | Subdivide or nest blocks                    |
| Dispatch role            | Select responsibility branch     | Define local episode or path segment        |
| Typical use              | Domain, role, output family      | Sequence, episode, function, region         |

---

# 51. Common Failure Modes

## Using Point-to-Block for Distributed Responsibility

The algorithm forces artificial contiguous regions.

## Using Point-to-Group for Sequence-Dependent Structure

The algorithm breaks important order and context.

## Treating Fixed Chunks as Blocks

Operational chunking is mistaken for responsibility structure.

## Forcing Exclusive Groups

Cross-domain or overlapping responsibilities are lost.

## Ignoring No-Split or No-Block

The system creates unnecessary architecture.

## Mixing Confidence Types

Point membership and boundary confidence are treated as equivalent.

## Algorithm-First Selection

The available algorithm determines the mode rather than the Goal Function.

---

# 52. Engineering Workflow

A practical GTDO workflow is:

```text
Step 1:
Define Goal Function

Step 2:
Determine whether continuity matters

Step 3:
Select Point-to-Group, Point-to-Block, or Hybrid Mode

Step 4:
Apply structural algorithm

Step 5:
Preserve Boundary outputs

Step 6:
Interpret Computational Responsibility

Step 7:
Validate organizational benefit

Step 8:
Construct Dispatch structure
```

---

# 53. Minimal Mode Specification

A grouping-mode specification may include:

```text
Mode Name

Goal Function

Input Object Type

Continuity Requirement

Structural Evidence

Context Requirements

Primary Algorithm

Allowed Outputs

Boundary Policy

Recursion Policy

Fallback Policy

Validation Measures

Version
```

---

# 54. Generality Beyond LLMs

## Language

Point-to-Group:

* distributed intent examples;
* output families;
* responsibility groups.

Point-to-Block:

* passages;
* arguments;
* dialogue episodes.

## Software

Point-to-Group:

* all security defects;
* all optimization cases.

Point-to-Block:

* functions;
* code regions;
* execution traces.

## Control

Point-to-Group:

* similar control conditions across runs.

Point-to-Block:

* operating regimes;
* failure and recovery episodes.

## Vision

Point-to-Group:

* distributed object examples.

Point-to-Block:

* spatial or temporal regions.

The distinction is general across AI computation.

---

# 55. Canonical GTDO Statements

> GTDO has two foundational grouping modes: Point-to-Group Assignment and Point-to-Block Grouping.

> Point-to-Group Assignment organizes distributed samples by Computational Responsibility.

> Point-to-Block Grouping organizes contiguous or ordered variable-size regions by Computational Responsibility.

> Two-Way CCC is the canonical Point-to-Group mechanism.

> Variable-Size Blocks Indexing and Searching is the canonical Point-to-Block mechanism.

> The Goal Function determines whether continuity is required.

> The two modes are complementary and may be combined hierarchically.

> Grouping is complete only when its output receives a Computational Responsibility interpretation.

---

# 56. Central Transformation

The unified GTDO grouping process is:

```text
Training Data
        ↓
Goal Function
        ↓
Continuity Decision
        ↓
┌─────────────────────────────┐
│ Point-to-Group Assignment   │
│ by Two-Way CCC              │
└─────────────────────────────┘
or
┌─────────────────────────────┐
│ Point-to-Block Grouping     │
│ by Variable-Size Blocks     │
└─────────────────────────────┘
        ↓
Groups / Blocks / Boundary / No-Split
        ↓
Computational Responsibility
        ↓
Dispatch Tree or Graph
```

---

# 57. Long-Term Significance

The distinction between Point-to-Group and Point-to-Block gives GTDO a general algorithmic foundation.

It prevents two common errors:

1. reducing all organization to clustering;
2. reducing all organization to segmentation.

Some computation is unified by distributed structural role.

Other computation is unified by contiguous regional integrity.

Future AI systems require both.

Once these modes are combined with Goal Functions, context, Boundary Sets, Computational Responsibility, and Dispatch, training data can be transformed into an explicit architecture of specialized, shared, general, and evolving computation.

---

# Key Takeaways

* GTDO requires two core grouping modes because distributed responsibility and continuous regional structure are different problems.
* Point-to-Group Assignment does not require continuity.
* Point-to-Block Grouping requires continuity or ordered adjacency.
* Two-Way CCC is the canonical Point-to-Group algorithm.
* Variable-Size Blocks Indexing and Searching is the canonical Point-to-Block algorithm.
* The Goal Function determines which mode is appropriate.
* Both modes must support Boundary, Fallback, No-Split or No-Block, and validation.
* The modes may be combined as Group-Then-Block, Block-Then-Group, or a hierarchical Hybrid Mode.
* Point-to-Group often defines responsibility branches.
* Point-to-Block often defines episodes, local contexts, or Call Path Segments.
* Neither grouping mode is complete until it is mapped to Computational Responsibility.
* Together, the two modes form the algorithmic foundation for GTDO Part II.

---

## Further Reading

### GTDO Foundations

* GTDO-003 — *Goal Functions and RHS-Driven Training Organization*
* GTDO-004 — *Dispatch Is Not Segmentation*
* GTDO-006 — *Computational Responsibility*
* GTDO-008 — *Context as an Organizational Dimension*
* GTDO-009 — *Boundary Sets*

### Part II — Core Algorithms

* GTDO-102 — *Point-to-Group Assignment by Two-Way CCC*
* GTDO-103 — *Point-to-Block Grouping by Variable-Size Blocks*
* GTDO-104 — *Recursive Two-Way CCC*
* GTDO-105 — *Boundary Resolution*
* GTDO-106 — *Goal Function Engineering*
* GTDO-108 — *Significance and Confidence*

### GTDO Computation Organization

* GTDO-201 — *From Training Groups to Computational Units*
* GTDO-207 — *Dispatch Trees*
* GTDO-208 — *Dispatch Graphs*
* GTDO-301 — *Dispatch Trees as Calling Graphs*

### Related Structural Work

* **Common Concept Core (CCC)**
* **Two-Way CCC**
* **Variable-Size Blocks Indexing and Searching**
* **Structural Runtime AI (SRAI)**
* **Structural Recognition above Metric Similarity (SRMS)**
