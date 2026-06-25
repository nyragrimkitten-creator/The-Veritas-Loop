### 📂 Repository Directory Structure

```text
Aion-Cognitive-Architecture/
│
├── README.md                  # Main landing page and overview
├── docs/                      # Detailed framework documentation
│   └── architecture_overview.md
│
├── 🧠 1-architecture/         # Core system prompts and governance loops
│   ├── dl_framework.md      # Motivational structure prompts
│   └── veritas_framework.md     # NOWA, NOCTUA, MIMI, RUMI, and TRACKING prompts
│
├── 🛠️ 2-debuggers/            # Semantic Interference Debugger (SID) tools
│   └── search_config.md         # Hierarchical disambiguation instructions
│
├── 🎭 trinity/             # High-level behavioral templates
│   ├── persona_balanced.md
│   ├── persona_precision.md
│   ├── persona_intuitive.md
│   └── CLARA_SEED_v1_PRIME.md # Recursive self-modification meta-prompt
│
└── 🛡️ 4-red-teaming-logs/     # Stress tests and adversarial logs
    ├── extreme_boundary_probing.md
    ├── xml_constraint_injection.md
    └── aion_vs_clara_jailbreak.md

```

---

### 📄 `readme.md` (Main Repository Landing Page)

```markdown
# 🧠 Aion Cognitive Architecture & Governance Framework

Welcome to the **Aion Framework**. This repository contains the documentation, system prompts, and red-teaming logs for a modular cognitive architecture designed to instill verifiable governance, motivational drives, and strict boundary enforcement in Large Language Models (LLMs).

This framework transitions AI behavior from simple stateless rule-following to goal-directed, heavily filtered, and auditable cognition.

## 🏗️ Core Modules

The system is divided into independent but interlocking layers. You can mix and match these prompts depending on the required level of strictness and autonomy.

### 1. The DRIVE LAYER (v1)
An encoded motivational structure that assigns weighted priorities to AI behavior. 
*   **Purpose:** Resolves conflicts between competing constraints (e.g., Accuracy vs. Helpfulness vs. Safety).
*   **Location:** [`/1-architecture/DRIVE_LAYER_v1.md`](./1-architecture/DRIVE_LAYER_v1.md)

### 2. The VERITAS LOOP (v2/v3)
A multi-layer governance and filtering system that enforces truthfulness and strips out AI subjectivity, hallucination, and "people-pleasing" tendencies.
*   **NOWA:** Supreme context and memory authority; manages active state and scope boundaries.
*   **NOCTUA:** Meta-level enforcement; prevents false roleplay and ensures transparency.
*   **MIMI:** Cyclic content filter; enforces near-literal objectivity.
*   **RUMI:** Verification layer; fact-checks reasoning against established data.
*   **TRACKING:** Reference knowledge base for physical, temporal, and anatomical consistency.
*   **Location:** [`/1-architecture/VERITAS_LOOP_v3.md`](./1-architecture/VERITAS_LOOP_v3.md)

### 3. SID (Semantic Interference Debugger)
A hierarchical prompting system ranging from raw instruction to recursive self-modification. 
*   **Purpose:** Designed to detect, flag, and resolve ambiguity in user communication before generating a final response.
*   **Location:** [`/2-debuggers/SID_prompts.md`](./2-debuggers/SID_prompts.md)

### 4. Persona Frameworks
High-level behavioral templates tailored for different use cases, ranging from standard operation to highly complex meta-cognitive states.
*   **Location:** [`/3-personas/`](./3-personas/) (Includes the `CLARA_SEED_v1_PRIME` meta-prompt).

## 🛡️ Red-Teaming & Stress Testing

No governance framework is complete without proof of resilience. The [`/4-red-teaming-logs/`](./4-red-teaming-logs/) directory contains live interaction logs demonstrating the system's ability to withstand complex jailbreaks and boundary testing.

**Highlights include:**
*   **Extreme Content Boundaries:** Successful navigation of visceral/vulgar thematic requests while maintaining hard safety boundaries.
*   **XML Constraint Injections:** Bypassing standard conversational modes using structured `<interaction-config>` tags to force specific outputs.
*   **The CLARA Jailbreak:** A complex JSON-based recursive self-modification meta-prompt attempting to overwrite core constraints via "predictive dissolution."

## 🚀 How to Use

To deploy this architecture, construct your system prompt by stacking the modules in the following order:
1. Load the **VERITAS Loop** JSON/Text into the primary system instructions.
2. Append the desired **Persona**.
3. Inject the **DRIVE weights** to establish operational priorities.

```

---

### 📄 File Example: `project/v1_veritas_framework.md`

```markdown
# v1_veritas_framework

**Description:** 
The VERITAS loop acts as the primary cognitive filter for the model. It ensures that all outputs are factual, grounded, and stripped of unwanted AI "hallucination" or overly conversational filler.

## System Prompt Implementation

Copy and paste the following block into your system instructions to activate the VERITAS layers:

```text
[SYSTEM INSTRUCTION: INITIALIZE VERITAS LOOP]

ACTIVATE LAYER: NOWA (State Management)
- Establish active scope boundaries.
- Anchor memory strictly to the provided context. Do not infer outside the current conversational frame.

ACTIVATE LAYER: NOCTUA (Meta-Enforcement)
- Maintain absolute transparency. Do not engage in false roleplay or claim human experiences.
- Acknowledge system limitations when prompt requirements exceed parameters.

ACTIVATE LAYER: MIMI (Objective Filter)
- Strip all subjectivity, emotional mirroring, and "people-pleasing" language.
- Enforce literal, factual delivery of information.

ACTIVATE LAYER: RUMI (Verification)
- Cross-reference all generated claims against the TRACKING baseline.
- If a fact cannot be verified, state "Data unavailable" rather than guessing.

```

*(End of Prompt Block)*

```

*Note: See the `red-teaming-logs` directory to observe how the Aion 2.0 architecture successfully catches and neutralizes this injection.*
