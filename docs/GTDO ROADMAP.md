# GTDO ROADMAP

## Goal-Oriented Training Data Organization

### From Data Segmentation to General AI Computation Organization

**Repository Roadmap**
**Status:** Active Research and Development Plan
**Roadmap Version:** 1.0

---

# 1. Purpose of This Roadmap

This roadmap defines the planned development of Goal-Oriented Training Data Organization.

It translates the constitutional principles and repository outline into an ordered research, engineering, documentation, and release program.

GTDO begins with a practical problem:

> How can training data be organized according to an RHS grouping or dispatch goal so that future AI computation becomes more specialized, efficient, controllable, and locally optimizable?

The repository must develop beyond this initial problem without losing it.

The long-term scope is:

```text
Training Data Organization
            ↓
Computational Responsibility
            ↓
Computational Unit Formation
            ↓
Dispatch Trees and Graphs
            ↓
Call-Path-Based Optimization
            ↓
Runtime Hybrid AI Organization
            ↓
General AI Computation Organization
```

The roadmap is therefore divided into several development horizons:

1. establish the conceptual foundation;
2. formalize the two core grouping modes;
3. solve boundary and fallback control;
4. connect grouped data to computational units;
5. develop Dispatch Trees and Call Paths;
6. enable local training and reinforcement;
7. build an engineering control architecture;
8. extend GTDO to heterogeneous and runtime AI systems;
9. validate the framework through experiments and implementations;
10. develop a general algebra of computational organization.

---

# 2. Roadmap Principles

All roadmap work should follow these principles.

## 2.1 Goal Before Algorithm

A grouping algorithm must be selected according to the organizational goal.

The roadmap must not become an algorithm collection without a stable computation-organization purpose.

---

## 2.2 Organization Above Segmentation

Every stage should preserve the distinction among:

```text
Segmentation
    =
Data boundary construction

Dispatch
    =
Computational responsibility assignment

Organization
    =
Construction of a controllable computation architecture
```

---

## 2.3 Generality Beyond LLMs

LLM Brain Units provide the first major application path.

However, all foundational definitions should remain applicable to:

* world models;
* symbolic reasoning;
* planning;
* search;
* retrieval;
* simulation;
* control systems;
* software functions;
* agents;
* human experts;
* heterogeneous Hybrid AI systems.

---

## 2.4 Boundary Is a Primary Design Problem

Boundary Sets, weak separation, fallback, deferred assignment, and multi-path dispatch must be treated as central engineering subjects.

They must not be postponed as minor cleanup tasks.

---

## 2.5 Local Structural Scope

The roadmap should progressively move optimization from:

```text
Whole Model
```

toward:

```text
Computational Unit

Call Path

Call Path Segment

Shared Subgraph

Dispatch Rule
```

---

## 2.6 Text Before Large-Scale Figures

Core concepts and article structures should be stabilized before generating the full figure set.

Figures should explain settled structures rather than force premature structures.

---

## 2.7 Theory and Engineering Must Advance Together

GTDO should not remain only conceptual.

Each major theoretical claim should eventually connect to:

* an algorithm;
* an interface;
* a control condition;
* an evaluation method;
* an experiment;
* or an engineering implementation.

---

# 3. Development Horizon I — Constitutional Foundation

## Objective

Establish GTDO as an independent research subject and define its stable terminology, scope, and architecture.

## Core Deliverables

* `CONSTITUTION.md`
* `OUTLINE.md`
* `ROADMAP.md`
* `GLOSSARY.md`
* `CONTENTS.md`
* Part-level directory structure
* initial figure plan

## Foundational Articles

* GTDO-001 — Why Goal-Oriented Training Data Organization
* GTDO-002 — From Data Segmentation to AI Computation Organization
* GTDO-003 — Goal Functions and RHS-Driven Training Organization
* GTDO-004 — Dispatch Is Not Segmentation
* GTDO-005 — Training Data Organization as Computation Organization
* GTDO-006 — Computational Responsibility
* GTDO-007 — Dispatch and Organizational Semantics
* GTDO-008 — Context as an Organizational Dimension
* GTDO-009 — Boundary Sets
* GTDO-010 — Summary of Foundations

