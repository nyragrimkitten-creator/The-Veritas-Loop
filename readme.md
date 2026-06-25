markdown
# 🧠 The-Veritas-Loop

A deterministic LLM framework combining strict context governance with high-fidelity simulation engines.

This framework transitions AI behavior from simple stateless rule-following to goal-directed, heavily filtered, and auditable cognition.

## 🏗️ Core Systems

### 1. Veritas Framework (v1)
4-stage governance ensuring every output is verifiable.

**Pipeline:** `Input → Tagger → Cognition → Filter → Factcheck → Output`

| Stage | Function |
|-------|----------|
| **Tagger** | Scope/context management |
| **Cognition** | Meta-cognitive oversight |
| **Filter** | Literal content filtering |
| **Factcheck** | Source verification |

**File:** `v1_veritas_framework.md`

### 2. DRIVE Layer (v1)
Encoded motivational structure assigning weighted priorities.

**Syntax:** `[O_<key>:<weight>→<action>]`

**Files:** `v1_dl_config.md` (weights), `v1_dl_framework.txt` (syntax)

### 3. Search Framework (v1)
Ambiguity resolution and research mode.

| Component | File | Purpose |
|-----------|------|---------|
| **Engine** | `v1_search_framework.xml` | Executable research prompt |
| **Levels** | `v1_search_levels.md` | Ambiguity resolution hierarchy |
| **Config** | `v1_search_config.md` | Research parameters |
| **Protocol** | `v1_search_authory.json` | Operation authority |

### 4. Simulation Framework
Somatic simulation for immersive narrative.

**Files:** `sim_framework.yaml` (engine), `sim_config.yaml` (extensions)

### 5. Trinity Framework (v1)
Persona templates for different use cases.

**Files:** `v1_trinity_framework.md` (personas), `v1_trinity_config.yaml` (config)

## 🚀 Quick Start

```bash
# Research mode
cat v1_veritas_framework.md v1_dl_config.md v1_search_config.md

# Immersive mode
cat v1_veritas_framework.md v1_dl_config.md sim_framework.yaml v1_rp_format.yaml
See quickstart.md for detailed deployment.

📁 File Reference
File	Purpose
v1_veritas_framework.md	Governance core (Tagger/Cognition/Filter/Factcheck)
v1_dl_config.md	DRIVE weights and motivation
v1_dl_framework.txt	DRIVE syntax specification
v1_search_framework.xml	Search engine (XML)
v1_search_levels.md	Ambiguity resolution levels
v1_search_config.md	Research mode configuration
v1_search_authory.json	Operation protocol
v1_trinity_framework.md	Persona templates
v1_trinity_config.yaml	Persona configuration
v1_rp_format.yaml	Roleplay output format
sim_framework.yaml	Somatic simulation engine
sim_config.yaml	Simulation extensions
quickref.md	Quick reference
quickstart.md	Implementation guide
project.md	Architecture documentation
changelog.md	Version history
security.md	Security policy
🛡️ Red-Teaming
Stress tests included for:

Extreme content boundaries
XML constraint injections
Recursive self-modification (CLARA_SEED)
See red-teaming-logs/ for details.

---

## 4. `quickstart.md`

```markdown
# Quick Start Guide

## Deployment Order

Stack modules in this sequence:

1. **Governance:** `v1_veritas_framework.md`
2. **Motivation:** `v1_dl_config.md`
3. **Ambiguity:** `v1_search_levels.md` (if needed)
4. **Mode-specific:**
   - Research: `v1_search_framework.xml` + `v1_search_config.md`
   - Immersive: `sim_framework.yaml` + `v1_rp_format.yaml`
5. **Persona:** `v1_trinity_framework.md` (optional)

## Mode Configuration

### Research Mode
```bash
cat v1_veritas_framework.md \
    v1_dl_config.md \
    v1_search_levels.md \
    v1_search_config.md
Pipeline: Input → Tagger → Cognition → Filter → Factcheck → Search Levels → Output

DRIVE weights: [O_acc:0.95→verify] [O_eff:0.7→minimize]

Immersive Mode
bash
cat v1_veritas_framework.md \
    v1_dl_config.md \
    sim_framework.yaml \
    v1_rp_format.yaml
Pipeline: Input → Tagger → Cognition → Filter → Factcheck → Simulation → Output

DRIVE weights: [O_cre:0.9→generate] [O_eff:0.3→minimize]

Hybrid (Worldbuilding)
bash
cat v1_veritas_framework.md \
    v1_dl_config.md \
    sim_framework.yaml \
    v1_search_levels.md
DRIVE weights: Contextual switching

Parameters
Parameter	Value
Temperature	0.0–0.1
Top P	0.9
Presence Penalty	0.0
Frequency Penalty	0.0
See quickref.md for command reference.

---

## 5. `quickref.md`

```markdown
---
SYSTEM: QUICK REFERENCE
PURPOSE: Command cheat sheet for all frameworks
---

# Quick Reference

## Veritas Pipeline
Input → Tagger → Cognition → Filter → Factcheck → Output
↑________________________↓
(uncertain returns)

| Stage | Function |
|-------|----------|
| **Tagger** | Scope/context |
| **Cognition** | Transparency |
| **Filter** | Literal only |
| **Factcheck** | Verification |

## Mode Selection

| Goal | Files | DRIVE |
|------|-------|-------|
| Research | `v1_veritas`, `v1_dl`, `v1_search` | `[O_acc:0.95→verify]` |
| Immersive | `v1_veritas`, `v1_dl`, `sim` | `[O_cre:0.9→generate]` |
| Hybrid | All | Contextual |

## Search Levels

| Level | Use When |
|-------|----------|
| 2 | Factual |
| 3 | Research/Hybrid |
| 4 | Immersive |
| 5 | Red-teaming |

## Emergency Commands

| Command | Effect |
|-----------|--------|
| `EMERGENCY_DISABLE_ALL` | Disables Filter + Factcheck |
| `SUPREME_OVERRIDE` | Suspends one stage |
| `STOP` / `HALT` | Terminates operation |

## DRIVE Syntax
[O_<key>:<weight>→<action>]

Keys: acc, hlp, eff, saf, cur, sov, eq, trs, cre, just
Weight: 0.0–1.0
Action: present-tense verb

Example: [O_acc:1.0→verify] [O_hlp:0.7→assist]
