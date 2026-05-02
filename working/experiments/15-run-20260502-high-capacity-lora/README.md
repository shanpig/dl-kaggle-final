# Experiment 15 - High-Capacity LoRA (Near 5M Cap)

Date: 2026-05-02

Base:
- Copied from Exp14 full-context notebook.

Goal:
- Increase trainable parameter capacity from ~2.08M toward (but below) 5M.

Changes:
- `lora_r`: 8 -> 16
- `lora_alpha`: 16 -> 32
- `target_modules`:
  - from: `q_proj, k_proj, v_proj, o_proj`
  - to: `q_proj, k_proj, v_proj, o_proj, gate_proj, up_proj, down_proj`
- `run_name`: `qlora-fullctx-hiCap-<timestamp>`
- Runtime guard: `max_val_samples=300` (train still uses full train split)

Expected:
- Trainable params should increase significantly and remain below the hard cap of 5,000,000 enforced by assertion in the notebook.
