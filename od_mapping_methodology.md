# Organizational Design Mapping Methodology

This document describes the methodology used to map taxonomy categories to organizational design (OD) concepts, addressing how the 3-6 "most relevant" concepts were selected for each category in Table 4 of the paper.

## Overview

The mapping process connected each taxonomy category (Orchestrated, Networked, Sequential for Organizational Structure; Iterative-Feedback, Graph-Routed, Staged-Pipeline for Operational Methodology) to established organizational design concepts from the management science literature. The goal was to identify which OD mechanisms each architectural pattern *inherently invokes* by virtue of its structure, regardless of whether current MAS implementations explicitly engage these concepts.

## Source Material

The primary source for OD concepts was Joseph and Sengul's comprehensive survey "Organizational Configurations" (2025), which reviews organizational design research from 2000-2023 across four theoretical approaches:

| Approach | Focus | Example Concepts |
|----------|-------|------------------|
| **Configuration** | How organizations structure and group activities | Decomposition, modularity, near-decomposability, mirroring hypothesis |
| **Control** | How organizations monitor and direct behavior | Span of control, oversight, locus of authority, information asymmetry |
| **Channelization** | How organizations direct attention and information flow | Aspiration levels, structural distribution of attention, problemistic search |
| **Coordination** | How organizations align interdependent activities | Common ground, integrator roles, predictive knowledge, trans-specialist knowledge |

## Mapping Process

### Step 1: Identify Primary OD Approaches per Category

Each taxonomy category was first matched to the OD approach(es) most relevant to its defining coordination mechanism:

| Taxonomy Category | Primary OD Approaches | Reasoning |
|-------------------|----------------------|-----------|
| **Orchestrated** | Control + Coordination | Manager-led structure inherently involves oversight, span limitations, and integration across specialists |
| **Networked** | Coordination + Channelization | Peer coordination requires shared understanding and distributed attention allocation |
| **Sequential** | Configuration + Coordination | Stage-based decomposition invokes modularity principles and interface management |
| **Iterative-Feedback** | Channelization + Configuration | Convergence-based iteration involves aspiration levels and performance gap detection |
| **Graph-Routed** | Channelization + Configuration | Dynamic routing involves attention allocation and coupled search decisions |
| **Staged-Pipeline** | Configuration + Channelization | Prescribed phases invoke decomposition and structural attention distribution |

### Step 2: Concept Identification

Within the identified OD approaches, all potentially applicable concepts were noted. For each taxonomy category, this produced an initial list of 8-15 candidate concepts.

### Step 3: Concept Selection

From the candidate list, 3-6 concepts were selected for each category based on three criteria applied jointly:

**Criterion 1: Centrality to Defining Mechanism**
The concept must address a challenge that is *inherent* to the architectural pattern, not merely possible or occasional. For example:
- Span of control is *inherent* to Orchestrated systems (any manager agent faces capacity limits)
- Information asymmetry is *inherent* to Orchestrated systems (orchestrators route tasks without full specialist knowledge)

**Criterion 2: Practical Implications for MAS Design**
The concept must have actionable implications for how MAS architectures could be designed or evaluated. Concepts were favored if they suggest:
- Design parameters that could be explicitly optimized (e.g., span of control → agent count decisions)
- Failure modes that could be anticipated (e.g., joint myopia → search diversity requirements)
- Mechanisms that could be deliberately implemented (e.g., common ground → shared memory design)

**Criterion 3: Distinctiveness Across Categories**
The concept must help differentiate one category from another rather than applying generically to all architectures. For example:
- Span of control distinguishes Orchestrated (centralized coordination capacity) from Networked (no central coordinator)
- Common ground distinguishes Networked (peer coordination requirement) from Orchestrated (coordinator mediates)

### Step 4: Exclusion Decisions

Concepts were excluded from the final mapping if they:

1. Failed to meet all three selection criteria (e.g., relevant but not distinctive, or distinctive but lacking practical MAS implications)

2. Were subsumed by a more central concept (e.g., if "oversight" and "monitoring" both applied, the more comprehensive term was retained)

3. Could not be included due to space constraints in the paper format (table space limitations required prioritizing the most essential concepts)

Excluded concepts are not irrelevant—they may provide additional analytical depth in future work—but the selected concepts represent the most essential OD mechanisms for each category.

## Validation Approach

Mappings were validated by verifying that:

1. **Definitional alignment**: Each selected concept's definition (per Joseph & Sengul) logically applies to the taxonomy category's defining mechanism

2. **Mutual exclusivity**: Concepts mapped to one category do not equally apply to all other categories (distinctiveness check)

3. **Completeness**: The selected concepts collectively address the primary coordination challenges the category faces

Validation was performed against the theoretical definitions of OD concepts, not against the 30 MAS papers in the corpus. This is intentional: the mapping identifies what OD mechanisms each architecture *inherently invokes*, which is independent of whether current implementations explicitly discuss these mechanisms. Indeed, the paper's central finding is that MAS implementations engage these concepts superficially despite their inherent relevance.

## Mapping Summary

The final mappings are:

### Organizational Structure

| Category | Primary Approaches | Selected Concepts |
|----------|-------------------|-------------------|
| **Orchestrated** | Control + Coordination | Span of control, Oversight, Information asymmetry, Locus of authority, Integrator roles |
| **Networked** | Coordination + Channelization | Common ground, Peer monitoring, Trans-specialist knowledge, Joint myopia, Predictive knowledge |
| **Sequential** | Configuration + Coordination | Decomposition, Modularity, Near-decomposability, Mirroring hypothesis, Viscosity |

### Operational Methodology

| Category | Primary Approaches | Selected Concepts |
|----------|-------------------|-------------------|
| **Iterative-Feedback** | Channelization + Configuration | Aspiration levels, Problemistic search, Ambidexterity, False negative avoidance, Managerial frames |
| **Graph-Routed** | Channelization + Configuration | Structural distribution of attention, Managerial frames, Omission vs. commission, Coupled search, Internal representations |
| **Staged-Pipeline** | Configuration + Channelization | Decomposition, Modularity, Aspiration levels, Structural distribution of attention, Mirroring hypothesis |

## Limitations

1. **Single-pass assignment**: Mappings were developed in one pass rather than through iterative refinement with multiple reviewers. Different researchers might emphasize different concepts.

2. **Source dependency**: The mapping relies primarily on Joseph and Sengul's synthesis. Alternative OD frameworks or primary sources might yield different concept selections.

3. **Space constraints**: Some relevant concepts were excluded due to publication format limitations. The supplementary materials here provide the most essential mappings; extended analysis could include additional concepts.

4. **Theoretical rather than empirical validation**: Mappings were validated against OD definitions, not empirically tested to confirm that these mechanisms affect MAS performance. Such empirical validation is identified as future work in the paper.

## References

Joseph, J., & Sengul, M. (2025). Organizational Configurations: Review and Agenda. *Journal of Management*.

Asimow, M. (1962). *Introduction to Design*. Prentice-Hall.
