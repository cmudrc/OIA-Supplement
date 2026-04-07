# Classification Rationale

This document provides taxonomy definitions and per-paper rationale for the organizational structure and operational methodology classifications used in the paper "Organizationally-Intelligent Agents: Connecting Multi-Agent Engineering Systems to Organizational Design Theory."

## Taxonomy Definitions

### Organizational Structure

| Category | Definition | Coordination Mechanism | Identifying Features |
|----------|------------|----------------------|---------------------|
| **Orchestrated** | Explicit orchestrator, manager, or supervisor agent whose primary role is coordinating other agents | Centralized decision-making with delegated execution; orchestrator routes tasks, controls information flow, and coordinates timing | Explicit orchestrator/manager/supervisor agents; hierarchical terminology; central control of task assignment |
| **Networked** | Peer agents communicating through shared state, message passing, or blackboard architectures without centralized coordinator | Distributed coordination via shared memory/blackboard or direct agent-to-agent messaging; coordination emerges from interactions | Group chat architectures; shared state or blackboard; peer-to-peer communication; collaborative terminology |
| **Sequential** | Pipeline or workflow architectures where agents execute in predetermined order with explicit stage-to-stage handoffs | Fixed execution sequences with defined stage transitions; agents activate in prescribed order | Explicitly described stages/phases/pipelines; linear workflow descriptions; V-Model implementations |

### Operational Methodology

| Category | Definition | Control Mechanism | Identifying Features |
|----------|------------|------------------|---------------------|
| **Iterative-Feedback** | Repeated generation-evaluation-refinement cycles until convergence or quality thresholds are met | Convergence-based iteration with closed-loop refinement driven by quality assessment | Explicit feedback loops; self-correction/reflection; iteration based on quality; "closed-loop" or "refinement" terminology |
| **Graph-Routed** | Dynamic task execution where next step is determined by routing logic, state machines, or conditional branching | Task graphs with nodes and edges where execution paths are determined dynamically | Explicit graph structures; router agents; state machines (FSM); dynamic path selection |
| **Staged-Pipeline** | Fixed sequences of distinct phases with prescribed transitions between stages | Predefined workflow phases executed in order; output of stage N becomes input of stage N+1 | Named sequential stages; pipeline terminology; engineering process model adoption (V-Model) |

---

## Per-Paper Classification Rationale

### 1. feng2025turbulence
**turbulence.ai: an end-to-end AI Scientist for fluid mechanics**

| Dimension | Classification | Rationale |
|-----------|---------------|-----------|
| Organizational Structure | **Sequential** | The system follows a "three-stage, multi-agent architecture" (Idea Generation, Simulation, Draft Write-Up) with linear stage-to-stage handoffs. |
| Operational Methodology | **Staged-Pipeline** | The process unfolds through "five distinct phases" orchestrated to transform raw experimental data into a structured manuscript. |

**Key Identifying Features:**
- OpenFOAMGPT 2.0 simulation pipeline
- VLM-based "AI Reviewer" feedback
- Automated LaTeX source synthesis

---

### 2. ni2024mechagents
**MechAgents: Large language model multi-agent collaborations can solve mechanics problems**

| Dimension | Classification | Rationale |
|-----------|---------------|-----------|
| Organizational Structure | **Networked** | Agents communicate via "autonomous, interactive and dynamic group chatting" where the topology is flexible and allows for mutual correction. |
| Operational Methodology | **Iterative-Feedback** | Employs self-correction and mutual correction loops where agents analyze and debug simulation scripts iteratively until correct results emerge. |

**Key Identifying Features:**
- Group chat manager agent
- Division of labor between Scientist and Engineer roles
- FEniCS simulation tool integration

---

### 3. cui2024large
**Large Language Models based Multi-Agent Framework for Objective Oriented Control Design in Power Electronics**

| Dimension | Classification | Rationale |
|-----------|---------------|-----------|
| Organizational Structure | **Orchestrated** | The "Manager Agent" parses user demands and "assigns the various tasks and requirements to the relevant functional agents." |
| Operational Methodology | **Staged-Pipeline** | Decomposes the process into sequential sub-tasks: task planning, modeling, controller design, simulation, and verification. |

**Key Identifying Features:**
- Manager Agent coordinator
- Objective-oriented sub-task decomposition
- Modelica model templates

---

### 4. ghafarollahi2024rapid
**Rapid and Automated Alloy Design with Graph Neural Network-Powered LLM-Driven Multi-Agent Systems**

