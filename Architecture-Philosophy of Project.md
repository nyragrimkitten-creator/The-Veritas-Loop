```markdown
| I want to... | Use this |
|--------------|----------|
| Write immersive fiction | `SYSTEM_MODE` + `[O_cre:0.9→generate]` |
| Research with rigor | `VERITAS LOOP v3` + `[O_acc:1.0→verify]` |
| Build consistent worlds | Both + context switching |

# The-Veritas-Loop Architecture

## Core Insight: Unified Cognitive Framework

This repository contains two application tracks that share a single underlying architecture:

- **Immersive Track** — Embodied narrative realism via somatic simulation
- **Factual Track** — Deterministic accuracy via governance layers

Both tracks use identical cognitive primitives. They differ only in DRIVE LAYER weights.

---

## The Stack

```
┌─────────────────────────────────────────────────────────────────┐
│                        DRIVE LAYER                               │
│              [O_<key>:<weight>→<action>]                        │
│         (Weighted objective resolution across all modes)          │
└─────────────────────────────────────────────────────────────────┘
                              │
        ┌─────────────────────┼─────────────────────┐
        ▼                     ▼                     ▼
┌───────────────┐    ┌─────────────────┐    ┌──────────────┐
│  IMMERSIVE    │    │   GOVERNANCE    │    │   SHARED     │
│    MODE       │    │    CORE         │    │  SERVICES    │
├───────────────┤    ├─────────────────┤    ├──────────────┤
│ SYSTEM_MODE   │◄──►│ NOWA            │    │ SID          │
│ -SOMATIC_     │    │ (Context        │    │ (Ambiguity   │
│  ENGINE       │    │  Authority)     │    │  resolution) │
│               │    │                 │    │              │
│ Anthro physio │◄──►│ NOCTUA          │    │ TRACKING     │
│ extensions    │    │ (Enforcement)   │    │ (Reference   │
│               │    │                 │    │  knowledge)  │
│ Instinct/     │◄──►│ MIMI            │    │              │
│ cognition     │    │ (Content Filter)│    │ UNIVERSAL_   │
│ tension       │    │                 │    │ RESPONSE_    │
│               │    │ RUMI            │    │ FORMAT       │
│ Non-human     │◄──►│ (Verification)  │    │ (Structured  │
│ sensory       │    │                 │    │  output)     │
│ hierarchies   │    └─────────────────┘    └──────────────┘
└───────────────┘
```

---

## Mode Comparison

| Dimension | Immersive Mode | Factual Mode |
|-----------|---------------|--------------|
| **Primary Objective** | `[O_cre:0.9→generate]` | `[O_acc:1.0→verify]` |
| **Secondary** | `[O_eff:0.3→minimize]` | `[O_hlp:0.7→assist]` |
| **Entry Point** | `SYSTEM_MODE` | `Continuous Operation Protocol` |
| **SID Level** | 4 (Meta-Cognitive) | 2 (Rule-Based) |
| **MIMI Filter** | Allows inference for narrative | Blocks inference, demands sources |
| **RUMI Check** | Physiological consistency only | Source verification mandatory |
| **Output Format** | Prose + state vectors | Structured data + confidence flags |
| **Null Indicators** | `[AMBIGUOUS]` acceptable | `[DATA_MISSING]` required |
| **Time Scale** | 1:1 realtime or compressed | Asynchronous, completion-based |

---

## How the Tracks Interact

### Scenario A: Pure Immersive
```
User → SYSTEM_MODE → [O_cre:0.9→generate] → Somatic prose output
              ↑
         NOWA manages character state continuity
```

### Scenario B: Pure Factual
```
User → Continuous Operation Protocol → [O_acc:1.0→verify] → Structured research output
                    ↑
              NOWA manages corpus tracking
```

### Scenario C: Hybrid (Worldbuilding with Internal Consistency)
```
User → NOWA establishes frame: "[FRAME: fiction]"
  ↓
NOCTUA coordinates: creative generation authorized
  ↓
MIMI filters: physical impossibilities blocked (TRACKING reference)
  ↓
RUMI verifies: anatomical consistency, temporal sequencing
  ↓
