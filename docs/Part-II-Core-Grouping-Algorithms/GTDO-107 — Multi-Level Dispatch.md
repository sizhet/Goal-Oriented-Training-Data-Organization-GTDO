# GTDO-107 — Multi-Level Dispatch

## Abstract

As AI systems evolve from isolated models into Hybrid AI organizations, computational dispatch becomes increasingly complex. A single dispatch decision is often insufficient for solving real-world tasks. Instead, computation proceeds through a hierarchy of organizational levels, where each level performs dispatch according to its own objectives and responsibilities.

Goal-Oriented Training Data Organization (GTDO) introduces **Multi-Level Dispatch**, a runtime organization mechanism in which computational decisions are made across multiple layers of abstraction. High-level dispatch determines organizational direction, while lower-level dispatch coordinates specialized Computational Units that execute concrete tasks.

Rather than viewing dispatch as a single routing operation, GTDO models it as a hierarchical organizational process that continuously refines computation toward increasingly specialized execution.

---

#### Fig-105-Dispatch-Tree-Example.png

![Fig-105-Dispatch-Tree-Example.png](../figures/Fig-105-Dispatch-Tree-Example.png)

---

# Why Single-Level Dispatch Is Insufficient

Simple systems often dispatch directly from an input to an execution module.

For example:

User Request

↓

Language Model

↓

Response

This architecture works well for relatively simple tasks but becomes increasingly inefficient as computational diversity grows.

Modern Hybrid AI systems may include:

- Retrieval Units
- Planning Units
- Symbolic Reasoning Units
- Vision Units
- Simulation Units
- Brain Units
- Validation Units
- External Services

A single dispatch decision cannot efficiently organize such heterogeneous resources.

Dispatch itself must therefore become hierarchical.

---

# Hierarchical Computational Organizations

Large organizations naturally divide responsibilities across multiple levels.

Human organizations provide familiar examples:

Executive Management

↓

Department Managers

↓

Project Leaders

↓

Engineering Teams

↓

Individual Engineers

Each level makes decisions appropriate to its organizational scope.

GTDO applies the same organizational principle to computational systems.

---

# Levels of Dispatch

A typical GTDO runtime may contain several dispatch levels.

### Level 1 — Goal Dispatch

Determines the overall computational objective.

Examples:

- answer a question
- generate software
- solve a planning problem
- analyze scientific data

This level selects the overall computational strategy.

---

### Level 2 — Organizational Dispatch

Determines which major Computational Organizations should participate.

Examples:

- Retrieval Organization
- Planning Organization
- Knowledge Organization
- Brain Unit Organization
- Validation Organization

At this level, computation is distributed among major organizational components.

---

### Level 3 — Unit Dispatch

Within each organization, computation is assigned to individual Computational Units.

Examples include:

- retrieval unit
- ranking unit
- reasoning unit
- summarization unit
- translation unit

Each unit performs specialized computation.

---

### Level 4 — Local Dispatch

Individual Computational Units may themselves perform additional dispatch.

Examples:

- selecting algorithms
- invoking specialized models
- querying databases
- executing verification routines

Dispatch therefore continues recursively inside each unit.

---

# Recursive Dispatch

One important characteristic of Multi-Level Dispatch is recursion.

A dispatched Computational Unit is not necessarily the final executor.

Instead, it may become another dispatcher.

For example:

User Goal

↓

Planning Unit

↓

Reasoning Unit

↓

Knowledge Unit

↓

Validation Unit

↓

Response Generation

Each level continues organizing computation until the objective is achieved.

Dispatch therefore propagates through the computational organization.

---

# Context-Dependent Dispatch

Different execution contexts may produce different dispatch hierarchies.

For example, answering:

"What is the capital of Japan?"

may require:

Goal Dispatch

↓

Retrieval

↓

Validation

↓

Response

Whereas solving a complex engineering problem may require:

Goal Dispatch

↓

Planning

↓

Knowledge Discovery

↓

Simulation

↓

Validation

↓

Explanation

The hierarchy emerges dynamically from runtime requirements rather than being predetermined.

---

# Dispatch Granularity

Different levels operate at different computational granularity.

Higher levels manage broad organizational decisions.

Lower levels manage increasingly detailed computational activities.

Examples include:

High-Level

- organizational strategy
- responsibility allocation
- resource selection

Mid-Level

- team coordination
- computational specialization
- workflow construction

Low-Level

- algorithm selection
- parameter configuration
- execution scheduling

Granularity naturally increases as computation progresses.

---

# Collaboration Across Levels

Higher levels establish direction.

Lower levels contribute specialized execution.

Information continuously flows between them.

Higher levels provide:

- goals
- priorities
- constraints
- organizational policies

Lower levels return:

- results
- confidence
- progress
- resource consumption
- exception reports

Multi-Level Dispatch therefore supports both top-down coordination and bottom-up feedback.

---

# Dispatch Trees

One convenient representation of Multi-Level Dispatch is the Dispatch Tree.

Each node represents a dispatch decision.

Each branch represents an organizational decomposition.

Leaves represent executable Computational Units.

As computation proceeds, Dispatch Trees evolve into executable Calling Graphs that describe actual runtime behavior.

This transformation connects organizational planning with computational execution.

---

# Multi-Level Dispatch in Hybrid AI

Hybrid AI systems naturally contain heterogeneous computational capabilities.

Examples include:

- Large Language Models
- symbolic reasoning engines
- planning systems
- simulation frameworks
- retrieval databases
- Brain Units
- verification modules
- external APIs

Different organizational levels determine how these heterogeneous resources cooperate.

Rather than relying upon centralized control, Multi-Level Dispatch distributes decision-making throughout the computational organization.

---

# Relationship to Goal Engineering

Goal Function Engineering defines:

> What should be achieved?

Multi-Level Dispatch determines:

> How organizational responsibilities should be distributed to achieve it.

Together they provide both direction and execution for Hybrid AI systems.

Goals establish organizational intent.

Dispatch organizes computational realization.

---

# Implications

Multi-Level Dispatch transforms computation from a linear execution pipeline into a hierarchical organizational process.

Instead of a single dispatcher controlling every decision, responsibility is progressively delegated across multiple computational levels.

This organizational structure improves scalability, modularity, adaptability, explainability, and runtime efficiency while allowing Hybrid AI systems to coordinate increasingly diverse Computational Units.

---

# Key Takeaways

- Multi-Level Dispatch organizes computation through hierarchical runtime decision-making.
- Different dispatch levels operate at different organizational and computational granularity.
- Computational Units may themselves become dispatchers, enabling recursive organizational structures.
- Dispatch hierarchies emerge dynamically according to runtime goals and context.
- Dispatch Trees provide a natural representation of hierarchical computational organization.
- Multi-Level Dispatch is a foundational mechanism for scalable Hybrid AI and Goal-Oriented Training Data Organization.