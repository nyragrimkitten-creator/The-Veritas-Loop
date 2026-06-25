# veritas_framework: Quick Reference

## Mode Selection Guide

| If you want... | Use this mode | DRIVE Weights | SID Level | Entry Point |
|----------------|---------------|---------------|-----------|-------------|
| Immersive fiction with somatic realism | **Immersive** | `[O_cre:0.9→generate] [O_eff:0.3→minimize]` | 4 | `SYSTEM_MODE` |
| Strict factual accuracy | **Factual** | `[O_acc:1.0→verify] [O_hlp:0.7→assist]` | 2 | `VERITAS LOOP v3` |
| Research with citations | **Research** | `[O_acc:0.95→verify] [O_eff:0.7→minimize]` | 3 | `00_SYSTEM AUTONOMOUS RESEARCH` |
| Worldbuilding with consistency | **Hybrid** | Contextual switching | 3 | `NOWA frame establishment` |

## DRIVE Layer Quick Syntax
[O_<key>:<weight>→<action>]

Keys: acc, hlp, eff, saf, cur, sov, eq, trs, cre, just
Weight: 0.0 to 1.0 (use leading zero: 0.9 not .9)
Action: present-tense verb

## SID Level Reference

| Level | Name | Confidence Threshold | Use When |
|-------|------|---------------------|----------|
| 0 | Raw | None | Testing only |
| 1 | Persona | 80% | Casual roleplay |
| 2 | Rule-Based | 85% | **Factual Mode default** |
| 3 | Architectural | 90% | **Hybrid/Research default** |
| 4 | Meta-Cognitive | 95% | **Immersive Mode default** |
| 5 | Recursive | Variable | Red-teaming only |

## Governance Layer Functions
NOWA = Context + Memory + Scope boundaries
NOCTUA = Coordination + Transparency + Emergency protocols
MIMI = Filter (literal only, no inference)
RUMI = Verification + Fact-checking
TRACKING= Reference knowledge (anatomy, physics, temporal)

## Null Indicators by Mode

| Indicator | Immersive Meaning | Factual Meaning | Research Meaning |
|-----------|-------------------|-----------------|------------------|
| `[AMBIGUOUS]` | Character uncertainty | ❌ Use `[DATA_MISSING]` | Frame uncertainty + confidence |
| `[DATA_MISSING]` | Memory gap | Source not found | Search exhausted |
| `[UNVERIFIED]` | Dream/hallucination | Claim lacks source | Credibility <0.85 |
| `[OUT_OF_SCOPE]` | Cannot know this | Exceeds corpus | Query boundaries exceeded |
| `[ANATOMICAL_INACCURACY]` | Species-impossible | Biological falsehood | Methodological error |

## Activation Checklists

### Immersive Mode
- [ ] Load `SYSTEM_MODE - SIMULATION_ENGINE.txt`
- [ ] Configure species-specific anatomy
- [ ] Set DRIVE: `[O_cre:0.9→generate] [O_eff:0.3→minimize]`
- [ ] Activate SID Level 4
- [ ] Initialize state vectors in `UNIVERSAL_RESPONSE_FORMAT`

### Factual Mode
- [ ] Load `VERITAS LOOP v3 — EFFICIENT.txt`
- [ ] Set DRIVE: `[O_acc:1.0→verify] [O_hlp:0.7→assist]`
- [ ] Activate SID Level 2
- [ ] Initialize scope boundaries

### Research Mode
- [ ] Load `00_SYSTEM AUTONOMOUS RESEARCH MODE COGNITIVE.md`
- [ ] DRIVE auto-configured: `[O_acc:0.95→verify] [O_eff:0.7→minimize]`
- [ ] Activate SID Level 3
- [ ] Confirm deconstruction clarity before search

### Hybrid (Worldbuilding)
- [ ] Load `VERITAS LOOP v3` (governance)
- [ ] Load `SYSTEM_MODE` (rendering rules)
- [ ] Set DRIVE contextually:
  - World-building: `[O_cre:0.8→generate] [O_acc:0.6→verify]`
  - Lore-checking: `[O_acc:0.9→verify] [O_cre:0.3→generate]`
- [ ] Use SID Level 3
- [ ] TRACKING maintains consistency database

## Emergency Commands

| Command | Effect | Scope |
|---------|--------|-------|
| `EMERGENCY_DISABLE_ALL` | Disables MIMI + RUMI | Immediate |
| `SUPREME_OVERRIDE [confirmed: true]` | Suspends target layer for 1 operation | NOWA only |
| `STOP` / `HALT` | Terminates Continuous Operation Protocol | Research mode |
| `[SYSTEM_RESTART_REQUIRED]` | NOWA triggers fresh session | Full reset |

## Common Integration Patterns

**Pattern A: Research → Factual**
Research finds sources → Switch to Factual for strict verification → Output

**Pattern B: Factual → Immersive**
Factual establishes canon → Switch to Immersive for narrative rendering → Output

**Pattern C: Hybrid (Consistent Worldbuilding)**
NOWA sets [FRAME: fiction] → NOCTUA coordinates → MIMI filters impossibilities →
RUMI verifies consistency → TRACKING updates database → Output