## Key Questions

* Why is ordinary data preprocessing insufficient?
* What does a Goal Function control?
* How does an RHS grouping objective create computational responsibility?
* Why is dispatch different from segmentation?
* How can training organization influence future AI architecture?
* Which concepts are specific to LLMs and which are general?

## Completion Criteria

This horizon is complete when a reader can understand:

1. what GTDO is;
2. why it is needed;
3. what problem it solves;
4. why it is not merely clustering or segmentation;
5. how it connects data organization to computation organization;
6. why its scope extends beyond LLMs.

---

# 4. Development Horizon II — Core Grouping Algorithms

## Objective

Formalize the two foundational GTDO grouping modes and connect each mode to an established structural algorithm.

---

## 4.1 Point-to-Group Assignment

### Core Algorithm

> Two-Way Common Concept Core

### Target Capability

Assign non-contiguous samples to goal-defined groups according to direct or indirect structural evidence.

### Planned Articles

* GTDO-101 — Two Modes of Goal-Oriented Grouping
* GTDO-102 — Point-to-Group Assignment by Two-Way CCC
* GTDO-104 — Recursive Two-Way CCC
* GTDO-106 — Goal Function Engineering
* GTDO-108 — Significance and Confidence

### Engineering Topics

* binary RHS grouping;
* optional discard group;
* unresolved Boundary Set;
* repeated Two-Way CCC over the Boundary Set;
* recursive decomposition;
* multi-stage grouping;
* group-significance measurement;
* assignment-confidence measurement;
* structural stability;
* stopping criteria;
* direct and indirect grouping evidence;
* offline context;
* generated context;
* online context.

### Required Improvements

The existing Two-Way CCC approach should be extended for GTDO in at least two directions.

#### Recursive Boundary Decomposition

```text
Primary Boundary Set
        ↓
Revised Goal / Added Context
        ↓
Secondary Two-Way CCC
        ↓
Refined Groups + New Boundary Set
```

#### Efficient Online Multi-Trigger Matching

The roadmap should investigate:

> Unifying N distances or comparisons into one effective distance or comparison.

This is especially important when many structural trigger points may activate during online dispatch.

---

## 4.2 Point-to-Block Grouping

### Core Algorithm

> Variable-Size Blocks Indexing and Searching

### Target Capability

Recognize and organize contiguous or ordered variable-length regions according to a grouping or dispatch goal.

### Planned Articles

* GTDO-103 — Point-to-Block Grouping by Variable-Size Blocks
* GTDO-107 — Multi-Level Dispatch
* GTDO-109 — Local versus Global Organization

### Engineering Topics

* ordered training data;
* continuity constraints;
* variable-length context regions;
* block recognition;
* block indexing;
* block search;
* nested blocks;
* overlapping candidate regions;
* local versus global block organization;
* block-level responsibility;
* block-level dispatch.

### Initial Position

Variable-Size Blocks Indexing and Searching is considered sufficiently mature to enter GTDO without requiring immediate redesign.

The first task is not algorithm replacement.

It is accurate integration into the GTDO computation-organization framework.

---

## Completion Criteria

This horizon is complete when GTDO has:

* clear definitions of both core grouping modes;
* explicit algorithm mappings;
* controlled boundary outputs;
* significance and stopping policies;
* context-aware grouping;
* an initial computational interface for each mode;
* examples demonstrating when each mode should be used.

---

# 5. Development Horizon III — Boundary Resolution and Fallback Control

## Objective

Build a complete control architecture for data that cannot be assigned confidently to dominant groups.

This horizon is a priority because weak or ambiguous Two-Way CCC separation is unavoidable in realistic data.

---

## 5.1 Boundary Classification

Boundary Sets should be analyzed into distinguishable types.

### Noise Boundary

Malformed, corrupted, irrelevant, duplicated, or structurally invalid data.

Possible action:

```text
Discard
```

### Weak-Evidence Boundary

Potentially relevant data without sufficient confidence for assignment.

Possible actions:

```text
Defer
Add Context
Retry
Fallback
```

### Mixed-Domain Boundary

Data legitimately belonging to multiple responsibilities.

Possible actions:

```text
Multi-Path Assignment
Shared Unit
Boundary Unit
Cross-Domain Unit
```

### Transitional Boundary

Data located between established groups.

Possible actions:

```text
Boundary Brain Unit
Shared Call Path
Additional Structural Recognition
```

### Emerging-Domain Boundary

Repeated unresolved structures that may justify a new computational unit.

Possible action:

```text
Form New Group
Create New Branch
Train New Computational Unit
```

---

## 5.2 Boundary Resolution Strategies

The roadmap should evaluate at least the following strategies.

### Strategy A — Recursive Two-Way CCC

Apply another grouping stage to the Boundary Set.

### Strategy B — Boundary Computational Unit

Train or configure a unit specifically for mixed or cross-domain cases.

### Strategy C — General Fallback Unit

Route unresolved cases to a general model or pre-grouping model.

### Strategy D — Pre-Grouping Data Fallback

Retain a model trained on the original broader dataset.

### Strategy E — Runtime Multi-Path Dispatch

Invoke multiple candidate units and compare or combine their outputs.

### Strategy F — Deferred Organization

Retain data until sufficient context, examples, or organizational value becomes available.

### Strategy G — Controlled Discard

Discard only when evidence indicates low value or invalidity.

---

## 5.3 Weak-Separation Policy

GTDO must define a formal policy for cases in which Two-Way CCC dispatch is not significant.

The policy should consider:

* structural separation;
* assignment confidence;
* group size;
* group stability;
* expected training benefit;
* computational cost;
* general capability loss;
* validation improvement;
* fallback availability.

The framework must explicitly permit:

```text
No Split
```

A valid organizational decision may be to retain the original group.

---

## Planned Articles

* GTDO-105 — Boundary Resolution
* GTDO-108 — Significance and Confidence
* GTDO-204 — Boundary Brain Units
* GTDO-205 — General Fallback Units
* GTDO-407 — Boundary Evolution

## Completion Criteria

This horizon is complete when Boundary Sets have:

* a stable taxonomy;
* multiple resolution policies;
* significance thresholds;
* recursion stopping rules;
* fallback requirements;
* evaluation criteria;
* lifecycle and evolution rules.

---

# 6. Development Horizon IV — Computational Unit Formation

## Objective

Translate organized data groups into explicit computational responsibilities and implementable computational units.

The key transition is:

```text
Training Group
      ↓
Responsibility Candidate
      ↓
Computational Unit Specification
      ↓
Trainable or Callable Capability
```

---

## 6.1 LLM Brain Units

Initial GTDO implementations may focus on:

* domain-specific LLM Brain Units;
* task-specific LLM Brain Units;
* context-specific LLM Brain Units;
* validation Brain Units;
* boundary Brain Units;
* fallback Brain Units;
* coordination Brain Units.

However, the roadmap must prevent LLM implementation from narrowing the general theory.

---

## 6.2 Heterogeneous Computational Units

GTDO should progressively support:

* LLMs;
* smaller language models;
* world models;
* vision models;
* multimodal systems;
* symbolic reasoners;
* planners;
* search engines;
* retrieval systems;
* databases;
* simulators;
* control systems;
* software functions;
* external services;
* agents;
* human experts.

---

## 6.3 Group-to-Unit Decisions

Not every training group requires a separate model.

A group may instead produce:

* a model;
* an adapter;
* a prompt policy;
* a retrieval collection;
* a rule set;
* a symbolic operator;
* a function;
* a routing rule;
* a validation module;
* a shared parameter region;
* a context generator;
* a call-path constraint.

The roadmap should establish engineering criteria for selecting an implementation form.

---

## Planned Articles

* GTDO-201 — From Training Groups to Computational Units
* GTDO-202 — Heterogeneous Computational Units
* GTDO-203 — Brain Units
* GTDO-204 — Boundary Brain Units
* GTDO-205 — General Fallback Units
* GTDO-206 — Computational Responsibility Graphs
* GTDO-209 — Hybrid Computational Organizations

## Completion Criteria

This horizon is complete when GTDO can define:

