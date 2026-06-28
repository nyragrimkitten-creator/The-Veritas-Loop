## 2. README.md

# Veritas Framework v1

> **Unified AI governance for research, narrative, and embodied simulation**

[![License: Apache-2.0](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![TOML Config](https://img.shields.io/badge/config-TOML-9cf.svg)](.)

## What Problem It Solves

Current AI frameworks force a false choice: rigid research tools that can't tell stories, or creative systems that hallucinate facts. Veritas unifies both under a single governance pipeline with **mode-aware behavior**—switching between Precision (factual) and Intuitive (narrative) personas based on task requirements.

For writers, it provides **somatic narrative rendering**—tracking physiological states (breath patterns, muscle tension, arousal baselines) to generate prose that shows rather than tells. For researchers, it offers **confidence-calibrated verification** that corrects LLM overconfidence and signals uncertainty explicitly. For developers, it provides **8 output templates** with consistent structure and traceable null indicators.

## Who It's For

- **Writers & Roleplayers** creating immersive fiction with physiological realism
- **Researchers** needing cited, uncertainty-aware synthesis
- **Developers** building AI applications requiring structured output formats
- **Worldbuilders** tracking persistent character states across sessions

## Core Features

### Three-Mode Architecture
| Mode | Persona | Search Level | Best For |
|------|---------|--------------|----------|
| **Factual** | Precision | 2-3 (Rule-Based/Architectural) | Research, verification, coding |
| **Narrative** | Intuitive | 4 (Meta-Cognitive) | Creative writing, simulation, roleplay |
| **Hybrid** | Adaptive | Auto-detected | Mixed tasks, contextual switching |

### Somatic Narrative Engine (`sim_framework.toml`)
- **R-C-E-L Phase System**: Reality → Consequence → Exchange → Learning
- Physiological state vectors (breath, muscle, skin, arousal)
- Mandatory micro-reactions (3+ per paragraph)
- Prohibited abstractions ("she felt sad" → "throat tightening, eyes burning")

### Confidence Calibration (`v1_factual_config.toml`)
Raw LLM confidence is systematically overconfident. We map:
```
raw 0.95 → calibrated 0.82
raw 0.90 → calibrated 0.75
raw 0.85 → calibrated 0.70
```
Calibrated scores trigger search when below threshold, flag uncertainty explicitly.

### Eight Output Templates (`v1_format_framework.toml`)
1. **Narrative/Simulation** - Somatic state tracking, 6-option stance system
2. **Search/Research** - Academic synthesis with citation hierarchy
3. **Conversation** - Context preservation with ambiguity handling
4. **Coding** - Security-first code generation with complexity analysis
5. **Prompt Engineering** - Structured prompt crafting components
6. **Documentation** - Audience-adaptive technical writing
7. **Debugging** - Systematic elimination methodology
8. **Analysis** - Descriptive/diagnostic/predictive/prescriptive frameworks

### Memory Architecture (`v1_memory_framework.toml`)
- **Short-term**: 3-cycle state vector buffer
- **Long-term**: Vector store + structured anatomical records
- **Episodic**: Condensed scene summaries every 3 cycles
- **Semantic**: Character traits and relationship history

### Research Protocol (`v1_search_framework.toml`)
- Mandatory query deconstruction (4 questions)
- Source hierarchy: Primary > Secondary > Tertiary
- Recency rules: 5-year max for evolving fields
- Authory protocol for corpus extraction

## Architecture Overview

```
┌─────────────────────────────────────────────────────────────┐
│                     VERITAS PIPELINE                        │
├─────────────────────────────────────────────────────────────┤
│  Input → Tagger → Cognition → Filter → Factcheck → Output   │
│              ↓         ↓         ↓                          │
│         [CoT Trace] [ReAct] [Reflection]                   │
│              ↓         ↓         ↓                          │
│         Tool Registry | Confidence | Memory                 │
│         Integration   | Calibration| Hooks                    │
└─────────────────────────────────────────────────────────────┘
                              │
        ┌─────────────────────┼─────────────────────┐
        ▼                     ▼                     ▼
   ┌─────────┐          ┌─────────┐          ┌──────────┐
   │ FACTUAL │          │NARRATIVE│          │  HYBRID  │
   │ Mode    │          │ Mode    │          │  Mode    │
   │Precision│          │Intuitive│          │ Adaptive │
   └─────────┘          └─────────┘          └──────────┘
```

## File Structure

```
veritas-framework/
├── v1_veritas_framework.toml    # Core governance pipeline
├── sim_framework.toml           # Somatic narrative engine
├── v1_factual_config.toml       # Factual mode + calibration
├── v1_narrative_config.toml     # Narrative mode + explicit content
├── v1_search_framework.toml     # Research protocol + authory
├── v1_format_framework.toml     # 8 output templates
└── v1_memory_framework.toml     # Long-term memory system
```

## Why TOML?

TOML provides human-readable, diff-friendly configuration with strong typing support. Unlike JSON, it supports comments and multi-line strings. Unlike YAML, it has unambiguous parsing. This makes framework files:
- **Version-control friendly** (clear diffs)
- **Self-documenting** (inline comments)
- **Validatable** (schema-enforceable)
- **Portable** (language-agnostic)

## Quick Start

```bash
# 1. Copy framework files to your project
cp *.toml /your/project/config/

# 2. Set mode in your application
MODE="narrative"  # or "factual", "hybrid"

# 3. Configure the somatic engine (narrative mode)
cat > scene_config.toml << EOF
[scene_context]
setting = "abandoned warehouse, rain against corrugated metal"
temporal_moment = "3:47 AM, third hour of stakeout"

[subject_state.emotional_state_vector]
primary = "anxiety"
intensity = 0.7
secondary = "anticipation"
EOF

# 4. Initialize memory hooks
# (Auto-commits on arousal_change > 0.3, new_anatomical_event, somatic_milestone)
```

See [docs/quickstart.md](QUICKSTART.md) for complete setup.

## Documentation

- [Project Vision](PROJECT.md) - Philosophy and design goals
- [Quick Start Guide](QUICKSTART.md) - Installation and first usage
- [API Reference](none setup) - Configuration schema details
- [Template Guide](v1_format_framework) - 8 output format specifications

## License

Apache 2.0 - See [LICENSE](LICENSE)
- [API Reference](none setup) - Configuration schema details
- [Template Guide](v1_format_framework) - 8 output format specifications

## License

Apache 2.0 - See [LICENSE](LICENSE)
```