| Dimension | Classification | Rationale |
|-----------|---------------|-----------|
| Organizational Structure | **Orchestrated** | The "Assistant" serves as the "central agent" that coordinates planning and calls specialized tools based on a master plan. |
| Operational Methodology | **Iterative-Feedback** | Follows a planning-execution-analysis cycle where a Reviewer agent provides iterative feedback to the Planner until the alloy design is optimized. |

**Key Identifying Features:**
- Assistant central coordinator
- GNN-powered physics prediction tool
- JSON-formatted structural models

---

### 5. hu2024multi
**A Multi-agent Framework for Materials Laws Discovery**

| Dimension | Classification | Rationale |
|-----------|---------------|-----------|
| Organizational Structure | **Sequential** | Agents operate within a workflow where handoffs occur between "generation," "translation," and "reflection" nodes in a linear path. |
| Operational Methodology | **Iterative-Feedback** | Repeated DFS processes are used to generate and refine formulas, with the best results stored in "long-term memory" for subsequent iterations. |

**Key Identifying Features:**
- Depth-First Search (DFS) trajectories
- Formula Memory state
- Tree-of-Thought (ToT) prompting

---

### 6. kant2025develop
**Develop AI Agents for System Engineering in Factorio**

| Dimension | Classification | Rationale |
|-----------|---------------|-----------|
| Organizational Structure | **Orchestrated** | Built on the "Viable System Model" (VSM) which utilizes hierarchical structures to handle increasing layers of systemic policy and planning. |
| Operational Methodology | **Iterative-Feedback** | Emphasizes "continuous integration and rapid feedback loops" to maintain healthy dynamic equilibrium within the simulation environment. |

**Key Identifying Features:**
- Viable System Model (VSM) levels 1-5
- Science Per Minute (SPM) benchmark
- Law of Requisite Variety (LRV)

---

### 7. ocker2025idea
**From Idea to CAD: A Language Model-Driven Multi-Agent System for Collaborative Design**

| Dimension | Classification | Rationale |
|-----------|---------------|-----------|
| Organizational Structure | **Orchestrated** | The "RequirementsEngineer" serves as the primary interface coordinating the "CadEngineer" and "QualityAssuranceEngineer." |
| Operational Methodology | **Staged-Pipeline** | Explicitly mirrors the "V-model" phases: requirements elicitation, design, verification, and validation. |

**Key Identifying Features:**
- V-model phase mirroring
- RequirementsEngineer interface
- Visual-based quality feedback loop

---

### 8. tian2025multi
**A Multi-Agent Framework Integrating Large Language Models and Generative AI for Accelerated Metamaterial Design**

| Dimension | Classification | Rationale |
|-----------|---------------|-----------|
| Organizational Structure | **Orchestrated** | Features a "Supervisor" who "oversees the entire process" to ensure alignment with properties and suggests restart points. |
| Operational Methodology | **Staged-Pipeline** | Follows a "structured three-step framework" design process involving architectural synthesis, fine-tuning, and cohesive generation. |

**Key Identifying Features:**
- Supervisor overseer agent
- Three-step fine-tuning framework
- Dall-E 3 prompt refinement

---

### 9. ho2025marco
**Marco: Configurable Graph-Based Task Solving and Multi-AI Agents Framework for Hardware Design**

| Dimension | Classification | Rationale |
|-----------|---------------|-----------|
| Organizational Structure | **Orchestrated** | Uses a "Group Manager" within a "Hierarchical Collaboration" structure to decide which single or multi-AI agent solves a sub-task. |
| Operational Methodology | **Graph-Routed** | Employs "configurable graph-based task solving" where execution flow and task dependencies are defined by edges within a graph. |

**Key Identifying Features:**
- Configurable Task Graphs
- Multi-AI agent debate nodes
- TCRG-based task planner

---

### 10. bogachov2025lightweight
**A Lightweight Multi-Expert Generative Language Model System for Engineering Information and Knowledge Extraction**

| Dimension | Classification | Rationale |
|-----------|---------------|-----------|
| Organizational Structure | **Orchestrated** | An "orchestrator" node receives the query and "routes it to the most relevant expert node" within the graph architecture. |
| Operational Methodology | **Graph-Routed** | The methodology is "based on graphs" where query path selection is determined by the orchestrator matching domain-specific expert names. |

**Key Identifying Features:**
- Orchestrator routing node
- Knowledge isolation strategy
- Expert nodes for subsections (Fuselage, Wing, etc.)

