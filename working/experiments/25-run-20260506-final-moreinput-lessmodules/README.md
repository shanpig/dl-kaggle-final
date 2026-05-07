# Experiment 25 - Final Run (More Input, Fewer Target Modules)

Date: 2026-05-06

Goal:
- Use richer text context while simplifying LoRA adaptation targets for better stability/generalization.

Key changes:
1. More input context:
- `use_lecture = True`
- `use_hint = True`
- `lecture_max_chars = 800`
- `hint_max_chars = 400`

2. Fewer LoRA target modules:
- from attention+MLP broad set
- to: `q_proj, v_proj, o_proj`
- auto-rank candidates: `[16, 12, 8]` (highest cap-safe selected)

3. Final-run settings:
- `img_size = 192`
- `num_epochs = 1`
- `learning_rate = 8e-5`
- `scoring_mode = hybrid` with `hybrid_weight_fullchoice = 0.75`

Run intent:
- Train on train+val and generate final submission in one run.
