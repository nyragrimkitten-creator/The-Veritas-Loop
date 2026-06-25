markdown
---
SYSTEM: PROJECT DOCUMENTATION
PURPOSE: Architecture overview and design rationale
---

# The-Veritas-Loop Architecture

## Core Insight: Unified Cognitive Framework

Two application tracks share one underlying architecture:

- **Immersive Track** — Embodied narrative realism via somatic simulation
- **Factual Track** — Deterministic accuracy via governance layers

Both use identical cognitive primitives. They differ only in DRIVE weights.

## The Pipeline
Input → Tagger → Cognition → Filter → Factcheck → Output
↑________________________↓
(uncertain returns)

## Stage Functions

| Stage | Function | Blocks |
|-------|----------|--------|
| **Tagger** | Scope/context tagging | Drift, violations |
| **Cognition** | Meta-cognitive oversight | False roleplay |
| **Filter** | Content filtering | Subjectivity |
| **Factcheck** | Verification | Unsourced claims |

## How Tracks Interact

### Pure Research
Input → Tagger → Cognition → Filter → Factcheck → Search Levels → Structured output

### Pure Immersive
Input → Tagger → Cognition → Filter → Factcheck → Simulation → Somatic prose

### Hybrid (Worldbuilding)
Input → Tagger → Cognition → Filter → Factcheck → [FRAME: fiction] → Simulation → Consistent fiction

## File Organization

| Track | Files |
|-------|-------|
| **Governance** | `v1_veritas_framework.md` |
| **Motivation** | `v1_dl_config.md`, `v1_dl_framework.txt` |
| **Ambiguity** | `v1_search_levels.md`, `v1_search_framework.xml` |
| **Simulation** | `sim_framework.yaml`, `sim_config.yaml` |
| **Persona** | `v1_trinity_framework.md`, `v1_trinity_config.yaml` |
| **Format** | `v1_rp_format.yaml` |

## Key Design Decisions

### 1. Why combine tracks?
Both require:
- State management
- Constraint enforcement
- Filter layers
- Verification

The Veritas pipeline is mode-agnostic. It governs cognition, not content type.

### 2. Why explicit DRIVE weights?
Without explicit weights, models default to "helpful" behavior:
- Guessing when uncertain (bad for facts)
- Over-explaining when immersed (bad for prose)

Weights make tradeoffs explicit.

### 3. Why somatic realism?
Standard emotional abstraction ("she felt sad") fails for non-human characters because:
- Different physiological correlates (ears, tail, fur, scent)
- Different sensory priorities (olfactory > visual)
- Instinct/cognition tension is more pronounced

## Summary

The-Veritas-Loop is one cognitive architecture with two primary applications. The same rigor that prevents hallucinations in research prevents physiological inconsistencies in fiction.

**The pipeline is the same. The weights change.**
