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