---

### 11. chen2025menter
**MenTeR: A fully-automated Multi-agenT workflow for end-to-end RF/Analog Circuits Netlist Design**

| Dimension | Classification | Rationale |
|-----------|---------------|-----------|
| Organizational Structure | **Orchestrated** | Features a "Meta Agent serving as the central orchestrator" that analyzes tasks and delegates sub-components to specialized specialists. |
| Operational Methodology | **Iterative-Feedback** | Employs "self-referential iteration" where validation errors from the Testbench or Executor are routed back to the Circuit Agent for refinement. |

**Key Identifying Features:**
- Meta Agent orchestrator
- Chain-of-Stage (CoS) reasoning
- Circuit Think Tank repository

---

### 12. youwai2025investigating
**Investigating the Potential of Large Language Model-Based Router Multi-Agent Architectures for Foundation Design Automation**

| Dimension | Classification | Rationale |
|-----------|---------------|-----------|
| Organizational Structure | **Orchestrated** | Employs a "routing agent framework" to classify design problems and direct tasks to specialized domain-expert agents. |
| Operational Methodology | **Graph-Routed** | The workflow initiates with a "classification node" that routes the task to a pre-configured agent path based on foundation type. |

**Key Identifying Features:**
- Router agent classifier
- Designer-Checker multi-agent architecture
- Dual-tier text classification framework

---

### 13. jin2025closed
**A Closed-Loop Multi-Agent Framework for Aerodynamics-Aware Automotive Styling Design**

| Dimension | Classification | Rationale |
|-----------|---------------|-----------|
| Organizational Structure | **Networked** | Comprises a team of "collaborative sub-agents" that work together to translate high-level requirements into market insights. |
| Operational Methodology | **Iterative-Feedback** | Follows a "search-reflect" iterative loop where queries are continuously optimized based on ongoing analysis of market trends. |

**Key Identifying Features:**
- Search-reflect iterative loop
- Competitive Analysis Agents
- Design Package state mapping

---

### 14. liang2025automating
**Automating Structural Engineering Workflows with Large Language Model Agents**

| Dimension | Classification | Rationale |
|-----------|---------------|-----------|
| Organizational Structure | **Orchestrated** | Framework is defined by "fully agentic hierarchies" with specialized roles (Analyst, Engineer, Manager) coordinated via AutoGen. |
| Operational Methodology | **Staged-Pipeline** | Operationalizes "professional workflows" by mirroring end-to-end consulting firm sequences from data loading to safety decisions. |

**Key Identifying Features:**
- Consultancy Team structure (Analyst/Engineer/Management)
- Safety Manager decision role
- Structured Memory Manager

---

### 15. xu2025engineering
**Engineering.ai: A Platform for Teams of AI Engineers in Computational Design**

| Dimension | Classification | Rationale |
|-----------|---------------|-----------|
| Organizational Structure | **Orchestrated** | Architecture consists of a "Chief Engineer" serving as the "central coordinator managing the entire team." |
| Operational Methodology | **Staged-Pipeline** | Transforms natural language requirements into computational workflows through "intelligent task decomposition and parallel execution strategies." |

**Key Identifying Features:**
- Chief Engineer central coordinator
- Specialized engineering agents (Aerodynamics, Structural, etc.)
- File-mediated data exchange

---

### 16. kumar2025toward
**Toward Autonomous Engineering Design: A Knowledge-Guided Multi-Agent Framework**

| Dimension | Classification | Rationale |
|-----------|---------------|-----------|
| Organizational Structure | **Orchestrated** | A human "Manager" acts as an orchestrator/gatekeeper determining when design cycles conclude, while AI agents fulfill delegated tasks. |
| Operational Methodology | **Iterative-Feedback** | Employs a continuous "feedback loop" between the Design Engineer and Systems Engineer for refinements until requirements are met. |

**Key Identifying Features:**
- Graph Ontologist agent
- Systems Engineer reviewer
- Knowledge Graph-guided reasoning

---

### 17. guo2025multidisciplinary
**A Multidisciplinary Design and Optimization (MDO) Agent Driven by Large Language Models**

| Dimension | Classification | Rationale |
|-----------|---------------|-----------|
| Organizational Structure | **Orchestrated** | Semi-automates workflows by "orchestrating three core capabilities" through a synergistic team of specialized designer and modeler agents. |
| Operational Methodology | **Iterative-Feedback** | Employs a "Thought-Action-Observation" loop where agents invoke FEA tools and evaluate performance variants until optimization is achieved. |

