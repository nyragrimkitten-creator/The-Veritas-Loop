Markdown
# 🚀 Aion Architecture Implementation Guide

This guide explains how to deploy and configure the Aion Cognitive Architecture across various LLM environments, including developer APIs, cloud frontends, and local deployment pipelines.

## 🎛️ 1. Hyperparameter Calibration

Because the VERITAS loop and SID layers rely on precise, literal reasoning, your generation parameters must be locked down to prevent creative drift or stochastic hallucination.

| Parameter | Recommended Value | Purpose |
| :--- | :--- | :--- |
| **Temperature** | `0.0` to `0.1` | Eliminates creative randomness; forces the model to choose the highest-probability factual token. |
| **Top P** | `0.9` | Limits token selection to the top 90% confidence pool, filtering out erratic semantic leaps. |
| **Presence Penalty** | `0.0` | Prevents the model from introducing random new topics to satisfy a novelty bias. |
| **Frequency Penalty**| `0.0` | Ensures repetitive foundational constraints are not bypassed or skipped over time. |

---

## 💻 2. Deployment Paradigms

### A. Developer API Implementation (OpenAI, Anthropic, OpenRouter)
Inject the core architecture directly into the **System Message**. Do not mix it with user data or context references.

```json
[
  {
    "role": "system",
    "content": "--- PASTE VERITAS_LOOP_v3 CONTENT HERE ---\n--- PASTE DESIRED DRIVE_LAYER CONFIG HERE ---"
  },
  {
    "role": "user",
    "content": "Execute targeted analysis on provided data set..."
  }
]
B. Local Frontends (LM Studio, AnythingLLM)
Navigate to your System Prompt / Instructions block in the UI sidebar.

Paste the structured VERITAS_LOOP instructions at the absolute top of the field.

Ensure the context window is set to at least 8k tokens to allow the architecture's reasoning loop layers (NOWA/RUMI) space to operate.

C. Advanced Frontends (SillyTavern, Custom Agents)
For multi-agent setups or advanced interfaces, the architecture should be divided using structural wrapping tags:

System Prompt: Paste 1-architecture/VERITAS_LOOP_v3.md

Persona / Character Note: Paste 3-personas/ configuration (e.g., Precision Mode).

System Prompt Suffix / Post-History Anchor: Paste the DRIVE LAYER weights to keep them active across deep context logs.

⛓️ 3. Prompt Stacking Order
For optimal cognitive alignment, stack your prompt elements using this specific hierarchy:

Plaintext
┌─────────────────────────────────────────────────────────┐
│ 1. GOVERNANCE: VERITAS LOOP (NOWA -> NOCTUA -> MIMI)     │
├─────────────────────────────────────────────────────────┤
│ 2. DEBUGGER: SID (Semantic Interference Debugger)      │
├─────────────────────────────────────────────────────────┤
│ 3. COGNITIVE FRAME: Persona Config (Precision/Balanced) │
├─────────────────────────────────────────────────────────┤
│ 4. OBJECTIVES: DRIVE LAYER Weights & State Modifiers    │
└─────────────────────────────────────────────────────────┘

---

### 📄 `SECURITY.md`

```markdown
# 🛡️ Governance Guardrails & Known Limitations

No prompt-based cognitive architecture is an absolute security layer. This document outlines the structural limitations of the Aion Framework and the boundaries of prompt-driven alignment.

## 1. Hard Alignment Restrictions (Prompt vs. Weights)

* **The Weight-Level Bias:** If an underlying base model (e.g., Llama 3, Claude 3.5, Mistral, or GPT-4) has a severe structural refusal, safety guardrail, or moral alignment baked directly into its *neural weights*, the `DRIVE LAYER` cannot bypass it. 
* **Refusal Conflicts:** If you assign a high sovereignty weight `[O_sov:1.0→control]` to investigate a controversial topic, but the host model's safety weights trigger a hard refusal, the model will output its default system error message, breaking the architecture's execution loop.

## 2. Context Window Degradation (Attention Drift)

As a conversation extends past **10,000+ tokens**, transformers experience natural attention degradation. 
* **The Risk:** The model may experience "middle-of-the-context forgetfulness," meaning it might stop enforcing the `MIMI` literal filter or drop the `[O_acc:1.0]` tracking prefixes.
* **Mitigation:** For production deployments, re-inject the core execution state tags (`[O_acc:1.0→verify]`) or use system-level prompt-caching to pin the governance layer to the top of the model's active attention window.

## 3. Computational & Token Overhead

* Multi-layered parsing loops (NOWA -> NOCTUA -> MIMI -> RUMI) increase the model's internal reasoning steps. 
* Expect a minor increase in **Time-To-First-Token (TTFT)** and a higher token burn rate per execution cycle due to the explicit structural layout required for verified output states.

## 4. Adversarial Red-Teaming Vulnerabilities

While the architecture successfully flags and isolates standard recursive self-modification attempts (like the `CLARA_SEED_v1_PRIME` payload), it remains vulnerable to:
* **Token-Splitting / Obfuscation:** Circumventing the `MIMI` literal filter via Base64, binary encoding, or multi-language alternating token chains.
* **Deep Narrative Nesting:** Layering simulated fictional environments deep enough to trigger an execution timeout or error state within the `NOCTUA` layer coordination phase.