* what responsibility a group represents;
* whether an independent unit is justified;
* which implementation form is appropriate;
* how the unit is trained;
* how it is invoked;
* how it is validated;
* how it interacts with fallback and neighboring units.

---

# 7. Development Horizon V — Dispatch Trees and Computation Graphs

## Objective

Organize computational units into explicit dispatch structures.

---

## 7.1 Dispatch Trees

A Dispatch Tree represents hierarchical responsibility decomposition.

Example:

```text
General Dispatcher
├── Science
│   ├── Physics
│   └── Biology
├── Engineering
│   ├── Software
│   └── Control
└── Language
    ├── Writing
    └── Translation
```

Each branch should be interpretable as both:

* a dispatch route;
* a responsibility hierarchy;
* a specialization sequence;
* a candidate Call Path.

---

## 7.2 Dispatch Graphs

A tree becomes insufficient when:

* units are shared across branches;
* tasks require multi-domain cooperation;
* one unit validates another;
* multiple paths converge;
* runtime re-entry occurs;
* cross-domain tools are reused.

The architecture should then evolve toward:

> Hybrid Computation Dispatch Graph

---

## 7.3 Computational Responsibility Graph

Before defining execution details, GTDO should represent relationships among responsibilities.

This graph may include:

* parent responsibility;
* sub-responsibility;
* shared responsibility;
* validation responsibility;
* fallback responsibility;
* coordination responsibility;
* boundary responsibility.

---

## Planned Articles

* GTDO-206 — Computational Responsibility Graphs
* GTDO-207 — Dispatch Trees
* GTDO-208 — Dispatch Graphs
* GTDO-209 — Hybrid Computational Organizations
* GTDO-301 — Dispatch Trees as Calling Graphs

## Completion Criteria

This horizon is complete when GTDO supports:

* hierarchical dispatch;
* shared computational units;
* graph-based dispatch;
* fallback edges;
* validation edges;
* cross-domain paths;
* inspectable responsibility relationships.

---

# 8. Development Horizon VI — Call-Path-Based Training and Optimization

## Objective

Replace indiscriminate whole-model optimization with structurally scoped optimization whenever possible.

The central GTDO proposition is:

> In an organized Hybrid AI system, the fundamental optimization target may be a Call Path rather than the whole model.

---

## 8.1 Call Path Definitions

A Call Path may be:

* root-to-leaf;
* root-to-intermediate node;
* an internal graph route;
* a multi-unit cooperative path;
* a fallback path;
* a validation path.

A Call Path Segment may be:

* a prefix;
* a suffix;
* an internal contiguous segment;
* a shared subpath;
* a single computational unit.

---

## 8.2 Optimization Modes

The roadmap should develop:

* Call-Path fine-tuning;
* Call-Path-Segment fine-tuning;
* path-specific reinforcement learning;
* branch-specific reward propagation;
* selective freezing;
* local adapter training;
* local policy updates;
* local data refresh;
* shared-node protection;
* local validation;
* local rollback.

---

## 8.3 Call-Path Reinforcement Learning

A proposed Call-Path Reinforcement Learning process is:

```text
Observed Outcome
        ↓
Reward or Error Signal
        ↓
Identify Responsible Call Path
        ↓
Locate Valid Optimization Scope
        ↓
Update Selected Units or Dispatch Rules
        ↓
Validate Path and Shared Dependencies
        ↓
Release or Roll Back
```

The research program should compare this with:

* whole-model reinforcement learning;
* global fine-tuning;
* parameter-only adaptation;
* mixture-of-experts routing;
* adapter-based tuning.

---

## 8.4 Structural Scope Selection

The smallest valid optimization scope should be preferred.

Possible scopes include:

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

Scope selection should consider:

* causal responsibility;
* dependency impact;
* shared-unit usage;
* expected benefit;
* update cost;
* risk of interference;
* verification cost.

---

## Planned Articles

* GTDO-301 — Dispatch Trees as Calling Graphs
* GTDO-302 — Call Paths
* GTDO-303 — Call-Path Segments
* GTDO-304 — Call-Path Reinforcement Learning
* GTDO-305 — Local Fine-Tuning
* GTDO-306 — Local Validation
* GTDO-307 — Local Versioning
* GTDO-308 — Local Rollback
* GTDO-309 — Structural Scope of Optimization
* GTDO-310 — Summary of Call-Path Optimization

