# OIA-Supplement

Supplementary materials for "Organizationally-Intelligent Agents: Connecting Multi-Agent Engineering Systems to Organizational Design Theory"

## Overview

This repository contains the corpus list, attribute classifications, and taxonomy rationale for the 30 multi-agent system (MAS) frameworks analyzed in the paper. These materials support reproducibility by enabling other researchers to replicate our data collection and classification methodology.

## Files

| File | Description |
|------|-------------|
| `corpus_summary.csv` | Citation keys, titles, one-line descriptions, domains, and taxonomy classifications for all 30 frameworks |
| `full_attributes.csv` | Complete 8-attribute classification for each framework (orchestration, organizational structure, reasoning protocols, operational methodologies, memory, modality, agent count, Asimow phase coverage) |
| `classification_rationale.md` | Taxonomy definitions and per-paper rationale explaining classification decisions with key identifying features |

## Taxonomy Overview

### Organizational Structure (3 categories)
- **Orchestrated**: Explicit orchestrator/manager agent coordinates other agents
- **Networked**: Peer agents communicate via shared state or message passing without central coordinator
- **Sequential**: Pipeline/workflow with predetermined execution order and stage-to-stage handoffs

### Operational Methodology (3 categories)
- **Iterative-Feedback**: Repeated generation-evaluation-refinement cycles until convergence
- **Graph-Routed**: Dynamic execution paths determined by routing logic or state machines
- **Staged-Pipeline**: Fixed sequence of distinct phases with prescribed transitions

## Data Collection

**Inclusion criteria**: Multi-agent systems employing LLMs or AI agents for hardware/physical product design (mechanical, structural, circuit, fluid mechanics, materials discovery) with sufficient description of agent architecture, task decomposition, or organizational structure.

**Exclusion criteria**: Software engineering (mature tooling with distinct patterns), robotic RL agents (distinct action spaces/reward structures), pure control theory/optimization without design synthesis.

**Search strategy**: Three keyword sets ("Multi-Agent Framework for engineering design," "AI Agents in Engineering Design," "Agentic Frameworks for Engineering Design") across arXiv, IEEE Xplore, ACM Digital Library, Design Society, and ASME IDETC-CIE proceedings. Searches targeted 2024-2025 publications and were conducted November-December 2024.

## Citation

If you use these materials, please cite:

```bibtex
@inproceedings{ezemba2025organizationally,
  title={Organizationally-Intelligent Agents: Connecting Multi-Agent Engineering Systems to Organizational Design Theory},
  author={Ezemba, Jessica and McComb, Christopher and Tucker, Conrad},
  booktitle={[Conference Name]},
  year={2025}
}
```

## Contact

For questions about the classification methodology or to report issues, please contact the corresponding author: jezemba@andrew.cmu.edu
