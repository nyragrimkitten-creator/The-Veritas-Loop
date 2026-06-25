---

### 📄 `security.md`

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
