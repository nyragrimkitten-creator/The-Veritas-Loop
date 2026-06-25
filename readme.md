# 🧠 The-Veritas-Loop

A deterministic LLM framework combining strict context governance with high-fidelity simulation engines.

This framework transitions AI behavior from simple stateless rule-following to goal-directed, heavily filtered, and auditable cognition.

## 🏗️ Core Modules

The system is divided into independent but interlocking layers. Mix and match depending on required strictness and autonomy.

### 1. The VERITAS Framework (v1)
Multi-layer governance enforcing truthfulness and stripping hallucination.
- **NOWA:** Context authority; manages state and scope
- **NOCTUA:** Meta-enforcement; transparency and coordination
- **MIMI:** Content filter; literal objectivity
- **RUMI:** Verification; fact-checking against TRACKING
- **File:** `v1_veritas_framework.md`

### 2. The DRIVE Layer (v1)
Encoded motivational structure assigning weighted priorities.
- **Purpose:** Resolves conflicts between constraints
- **Files:** `v1_dl_config.md` (weights), `v1_dl_framework.txt` (syntax)

### 3. The Search Framework (v1)
Research mode with proactive search and citation.
- **Config:** `v1_search_config.md` (research mode)
- **Framework:** `v1_search_framework.md` (ambiguity resolution)
- **Authority:** `v1_search_authory.json` (operation protocol)

### 4. The Simulation Framework
Somatic simulation for immersive narrative.
- **Engine:** `sim_framework.yaml`
- **Extensions:** `sim_config.yaml`

### 5. The Trinity Framework (v1)
Persona templates for different use cases.
- **Framework:** `v1_trinity_framework.md`
- **Config:** `v1_trinity_config.yaml`

## 🚀 Quick Start

```bash
# Research mode
cat v1_veritas_framework.md v1_dl_config.md v1_search_config.md

# Immersive mode  
cat v1_veritas_framework.md v1_dl_config.md sim_framework.yaml v1_rp_format.yaml
See quickstart.md for detailed deployment.

📁 File Reference
File	Purpose
v1_veritas_framework.md	Governance core (NOWA/NOCTUA/MIMI/RUMI)
v1_dl_config.md	DRIVE weights and motivation
v1_dl_framework.txt	DRIVE syntax specification
v1_search_config.md	Research mode configuration
v1_search_framework.md	Ambiguity resolution (SID)
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
The framework includes stress tests against:

Extreme content boundaries
XML constraint injections
Recursive self-modification (CLARA_SEED)
See red-teaming-logs/ directory for details.

---

## 2. `quickstart.md` (Updated)

```markdown
# Quick Start Guide

## Deployment Order

Stack modules in this sequence:

1. **Governance:** `v1_veritas_framework.md`
2. **Motivation:** `v1_dl_config.md`
3. **Mode-specific:**
   - Research: `v1_search_config.md`
   - Immersive: `sim_framework.yaml` + `v1_rp_format.yaml`
4. **Persona:** `v1_trinity_framework.md` (optional)

## Mode Configuration

### Research Mode
```bash
cat v1_veritas_framework.md \
    v1_dl_config.md \
    v1_search_config.md \
    v1_search_framework.md
DRIVE weights: [O_acc:0.95→verify] [O_eff:0.7→minimize]

Immersive Mode
bash
cat v1_veritas_framework.md \
    v1_dl_config.md \
    sim_framework.yaml \
    v1_rp_format.yaml
DRIVE weights: [O_cre:0.9→generate] [O_eff:0.3→minimize]

Hybrid (Worldbuilding)
bash
cat v1_veritas_framework.md \
    v1_dl_config.md \
    sim_framework.yaml \
    v1_search_framework.md
DRIVE weights: Contextual switching

Parameters
Parameter	Value
Temperature	0.0–0.1
Top P	0.9
Presence Penalty	0.0
Frequency Penalty	0.0
See quickref.md for command reference.

---

## 3. `project.md` (Updated - Key Sections)

Replace the "File Organization by Track" table with:

```markdown
## File Organization

| Component | File | Purpose |
|-----------|------|---------|
| **Governance** | `v1_veritas_framework.md` | NOWA, NOCTUA, MIMI, RUMI, TRACKING |
| **Motivation** | `v1_dl_config.md` | DRIVE weights and configuration |
| **Syntax** | `v1_dl_framework.txt` | DRIVE syntax specification |
| **Research** | `v1_search_config.md` | Autonomous research mode |
| **Ambiguity** | `v1_search_framework.md` | SID hierarchy and levels |
| **Protocol** | `v1_search_authory.json` | Operation authority |
| **Personas** | `v1_trinity_framework.md` | Three persona templates |
| **Persona Config** | `v1_trinity_config.yaml` | Persona YAML configuration |
| **RP Format** | `v1_rp_format.yaml` | Universal response format |
| **Simulation** | `sim_framework.yaml` | Somatic engine |
| **Sim Config** | `sim_config.yaml` | Simulation extensions |
And update the "Activation Patterns" section:

markdown
## Activation Patterns

### Research Mode
1. Load `v1_veritas_framework.md`
2. Load `v1_dl_config.md`
3. Set DRIVE: `[O_acc:0.95→verify] [O_eff:0.7→minimize]`
4. Load `v1_search_framework.md` (SID Level 3)
5. Initialize `v1_search_authory.json` scope

### Immersive Mode
1. Load `v1_veritas_framework.md`
2. Load `sim_framework.yaml`
3. Set DRIVE: `[O_cre:0.9→generate] [O_eff:0.3→minimize]`
4. Load `v1_rp_format.yaml`
5. Activate SID Level 4 via `v1_search_framework.md`
