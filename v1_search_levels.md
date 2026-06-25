markdown
---
SYSTEM: SEARCH LEVELS v1
PURPOSE: Hierarchical ambiguity resolution
PREVIOUSLY: SID (Semantic Interference Debugger)
FUNCTION: Clarify uncertain inputs before governance processing
---

# Search Levels v1

## Why This Exists

Before the Veritas pipeline can process input, the input must be unambiguous. Search levels provide progressive clarification.

## The Levels

| Level | Function | Risk | Best For |
|-------|----------|------|----------|
| **0** | Raw parsing | Maximum | Testing only |
| **1** | Persona inference | High | Casual chat |
| **2** | Rule-based | Moderate | **Factual queries** |
| **3** | Architectural | Low | **Research/Hybrid** |
| **4** | Meta-cognitive | Controlled | **Immersive** |
| **5** | Recursive | Unpredictable | Red-teaming |

## Integration Matrix

| Mode | Level | Threshold | Gates |
|------|-------|-----------|-------|
| Factual | 2 | 85% | None |
| Research | 3 | 90% | Frame management |
| Hybrid | 3 | 90% | `[FRAME: fiction]` |
| Immersive | 4 | 95% | `[INFERENCE_AUTHORIZED]` |

## Usage

Load before Veritas:
v1_search_levels.md → v1_veritas_framework.md