**Key Identifying Features:**
- Designer/Modeler/Verifier/Optimizer roles
- ReAct reasoning framework
- Visual self-correction mechanism

---

### 18. jin2025gridmind
**GridMind: LLMs-Powered Agents for Power System Analysis and Operations**

| Dimension | Classification | Rationale |
|-----------|---------------|-----------|
| Organizational Structure | **Orchestrated** | Architecture features specialized domain agents working under an "agent coordinator" that manages inter-agent communication and context. |
| Operational Methodology | **Iterative-Feedback** | Implements a "reason-act-reflect" loop where agents validate numerical results from solvers and trigger recovery paths if errors are detected. |

**Key Identifying Features:**
- Agent Coordinator
- PydanticAI schema validation
- IEEE standard test case integration

---

### 19. liao2024autoforma
**AutoForma: A Large Language Model-Based Multi-Agent for Computer-Automated Design**

| Dimension | Classification | Rationale |
|-----------|---------------|-----------|
| Organizational Structure | **Sequential** | Workflow consists of specialized agents performing tasks across "four primary stages" with specific handoffs between analysis and execution. |
| Operational Methodology | **Staged-Pipeline** | Follows a fixed sequence of phases (Requirement Analysis, Planning, Coding, Execution) to automate CAD model generation. |

**Key Identifying Features:**
- Requirement Analyst agent
- CadQuery Vector Database
- Executor agent verification

---

### 20. ding2023designgpt
**DesignGPT: Multi-Agent Collaboration in Design**

| Dimension | Classification | Rationale |
|-----------|---------------|-----------|
| Organizational Structure | **Networked** | Simulates a "Meeting Room" environment where agents representing different professional roles (PM, Director, CMF) collaborate through group discussion. |
| Operational Methodology | **Iterative-Feedback** | Uses standardized operating procedures and peer reflection to refine design concepts based on consensual assessment criteria. |

**Key Identifying Features:**
- Meeting room collaboration model
- CMF Designer role
- Stable Diffusion image synthesis

---

### 21. mushtaq2025harnessing
**Harnessing Multi-Agent LLMs for Complex Engineering Problem-Solving: A Framework for Senior Design Projects**

| Dimension | Classification | Rationale |
|-----------|---------------|-----------|
| Organizational Structure | **Orchestrated** | Uses a "centralized control mechanism managed by a Coordinator Agent" who oversees and reassigns tasks to specialized perspective experts. |
| Operational Methodology | **Iterative-Feedback** | The Coordinator evaluates agent outputs against standards and redirects tasks for refinement with "refined sub-goals" if quality gates aren't met. |

**Key Identifying Features:**
- Coordinator Agent overseer
- Task Channel distribution
- Perspective agents (Innovation, Ethics, etc.)

---

### 22. panta2025meda
**MEDA: A Multi-Agent System For Parametric CAD Model Creation**

| Dimension | Classification | Rationale |
|-----------|---------------|-----------|
| Organizational Structure | **Orchestrated** | Orchestrated by a "group chat manager" who selects the next agent based on a specific transition policy for logical sequencing. |
| Operational Methodology | **Graph-Routed** | Employs a "finite state machine (FSM) that constrains agent transitions" during the conversation to ensure robust and reproducible outcomes. |

**Key Identifying Features:**
- FSM transition policy
- Script Execution Reviewer
- CAD Image Reviewer

---

### 23. wang2025llm
**An LLM-enabled Multi-Agent Autonomous Mechatronics Design Framework**

| Dimension | Classification | Rationale |
|-----------|---------------|-----------|
| Organizational Structure | **Orchestrated** | Features a "hierarchical architecture governed by a High-Level Planning Agent" that decomposes challenges into tasks for domain specialists. |
| Operational Methodology | **Staged-Pipeline** | Follows a "language-driven workflow" where requirements are systematically translated through mechanical, electronic, and software stages. |

**Key Identifying Features:**
- High-Level Planning Agent
- COMSOL-MATLAB simulator interface
- Structured human feedback loop

---

### 24. ghafarollahi2025automating
**Automating Alloy Design and Discovery with Physics-Aware Multimodal Multiagent AI**