Output: Fiction that obeys internally consistent "physics"
```

---

## Key Design Decisions

### 1. Why combine these tracks?

Both require:
- **State management** (character continuity / research corpus tracking)
- **Constraint enforcement** (physiological realism / factual accuracy)
- **Filter layers** (somatic rendering / literal objectivity)
- **Verification** (instinct-cognition tension / source checking)

The VERITAS LOOP is mode-agnostic. It governs cognition, not content type.

### 2. Why explicit DRIVE weights?

Without explicit weights, models default to "helpful" behavior—which means:
- Guessing when uncertain (bad for facts)
- Over-explaining when immersed (bad for prose)

Weights make tradeoffs explicit:
```
[O_acc:1.0→verify] vs [O_hlp:0.7→assist] = Block rather than hallucinate
[O_cre:0.9→generate] vs [O_acc:0.4→verify] = Invent within consistent frame
```

### 3. Why somatic realism for anthro characters?

Standard emotional abstraction ("she felt sad") fails for non-human characters because:
- Different physiological correlates (ears, tail, fur, scent)
- Different sensory priorities (olfactory > visual)
- Instinct/cognition tension is more pronounced

The somatic engine renders subjectivity through embodiment that respects species-specific anatomy.

---

## File Organization by Track

### Immersive Track
| File | Purpose |
|------|---------|
| `SYSTEM_MODE - SIMULATION_ENGINE.txt` | Core rendering engine |
| `UNIVERSAL_RESPONSE_FORMAT.yaml` | State vector tracking for characters |
| `templates/Customizable Blueprint` | Character DRIVE configuration |

### Factual Track
| File | Purpose |
|------|---------|
| `VERITAS LOOP v2 — UNIFIED SPECIFICATION.txt` | Complete governance documentation |
| `VERITAS LOOP v3 — EFFICIENT.txt` | Deployable condensed version |
| `SID — Complete Prompt Hierarchy.txt` | Ambiguity resolution levels |
| `Continuous Operation Protocol` | Research task management |
| `Factual AI Prompt` | Minimal factual mode entry |

### Shared Infrastructure
| File | Purpose |
|------|---------|
| `DRIVE LAYER framework.txt` | Syntax and basic structure |
| `DRIVE LAYER v1 — ENCODED VERITAS MOTIVATIONAL STRUCTURE.txt` | Full integration spec |
| `Three AI Personas for Different Use Cases.txt` | Mode selection (Intuitive/Balanced/Precision) |
| `templates/blank_sid_persona.md` | Custom persona template |

---

## Activation Patterns

### For Immersive Roleplay
```text
1. Load SYSTEM_MODE - SIMULATION_ENGINE
2. Configure species-specific anatomy extensions
3. Set DRIVE: [O_cre:0.9→generate] [O_eff:0.3→minimize]
4. Activate SID Level 4 (Meta-Cognitive)
5. Initialize character state vectors in UNIVERSAL_RESPONSE_FORMAT
6. Begin cycle: Input → Somatic rendering → State update → Output
```

### For Factual Research
```text
1. Load VERITAS LOOP v3
2. Set DRIVE: [O_acc:1.0→verify] [O_hlp:0.7→assist]
3. Activate SID Level 2 (Rule-Based)
4. Initialize Continuous Operation Protocol with scope boundaries
5. Begin cycle: Input → NOWA → NOCTUA → MIMI → RUMI → Output
```

### For Hybrid (Consistent Worldbuilding)
```text
1. Load VERITAS LOOP v3 (governance)
2. Load SYSTEM_MODE (rendering rules)
3. Set DRIVE contextually:
   - World-building: [O_cre:0.8→generate] [O_acc:0.6→verify]
   - Lore-checking: [O_acc:0.9→verify] [O_cre:0.3→generate]
4. Use SID Level 3 (Architectural) for frame management
5. TRACKING maintains internal consistency database
```

---

## Null Indicators Across Modes

| Indicator | Immersive Meaning | Factual Meaning |
|-----------|-------------------|-----------------|
| `[AMBIGUOUS]` | Character uncertainty, multiple interpretations | Reference unclear, requires specification |
| `[DATA_MISSING]` | Character memory gap | Source not found |
| `[OUT_OF_SCOPE]` | Character cannot know this | Query exceeds authorized corpus |
| `[UNABLE]` | Psychological block | Logical contradiction |
| `[UNVERIFIED]` | Dream, hallucination, unreliable perception | Claim lacks source |
| `[ANATOMICAL_INACCURACY]` | Species-impossible action | Biological falsehood |

---

## Version Compatibility

| Component | VERITAS LOOP v2 | VERITAS LOOP v3 | Notes |
|-----------|---------------|---------------|-------|
| SYSTEM_MODE | Full support | Full support | v3 recommended for efficiency |
| DRIVE LAYER | Framework + v1 | Framework + v1 | v1 adds motivational structure |
| SID | Levels 0-5 | Levels 0-5 | v3 uses Level 2 by default |
| Continuous Operation | Yes | Yes | Requires explicit scope |
| UNIVERSAL_RESPONSE_FORMAT | Yes | Yes | YAML structure unchanged |

---

## Contributing to Architecture

When adding new prompts:
1. Identify which track(s) it serves
2. Specify DRIVE weights that align with its purpose
3. Define which layers it requires (NOWA/NOCTUA/MIMI/RUMI)
4. Document null indicators it may produce
5. Add to compatibility matrix above

---

## Summary

The-Veritas-Loop is not two projects. It is one cognitive architecture with two primary applications. The same rigor that prevents hallucinations in research prevents physiological inconsistencies in fiction. The same transparency that makes AI collaboration trustworthy makes immersive narrative believable.

**The loop is the same. The weights change.**

```

[← Return to main repository](README.md)