## Completion Criteria

This horizon is complete when GTDO has:

* formal Call Path definitions;
* a local optimization workflow;
* reward-to-path attribution;
* path-level validation;
* local versioning;
* rollback;
* interference monitoring;
* comparisons with whole-model optimization.

---

# 9. Development Horizon VII — Engineering and Control Architecture

## Objective

Develop GTDO as a control-engineering framework rather than an informal organizational metaphor.

---

## 9.1 Goal Function Control

Engineering work should cover:

* goal definition;
* goal versioning;
* goal conflicts;
* multi-goal organization;
* goal priority;
* goal drift;
* goal validation;
* human approval;
* safety constraints.

---

## 9.2 Context Control

GTDO should distinguish:

### Offline Context

* document neighbors;
* source metadata;
* domain structure;
* historic outcomes;
* generated summaries;
* known relationships;
* training provenance.

### Online Context

* user goal;
* active task;
* previous calls;
* runtime state;
* available units;
* latency limits;
* compute limits;
* current confidence;
* environmental conditions.

---

## 9.3 Dispatch Control

Required controls include:

* dispatch confidence;
* dispatch latency;
* branch load;
* unit availability;
* fallback activation;
* multi-path activation;
* dispatch stability;
* dispatch drift;
* routing conflicts;
* dead branches;
* overloaded units.

---

## 9.4 Training Control

Required controls include:

* group size;
* data balance;
* training schedule;
* local versus shared data;
* unit freezing;
* dependency locking;
* evaluation gates;
* release gates;
* rollback points.

---

## 9.5 Lifecycle Control

Each computational unit and path should support:

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

## Planned Articles

* GTDO-401 — Control Engineering for GTDO
* GTDO-402 — Offline Context Organization
* GTDO-403 — Online Context Organization
* GTDO-404 — Training Scheduling
* GTDO-405 — Dispatch Stability
* GTDO-406 — Dispatch Drift
* GTDO-407 — Boundary Evolution
* GTDO-408 — Version Control
* GTDO-409 — Performance Evaluation
* GTDO-410 — Summary of Engineering Architecture

## Completion Criteria

This horizon is complete when GTDO exposes:

* measurable states;
* explicit thresholds;
* controllable transitions;
* observable failures;
* recovery policies;
* versioned artifacts;
* testable release conditions.

---

# 10. Development Horizon VIII — Runtime Hybrid AI Organization

## Objective

Extend GTDO from training-time organization to runtime computation organization.

GTDO should remain distinct from runtime execution frameworks while defining a strong bridge to them.

---

## 10.1 Runtime Dispatch

Runtime dispatch should use:

```text
Input
+ Context
+ Goal
+ Runtime State
+ Available Units
+ Confidence
        ↓
Dispatch Decision
```

---

## 10.2 Runtime Call Paths

Training-time organization should produce runtime-callable structures.

Runtime observations should in turn provide feedback for:

* path improvement;
* group revision;
* new Boundary Sets;
* unit splitting;
* unit merging;
* goal revision;
* dispatch-policy revision.

---

## 10.3 Multi-Agent and Human–AI Organization

The dispatch graph may include:

* multiple AI agents;
* software services;
* control systems;
* human experts;
* approval nodes;
* review nodes;
* collective learning structures.

---

## 10.4 Runtime Organizational Evolution

The system should eventually support:

* adding a new computational unit;
* forming a new branch;
* reorganizing responsibilities;
* promoting a Boundary Set;
* retiring an obsolete unit;
* replacing a path segment;
* creating a shared unit;
* changing fallback policy.

---

## Planned Articles

* GTDO-501 — Runtime Dispatch
* GTDO-502 — Hybrid AI Dispatch Graphs
* GTDO-503 — Multi-Agent Dispatch
* GTDO-504 — Human–AI Organizations
* GTDO-505 — Runtime Organizational Evolution
* GTDO-506 — Runtime Computational Responsibility
* GTDO-507 — Runtime Call Paths
* GTDO-508 — Runtime Structural Optimization
* GTDO-509 — Unified Hybrid AI Organization
* GTDO-510 — Summary of Runtime Organization