| Dimension | Classification | Rationale |
|-----------|---------------|-----------|
| Organizational Structure | **Orchestrated** | A "Group chat manager" selects speakers while a team of core agents (Planner, Critic) coordinates task approval and tool execution. |
| Operational Methodology | **Iterative-Feedback** | Plans are iteratively "evaluated and approved" by a critic, and agents iterate on molecular simulations to refine material properties based on plot analysis. |

**Key Identifying Features:**
- Physics-aware multimodal agents
- Plot analyzer agent
- LAMMPS simulation tool use

---

### 25. ataei2025elicitron
**Elicitron: A Large Language Model Agent-Based Simulation Framework for Design Requirements Elicitation**

| Dimension | Classification | Rationale |
|-----------|---------------|-----------|
| Organizational Structure | **Sequential** | Uses a "serial" generation approach where agents are created in sequence to ensure that previous generations serve as persistent context. |
| Operational Methodology | **Staged-Pipeline** | Process mirrors real-world phases of gathering requirements: Agent Generation, Simulation, Agent Interview, and Needs Identification. |

**Key Identifying Features:**
- Action-Observation-Challenge (AOC) chain
- Pydantic model constraints
- Diversity sampling (K-means filtering)

---

### 26. chen2025cost
**A Cost-Aware Multi-Agent System for Black-Box Design Space Exploration**

| Dimension | Classification | Rationale |
|-----------|---------------|-----------|
| Organizational Structure | **Orchestrated** | Employs a "global evaluator" that coordinates and "consolidates data across all local searches" to share information among rational agents. |
| Operational Methodology | **Graph-Routed** | Decisions regarding "where to sample" and "when to stop" are determined by cost-aware routing logic that balances exploration and exploitation. |

**Key Identifying Features:**
- Global evaluator coordinator
- Cost-aware stopping criterion
- Experience replay buffer

---

### 27. massoudi2025agentic
**Agentic Large Language Models for Conceptual Systems Engineering and Design**

| Dimension | Classification | Rationale |
|-----------|---------------|-----------|
| Organizational Structure | **Orchestrated** | Architecture is "orchestrated" by specialized agents (Planner, Supervisor) through a LangGraph framework managing task hand-offs. |
| Operational Methodology | **Iterative-Feedback** | Adopts a "generate → critique → evolve" loop where reflection agents test each proposal to progressively refine design elements. |

**Key Identifying Features:**
- Design State Graph (DSG)
- Generate-critique-evolve loop
- Meta-Reviewer elitist selection

---

### 28. elrefaie2025ai
**AI Agents in Engineering Design: A Multi-Agent Framework for Aesthetic and Aerodynamic Car Design**

| Dimension | Classification | Rationale |
|-----------|---------------|-----------|
| Organizational Structure | **Orchestrated** | Follows a "structured decision-making approach" where a "central agent" (controller) delegates tasks to specialized sub-agents. |
| Operational Methodology | **Staged-Pipeline** | Workflow involves both sequential dependencies (Sketching → Styling → Simulation) and parallel independent tasks in a prescribed sequence. |

**Key Identifying Features:**
- Hybrid agent approach
- Styling and CAD sub-agents
- DrivAerNet++ database retrieval

---

### 29. navarro2025autonomous
**Autonomous Multi-Agent AI Systems for Satellite Mission Design**

| Dimension | Classification | Rationale |
|-----------|---------------|-----------|
| Organizational Structure | **Orchestrated** | Workflow uses a "hierarchical structure" where an "AI Study Manager" oversees the mission design and "dynamically assigns tasks." |
| Operational Methodology | **Iterative-Feedback** | Features "multi-agent debate and self-correction," where AI agents iteratively refine configurations through self-improving loops. |

**Key Identifying Features:**
- Mission Study Manager orchestrator
- Multi-agent debate loop
- Real-time trade-off analysis

---

### 30. zhang2025desagent
**DesAgent: A Multi-Agent Mechanical Design Method Based on Collaborative Large and Small Models**

| Dimension | Classification | Rationale |
|-----------|---------------|-----------|
| Organizational Structure | **Orchestrated** | Features a "hierarchical multi-agent system" consisting of four specialized agents coordinated to resolve multidisciplinary coupling. |
| Operational Methodology | **Iterative-Feedback** | Employs a "Semantic-Numerical Synergy Loop (SNS-Loop)" for "iterative optimization" and dynamic feedback coordination between LLMs and ROSMs. |

**Key Identifying Features:**
- SNS-Loop architecture
- Reduced-Order Small Models (ROSMs)
- Multidisciplinary coupling matrix
