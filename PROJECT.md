## 3. PROJECT VISION (PROJECT.md)


# Veritas Framework: Vision & Intent

## Why This Framework Exists

Large language models are Janus-faced: they can synthesize research or spin fiction, but rarely both with fidelity. Existing frameworks treat these as separate domains—research tools that can't tell stories, creative tools that hallucinate facts.

Veritas emerged from a simple observation: **the same cognitive infrastructure serves both modes**. A system that can track confidence thresholds for research can track physiological states for narrative. A pipeline that validates citations can validate anatomical consistency.

This framework exists to provide **unified governance** for AI systems that must be simultaneously:
- **Accountable** (traceable claims, explicit uncertainty)
- **Immersive** (embodied narrative, persistent state)
- **Adaptable** (mode-aware switching, hybrid workflows)

## Philosophy

### 1. Epistemic Humility
AI systems should signal uncertainty explicitly. We never merge conflicting sources without flagging. We calibrate confidence scores to empirical accuracy. We use null indicators (`[DATA_MISSING]`, `[UNVERIFIED]`, `[CALIBRATED_LOW]`) rather than confident fabrications.

### 2. Somatic Realism
In narrative mode, we render experience through the body. Emotions manifest as physical correlates—"throat tightening" not "she felt sad." This grounds abstract concepts in sensory reality and maintains immersion.

### 3. Methodical Progression
Explicit content receives the same anatomical rigor as combat or survival mechanics. Stages progress methodically (Initiation → Arousal → Throbbing → Foreplay → Penetration → Climax → Recovery) with physiological tracking at each step. No instant transitions. No poetic abstraction replacing sensation.

### 4. State Persistence
Characters have memory. Anatomical states carry over between scenes. Relationships accumulate history. This isn't "worldbuilding" as static lore—it's **computational state** that affects future outputs.

### 5. Declarative Configuration
Behavior is defined in TOML, not code. This makes the framework:
- Auditable (read the config, know the behavior)
- Version-controlled (diff-friendly)
- Composable (mix configurations for hybrid modes)
- Portable (language-agnostic)

## Design Goals

| Goal | Implementation |
|------|----------------|
| **Traceability** | Every claim has citation or null indicator |
| **Calibration** | Confidence scores map to empirical accuracy |
| **Embodiment** | Narrative renders through physiological state |
| **Persistence** | Memory architecture spans sessions |
| **Modularity** | Components compose without entanglement |
| **Explicitness** | Uncertainty flagged, assumptions labeled |

## What Success Looks Like

### For Research Tasks
A user asks: "What are the cardiovascular effects of prolonged spaceflight?"

The framework:
1. Deconstructs the query (4 questions)
2. Searches with calibrated confidence thresholds
3. Returns structured analysis with citations `[Author, Year]`
4. Flags outdated sources `[Source, 2018] ⚠️ [Current understanding may differ]`
5. Presents conflicting evidence without merging
6. Reports calibrated confidence: `0.78/1.00`

### For Narrative Tasks
A user initiates: "The guard has been watching her for hours."

The framework:
1. Enters narrative mode (Intuitive persona)
2. Queries memory for character history
3. Renders through somatic lens: "His neck flushes, breath hitching as she shifts—three hours of surveillance eroding his professional distance."
4. Tracks arousal baseline (0.2 → 0.4)
5. Commits to long-term memory (threshold crossed)
6. Offers 6 stance options (Pragmatic, Dominant, Devoted, Feral, Attentive, Deviant)

### For Hybrid Tasks
A user asks: "Write a scene where a character uses actual lockpicking techniques."

The framework:
1. Detects hybrid mode (narrative + factual)
2. Searches lockpicking mechanics (Search Level 2)
3. Renders scene with verified techniques
4. Maintains somatic state (tension, focus, sweat)
5. Cites sources inline without breaking immersion

## Anti-Goals

We explicitly avoid:
- **Hallucination as feature** — Creativity is bounded by anatomical/physical possibility
- **Opaque confidence** — Raw scores are calibrated; uncertainty is explicit
- **Stateless generation** — Each output considers accumulated history
- **One-size-fits-all** — Modes adapt behavior; no universal persona

## The Name

*Veritas* (truth) reflects our commitment to epistemic accountability—not naive realism, but honest representation of what is known, unknown, and uncertain. The framework doesn't claim to generate truth, but to **govern generation with truth-tracking mechanisms**.
