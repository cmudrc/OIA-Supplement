# Coding Protocol

This document describes the coding protocol used to extract attributes and assign taxonomy classifications for the 30 multi-agent system (MAS) frameworks analyzed in the paper.

## Overview

Attribute coding was performed by a single coder using a fixed coding scheme established prior to data extraction. This approach is appropriate for primarily extractive coding tasks where attributes are directly reported in source materials rather than requiring interpretive judgment. For the two taxonomy dimensions (Organizational Structure and Operational Methodology), decision trees with explicit classification criteria were used to minimize subjectivity and ensure consistent application across all frameworks.

## Information Sources

For each paper, the coder examined the following sources in order:

1. **Main text** — Methods, system architecture, and results sections
2. **Figures and diagrams** — Architecture diagrams, workflow figures, agent interaction illustrations
3. **Appendices** — Supplementary technical details
4. **Supplementary materials** — Extended methods, additional figures
5. **Code repositories** — When publicly available and linked in the paper

## Attribute-Specific Coding Rules

### 1. Orchestration Framework

| Condition | Coding Rule |
|-----------|-------------|
| Framework explicitly named (e.g., "built using AutoGen") | Record named framework |
| Framework implied by citation or import statements | Record inferred framework with verification |
| No framework mentioned but custom implementation described | Record as "Custom" |
| No framework mentioned and no implementation details | Record as "Not Specified" |

### 2. Organizational Structure (Original Labels)

The original organizational structure labels were extracted verbatim from papers where explicitly stated. When papers did not explicitly describe organizational structure, labels were inferred from:

- Agent role names (e.g., "Manager," "Supervisor," "Coordinator" suggest hierarchy)
- Communication patterns described or depicted in diagrams
- Task allocation mechanisms described in methods

Papers requiring inference were flagged in the dataset (approximately 33% of corpus).

### 3. Organizational Structure (Taxonomy Classification)

Taxonomy classification used the decision tree presented in Figure 3 of the paper:

```
START
  │
  ▼
Is there a dedicated orchestration agent
(manager/supervisor/coordinator)?
  │
  ├─ YES → ORCHESTRATED
  │
  └─ NO
      │
      ▼
    Is execution order predetermined
    with fixed stage transitions?
      │
      ├─ YES → SEQUENTIAL
      │
      └─ NO → NETWORKED
```

**Classification criteria:**

| Classification | Required Evidence |
|----------------|-------------------|
| **Orchestrated** | Explicit orchestrator/manager/supervisor agent whose primary role is coordination; hierarchical terminology; central control of task assignment |
| **Sequential** | Explicitly described stages/phases/pipelines; linear workflow with handoffs; V-Model or similar process framework |
| **Networked** | Group chat or blackboard architecture; peer-to-peer communication; collaborative terminology without central coordinator |

### 4. Cognitive & Reasoning Protocols

Recorded all reasoning strategies explicitly mentioned in the paper, including:
- Named techniques (Chain-of-Thought, ReAct, Tree-of-Thoughts, RAG, Reflexion)
- Described mechanisms (self-correction, planning, task decomposition)

When multiple techniques were used, all were recorded.

### 5. Operational Methodologies (Original Labels)

Original workflow descriptions were extracted verbatim from papers, capturing terminology used by authors (e.g., "closed-loop," "iterative refinement," "V-Model workflow").

### 6. Operational Methodologies (Taxonomy Classification)

Taxonomy classification used the decision tree presented in Figure 4 of the paper:

```
START
  │
  ▼
Does the system use dynamic routing logic,
state machines, or conditional branching
to determine execution paths?
  │
  ├─ YES → GRAPH-ROUTED
  │
  └─ NO
      │
      ▼
    Does the system follow a prescribed
    phase sequence or pipeline?
      │
      ├─ YES → STAGED-PIPELINE
      │
      └─ NO → ITERATIVE-FEEDBACK
```

**Classification criteria:**

| Classification | Required Evidence |
|----------------|-------------------|
| **Graph-Routed** | Explicit graph structures for task representation; router agents; state machines (FSM); dynamic path selection based on intermediate results |
| **Staged-Pipeline** | Named sequential stages/phases; pipeline terminology; engineering process model adoption (V-Model, MBSE); prescribed workflow sequence |
| **Iterative-Feedback** | Explicit feedback loops; self-correction/reflection cycles; iteration until convergence or quality threshold; "closed-loop" terminology |

### 7. State Representation & Memory

Recorded all memory mechanisms described, categorized as:
- Short-term (context window, conversation history)
- Long-term (vector databases, knowledge graphs, persistent storage)
- Structured (JSON, state graphs, design representations)

When no memory mechanism was described, recorded as "Not Specified" or "Context Window" if standard LLM usage was implied.

### 8. Modality

Recorded all input/output types explicitly mentioned:
- Text (universal across all frameworks)
- Code (Python, Modelica, etc.)
- Images (sketches, renderings, plots)
- 3D Geometry (CAD, STL, point clouds)
- Simulation data (FEA results, CFD outputs)
- Domain-specific formats (netlists, waveforms)

### 9. Number of Agents

| Condition | Coding Rule |
|-----------|-------------|
| Fixed count explicitly stated | Record exact number |
| Range provided (e.g., "5-7 agents") | Record as range |
| Variable based on task | Record as "Variable" with notes |
| Count inferable from agent list | Count named agents |

All papers in the corpus reported agent counts either explicitly or through enumeration of agent roles.

### 10. Asimow Design Phase Coverage

Phase coverage was determined by mapping described system capabilities to Asimow's three phases based on definitions from the original work (Asimow, 1962):

| Phase | Definition | Indicators |
|-------|------------|------------|
| **Analysis** | Requirements definition, problem formulation, constraint identification | Requirements elicitation, specification parsing, constraint extraction |
| **Synthesis** | Artifact creation, design generation, solution development | CAD generation, code synthesis, design space exploration |
| **Evaluation** | Verification, validation, testing, performance assessment | Simulation validation, safety checking, performance verification, quality assessment |

Papers were coded as covering a phase if system capabilities explicitly addressed that phase's activities.

## Quality Assurance

1. **Fixed coding scheme**: All coding rules were established prior to data extraction and applied consistently across all 30 frameworks.

2. **Decision tree application**: Taxonomy classifications used explicit decision trees with binary decision points, reducing subjective judgment.

3. **Source triangulation**: When primary text was ambiguous, supplementary materials, figures, and code repositories were consulted to verify classifications.

4. **Transparent inference flagging**: Papers requiring inference for organizational structure (rather than explicit statement) were flagged in the dataset.

## Limitations

- Single-coder design limits assessment of inter-rater reliability; however, the primarily extractive nature of coding and use of decision trees mitigates subjectivity concerns.
- Papers with limited methodological detail may have less reliable classifications despite inference procedures.
- Rapidly evolving terminology in MAS literature may result in inconsistent usage across papers that our fixed coding scheme could not fully accommodate.

## References

Asimow, M. (1962). *Introduction to Design*. Prentice-Hall.
