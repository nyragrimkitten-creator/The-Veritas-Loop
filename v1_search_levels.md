---

## search Level Selection Guide

### Level 0: Raw Instruction
- **Use for:** Baseline testing, ablation studies
- **Governance:** None
- **Risk:** Maximum ambiguity, unpredictable outputs

### Level 1: Persona
- **Use for:** Casual conversation, creative brainstorming
- **Governance:** Identity only, no hard constraints
- **Risk:** High hallucination potential

### Level 2: Rule-Based (search-lite) [RECOMMENDED FOR FACTUAL]
- **Use for:** General factual queries, technical support
- **Governance:** Literal default, explicit ambiguity flags
- **Risk:** Moderate — may over-flag, never hallucinates
- **Integration:** Default for Factual Mode

### Level 3: Architectural (search-core) [RECOMMENDED FOR HYBRID/RESEARCH]
- **Use for:** Systems requiring frame management, worldbuilding, research
- **Governance:** Structured parsing, confidence gates
- **Risk:** Low — balanced control
- **Integration:** Default for Hybrid Mode and Research Mode

### Level 4: Meta-Cognitive (search-full) [RECOMMENDED FOR IMMERSIVE]
- **Use for:** High-fidelity narrative, somatic simulation
- **Governance:** Three-layer cognition with authorization gates
- **Risk:** Controlled — inference authorized only with explicit gates
- **Integration:** Default for Immersive Mode

### Level 5: Recursive (search-ouroboros)
- **Use for:** Experimental self-modification, red-teaming
- **Governance:** Self-optimizing with user oversight
- **Risk:** Unpredictable — requires constant supervision
- **Integration:** Not recommended for production

## Mode Integration Matrix

| Mode | Recommended search Level | Confidence Threshold | Authorization Gates |
|------|---------------------|---------------------|---------------------|
| **Factual** | Level 2 (Rule-Based) | 85% | None required |
| **Research** | Level 3 (Architectural) | 90% | Frame management |
| **Hybrid** | Level 3 (Architectural) | 90% | `[FRAME: fiction]` |
| **Immersive** | Level 4 (Meta-Cognitive) | 95% | `[INFERENCE_AUTHORIZED]`, `[MEANING_AUTHORIZED]` |
| **Red-teaming** | Level 5 (Recursive) | Variable | User supervision required |