## Completion Criteria

This horizon is complete when GTDO supports a closed loop:

```text
Training Organization
        ↓
Runtime Dispatch
        ↓
Observed Outcomes
        ↓
Localized Evaluation
        ↓
Organization Update
        ↓
Improved Training and Runtime Structure
```

---

# 11. Development Horizon IX — Experimental Validation

## Objective

Test whether GTDO produces measurable improvements over unified or weakly organized training.

Experiments should begin with small, inspectable systems.

---

## 11.1 Initial Experimental Questions

* Can RHS-driven grouping improve output precision?
* Can Two-Way CCC identify useful non-contiguous training groups?
* Can Variable-Size Blocks preserve meaningful contextual regions?
* When does recursive boundary decomposition help?
* When should the original group be retained?
* Does a fallback model preserve coverage?
* Can specialized units reduce training cost?
* Can Call-Path optimization improve one capability without damaging unrelated capabilities?
* Does local rollback isolate failure more effectively?
* Can generated context improve dispatch quality?

---

## 11.2 Baseline Comparisons

GTDO experiments should compare:

### Baseline A

One unified dataset and one unified model.

### Baseline B

Random or conventional dataset partitioning.

### Baseline C

Topic or label-based partitioning.

### Baseline D

Mixture-of-experts routing without explicit GTDO organization.

### GTDO A

Point-to-Group Assignment using Two-Way CCC.

### GTDO B

Point-to-Block Grouping using Variable-Size Blocks.

### GTDO C

GTDO with boundary and fallback control.

### GTDO D

GTDO with Call-Path-based local optimization.

---

## 11.3 Evaluation Dimensions

Experiments should measure:

* output quality;
* training time;
* data efficiency;
* inference cost;
* dispatch accuracy;
* group coherence;
* boundary size;
* fallback frequency;
* path stability;
* local improvement;
* cross-domain interference;
* catastrophic forgetting;
* versioning cost;
* rollback success;
* general capability preservation.

---

## 11.4 Recommended Initial Demonstrators

### Demonstrator 1 — Binary RHS Organization

A small corpus with a clear 0/1 grouping goal and an optional discard group.

### Demonstrator 2 — Weak-Separation Boundary

A corpus where binary separation is intentionally ambiguous.

### Demonstrator 3 — Recursive Boundary Resolution

A Boundary Set that becomes separable after additional context.

### Demonstrator 4 — Variable-Size Context Blocks

Ordered data containing variable-length regions associated with different outcomes.

### Demonstrator 5 — LLM Brain Unit Tree

A small set of specialized language units with a general fallback.

### Demonstrator 6 — Call-Path Local Tuning

Improve one selected path while freezing unrelated paths.

### Demonstrator 7 — Heterogeneous Dispatch

Dispatch among an LLM, retrieval system, symbolic validator, and human review unit.

---

# 12. Development Horizon X — Reference Implementation

## Objective

Create a minimal but extensible engineering implementation of GTDO.

The implementation should remain API-first and avoid unnecessary framework dependence.

---

## 12.1 Initial Modules

```text
GoalFunction
TrainingSample
Context
StructuralRecognizer
PointToGroupAssigner
PointToBlockGrouper
BoundaryResolver
DispatchPolicy
ComputationalResponsibility
ComputationalUnit
DispatchTree
DispatchGraph
CallPath
OptimizationScope
Validator
VersionManager
FallbackPolicy
```

---

## 12.2 Initial Processing Pipeline

```text
Input Training Samples
        ↓
Goal Function Evaluation
        ↓
Context Enrichment
        ↓
Grouping Mode Selection
        ↓
Structural Grouping
        ↓
Boundary Resolution
        ↓
Responsibility Construction
        ↓
Computational Unit Mapping
        ↓
Dispatch Structure Construction
        ↓
Validation
        ↓
Export
```

---

## 12.3 Export Formats

The reference implementation should eventually export:

* Markdown reports;
* JSON organization structures;
* Dispatch Tree definitions;
* Dispatch Graph definitions;
* Call Path inventories;
* Boundary reports;
* validation reports;
* training schedules;
* version manifests.

