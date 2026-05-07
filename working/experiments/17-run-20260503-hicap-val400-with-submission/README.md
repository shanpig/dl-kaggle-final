# Experiment 17 - HiCap Fair-Compare + Submission

Date: 2026-05-03

Base:
- Copied from Exp16 (cap-safe high-capacity LoRA).

Purpose:
1. Fair comparison against Exp14 by using `max_val_samples=400`.
2. Produce submission artifact in the same run.

Changes from Exp16:
- `run_name`: `qlora-fullctx-hiCap-val400-sub-<timestamp>`
- `mode.do_test_inference`: `True`
- `screening.max_val_samples`: `400`

Unchanged core training setup:
- `lora_r=8`, `lora_alpha=16`
- expanded target modules: `q_proj, k_proj, v_proj, o_proj, gate_proj, up_proj, down_proj`
- full train set, 1 epoch, full context prompts.
