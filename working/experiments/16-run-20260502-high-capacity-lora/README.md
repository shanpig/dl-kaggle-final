# Experiment 16 - High-Capacity LoRA (Cap-Safe)

Date: 2026-05-02

Base:
- Copied from Exp14 full-context notebook.

Issue observed:
- Previous settings exceeded cap: 9,568,256 trainable params > 5,000,000.
- Run failed at assertion check in training setup.

Reason for this change:
- Competition rule requires trainable parameters to stay below 5M.
- We reduced LoRA rank while keeping broader module coverage so the run remains valid and still tests the intended strategy (attention + MLP adaptation).

Current cap-safe config:
- `lora_r`: 8
- `lora_alpha`: 16
- `target_modules`:
  - `q_proj, k_proj, v_proj, o_proj, gate_proj, up_proj, down_proj`

Rationale:
- Keep expanded module coverage (attention + MLP) while reducing rank to stay under the 5M trainable parameter rule.
