```markdown
# Advanced Deterministic Inference & Somatic Simulation Architectures

Welcome to the repository. This project contains a suite of advanced, production-grade system prompts designed to enforce strict semantic constraints, prevent hallucination through strict context tracking, and model high-fidelity, somatic state-machine simulations. 

Rather than relying on continuous semantic spaces or probabilistic approximation, these prompts treat Large Language Model (LLM) inference as a discrete, multi-layered execution engine.

---

## 🏗️ System Architecture Overview

These components form an advanced, full-stack prompt execution pipeline. They transition from absolute structural oversight down to a highly visceral, state-driven rendering output:

```text
┌─────────────────────────────────────────────────────────────┐
│             LAYER 0: GOVERNANCE & CONTEXT                   │
│             THE_VERITAS_LOOP.json                          │
│             (Veto Power, Memory Authority, Schema Auditing)  │
└──────────────────────────────┬──────────────────────────────┘
                               │ Passes Clean Context
                               ▼
┌─────────────────────────────────────────────────────────────┐
│             LAYER 1: COGNITIVE GATEKEEPER                  │
│             SID v2_5-HYBRID.md                             │
│             (Literal Intent Parser, 3-Layer Fact Gating)    │
└──────────────────────────────┬──────────────────────────────┘
                               │ Authorizes Inference Bounds
                               ▼
┌─────────────────────────────────────────────────────────────┐
│             LAYER 2: STATE VECTOR TRACKING                 │
│             UNIVERSAL_RESPONSE_FORMAT.yaml                  │
│             (Delta Logs, Physiological & Environmental Metrics)│
└──────────────────────────────┬──────────────────────────────┘
                               │ Feeds Vector Deltas
                               ▼
┌─────────────────────────────────────────────────────────────┐
│             LAYER 3: SOMATIC RENDERING CORE                 │
│             SYSTEM_MODE - SIMULATION_ENGINE.txt            │
│             (Fragmented Present-Participle Narrative Output)│
└─────────────────────────────────────────────────────────────┘

```

---

## 📂 File Registry & Descriptions

### 1. `THE_VERITAS_LOOP.json`

* **Role:** Supreme Governance, Memory, and Context Management.
* **Mechanism:** Implements a strict JSON-schema workflow split into discrete system agents: `NOWA` (Supreme Context Authority), `NOCTUA` (Meta-cognitive Enforcer), `MIMI` (Content Filter), and `RUMI` (Default Verification Filter).
* **Key Feature:** Uses global null indicators (such as `[SCOPE_VIOLATION]`, `[CIRCULAR_BLOCKED]`, and `[REFERENCE_TO_FORGOTTEN]`) to hard-abort processing if an internal subsystem attempts to overreach its operational boundaries or fabricate missing contextual data.

### 2. `SID v2_5-HYBRID.md`

* **Role:** Pragmatic Semantic Gatekeeper & Narrative Interpreter.
* **Mechanism:** Utilizes a custom **Literal Intent Parser (LIP)** syntax script (`[DIRECTIVE] [OBJECT] [PARAMS] [FRAME]`) to parse incoming user commands against a rigid 3-Layer Cognitive Model.
* *Layer 1 (Observation):* Directly stated facts (100% confidence).
* *Layer 2 (Experiential Inference):* Plausible internal states, sensory framing, and mood (70% confidence). Only unlocked under explicit narrative frames.
* *Layer 3 (Meaning Attribution):* Deep thematic significance (85% confidence). Requires an explicit `[MEANING_AUTHORIZED]` token flag.


* **Key Feature:** Features a compiled metaphor translation system that processes "Soft Symbolism" as valid character perception while reverting unauthorized "Hard Symbolism" back to a strict literal reading.

### 3. `UNIVERSAL_RESPONSE_FORMAT.yaml`

* **Role:** Structural Output State-Vector Sheet.
* **Mechanism:** Implements a compact, structured database tracking syntax for state-machine loops. Every output cycle updates numerical system indicators across multiple key matrices:
* `P1 / P2`: Core physical attributes (Health, Hydration, Bladder, Core Temp, Scent).
* `M1 / M2`: Psychological states (Arousal, Embarrassment, Focus, Cognitive Capacity).
* `B1 / B2`: Biological/Anatomical focus trackers (Pulse, Muscles, Pupil response).
* `V / H / K`: Environmental threat calculations, supply tracking, and apparel degradation status.



### 4. `SYSTEM_MODE - SIMULATION_ENGINE.txt`

* **Role:** Somatic Narrative Output Renderer.
* **Mechanism:** This prompt enforces a highly restricted, visceral prose-generation style. It strips abstract descriptions and psychological conclusions, forcing the model to render internal states exclusively through structural micro-reactions.
* **Key Stylistic Invariants:**
* Mandatory fragmented sentence structures that mirror natural breathing pauses.
* Present participles must dominate all verb phrases.
* Prohibits emotional abstractions (e.g., writing *"she felt anxious"* is blocked and must be written as *"throat tightening, eyes burning, chest hollow"*).
* Maintains a constant "physiological hum" across all scenes, ensuring the character's physical presence is never entirely static or neutral.



---

## 🚀 Deployment Instructions

### Option A: The Full Stack (Recommended)

To run a completely locked-down, ultra-grounded visceral narrative simulation, initialize your LLM session by providing all four documents in order:

1. Load `THE_VERITAS_LOOP.json` to configure the baseline systemic firewall.
2. Initialize `SID v2_5-HYBRID.md` to establish the semantic boundary controls.
3. Inject `SYSTEM_MODE - SIMULATION_ENGINE.txt` along with `UNIVERSAL_RESPONSE_FORMAT.yaml` to configure the active runtime parser.

### Option B: The Pure Logical Framework

If your goal is purely data analysis, verification, or structured code generation without narrative prose, deploy only `THE_VERITAS_LOOP.json` and `SID v2_5-HYBRID.md`. Set `[FRAME: analytical]` to completely disable Layer 2 and Layer 3 expansions, locking the engine into a pure Layer 1 literal processing loop.

---

## 🛠️ Contribution and Extension Guidelines

* **Prompt Stability:** When modifying the system schemas, avoid adding conversational explanations or general instructions. Use explicit rules, logical conditions (`IF/THEN`), and clear error tokens to prevent semantic leakage.
* **Formatting:** If editing configuration files or prompts locally on Windows machines, verify your editor configuration matches **UTF-8 encoding** and preserves appropriate line endings (**LF** for UNIX deployment targets) to prevent formatting corruption during execution.

```