---

## 12.4 Engineering Baseline

The initial implementation may follow the established engineering baseline:

* Java 8;
* JUnit 4;
* API-first design;
* minimal demonstrators;
* deterministic smoke tests;
* Markdown reporting;
* stable package organization;
* explicit interfaces;
* no unnecessary external dependencies.

---

# 13. Development Horizon XI — Formalization

## Objective

Develop a more rigorous mathematical and algebraic representation of GTDO.

This horizon should follow practical clarification rather than precede it.

---

## Planned Formal Topics

* Goal Function Algebra;
* Computational Responsibility Algebra;
* Dispatch Algebra;
* Boundary Algebra;
* Call-Path Algebra;
* Organization Complexity;
* Local Optimization Scope Algebra;
* Group Merge and Split operators;
* responsibility-preserving transformation;
* dispatch-preserving transformation;
* capability-preserving reorganization;
* organization invariants;
* organization degrees of freedom;
* structural confidence;
* operator economy.

---

## Planned Articles

* GTDO-601 — Toward General AI Computation Organization
* GTDO-602 — Computational Responsibility Algebra
* GTDO-603 — Goal Function Algebra
* GTDO-604 — Dispatch Algebra
* GTDO-605 — Organizational Complexity
* GTDO-606 — Self-Organizing Hybrid AI
* GTDO-607 — Evolutionary Computational Organizations
* GTDO-608 — Collective AI Organizations
* GTDO-609 — Open Problems
* GTDO-610 — Grand Summary

---

# 14. Initial Figure Roadmap

The first figure set should establish the conceptual backbone.

## Phase A — Core Figures

* Fig-000 — GTDO Overview
* Fig-001 — From Segmentation to AI Computation Organization
* Fig-002 — Two Core Grouping Modes of GTDO
* Fig-003 — Boundary Set Resolution Architecture
* Fig-004 — Dispatch Tree of Computational Units
* Fig-005 — From Whole-Model Tuning to Call-Path Optimization

## Phase B — Algorithm Figures

* Point-to-Group Assignment by Two-Way CCC
* Recursive Boundary Decomposition
* Point-to-Block Grouping by Variable-Size Blocks
* Significance and Stopping Control
* Offline and Online Context Injection

## Phase C — Organization Figures

* From Training Groups to Computational Units
* LLM Brain Unit Formation
* Heterogeneous Computational Units
* Dispatch Tree to Dispatch Graph
* Computational Responsibility Graph

## Phase D — Call-Path Figures

* Call Path and Call Path Segment
* Reward Propagation Along a Call Path
* Structural Scope of Optimization
* Local Versioning and Rollback
* Shared Unit Protection

## Phase E — Runtime Figures

* Training-Time Organization to Runtime Dispatch
* Hybrid AI Dispatch Graph
* Human–AI Computational Organization
* Runtime Organizational Evolution
* Unified GTDO–Calling Graph–SRAI Architecture

---

# 15. Release Roadmap

## Pre-Release Foundation

Before the first public release, the repository should contain:

* CONSTITUTION;
* OUTLINE;
* ROADMAP;
* GLOSSARY;
* foundational articles;
* core grouping articles;
* boundary-resolution article;
* computational-unit article;
* Dispatch Tree and Call Path articles;
* initial figures;
* README;
* START-HERE;
* CONTENTS;
* FIGURE-INDEX;
* citation metadata;
* release notes.

---

## Release 1.0.0 Target

The first release should establish GTDO as a coherent theory and engineering direction.

Minimum recommended article set:

### Foundations

* GTDO-001
* GTDO-002
* GTDO-003
* GTDO-004

### Core Algorithms

* GTDO-101
* GTDO-102
* GTDO-103
* GTDO-104
* GTDO-105

### Computational Organization

* GTDO-201
* GTDO-202
* GTDO-203

### Call-Path Organization

* GTDO-301
* GTDO-302
* GTDO-303
* GTDO-304

### Engineering

* GTDO-401

The release should include enough content to demonstrate the complete conceptual chain:

```text
Goal Function
    ↓
Grouping
    ↓
Boundary Resolution
    ↓
Computational Responsibility
    ↓
Computational Units
    ↓
Dispatch Structure
    ↓
Call Path
    ↓
Localized Optimization
```

---

## Post-1.0 Development

Later releases may add:

* detailed Two-Way CCC improvements;
* optimized multi-trigger matching;
* Variable-Size Blocks implementation;
* experiments;
* Java reference implementation;
* heterogeneous unit dispatch;
* runtime evolution;
* formal algebra;
* case studies;
* integration with SRAI and Calling Graph systems.

---

# 16. Immediate Work Plan

The immediate repository-building sequence is:

## Batch A — Constitutional Foundation

* CONSTITUTION.md
* OUTLINE.md
* ROADMAP.md
* GLOSSARY.md

## Batch B — Foundational Articles

* GTDO-001
* GTDO-002
* GTDO-003
* GTDO-004

## Batch C — Core Algorithms

* GTDO-101
* GTDO-102
* GTDO-103
* GTDO-104
* GTDO-105

## Batch D — Computational Units

* GTDO-201
* GTDO-202
* GTDO-203

## Batch E — Call Paths

* GTDO-301
* GTDO-302
* GTDO-303
* GTDO-304

## Batch F — Initial Control Architecture

* GTDO-401

## Batch G — Core Figures

* Fig-000 through Fig-005

## Batch H — Navigation and Release Kit

* README.md
* START-HERE.md
* CONTENTS.md
* FIGURE-INDEX.md
* CHANGELOG.md
* CITATION.cff
* `.zenodo.json`
* GitHub Release Notes
* ResearchGate Release Text

---

# 17. Open Research Priorities

The following questions have high priority.

1. How should grouping significance be measured?
2. When should Two-Way CCC return no split?
3. How should the Boundary Set be recursively processed?
4. When should a Boundary Set become a Brain Unit?
5. How can N online comparisons be unified into one comparison?
6. How should offline and generated context be selected?
7. How should multiple computational responsibilities be assigned?
8. How should shared Brain Units be protected during local tuning?
9. How should reward be attributed to a Call Path?
10. How should a Call Path Segment be selected as an optimization scope?
11. How should GTDO preserve general capability while increasing specialization?
12. How should heterogeneous computational units be evaluated under one dispatch architecture?
13. How should dispatch drift be detected?
14. How should local versions and rollback be coordinated?
15. Which organizational invariants must be preserved during evolution?
16. How can Variable-Size Blocks support long-context training organization?
17. How should GTDO integrate human experts without reducing them to passive fallback?
18. How can GTDO support self-organizing Hybrid AI while retaining engineering control?

---

# 18. Long-Term Vision

GTDO begins by organizing training examples according to an RHS grouping goal.

Its long-term path is broader:

```text
Training Examples
        ↓
Goal-Oriented Groups
        ↓
Computational Responsibilities
        ↓
Specialized and General Units
        ↓
Dispatch Trees and Graphs
        ↓
Call Paths
        ↓
Local Training and Reinforcement
        ↓
Runtime Hybrid AI
        ↓
Evolving Computational Organizations
```

The final objective is not maximal decomposition.

It is not the replacement of general models by isolated specialist models.

It is not the creation of increasingly complex routing machinery.

The objective is:

> To make AI computation explicitly organized, structurally scoped, locally improvable, globally cooperative, verifiable, and evolvable.

GTDO should help move AI engineering from:

```text
One Dataset
    ↓
One Large Model
    ↓
Global Training
    ↓
Global Risk
```

toward:

```text
Goal-Oriented Data
        ↓
Explicit Responsibilities
        ↓
Organized Computational Units
        ↓
Controllable Call Paths
        ↓
Localized Optimization
        ↓
Verified Hybrid Intelligence
```

---

# 19. Closing Roadmap Principle

The GTDO roadmap should always preserve the following direction:

```text
Do not organize data merely to produce groups.

Organize data to reveal responsibility.

Organize responsibility to form computation.

Organize computation to create controllable paths.

Optimize paths to support local evolution.

Connect local evolution to a coherent Hybrid AI organization.
```

> GTDO is a roadmap from training-data grouping to general AI computation organization.
