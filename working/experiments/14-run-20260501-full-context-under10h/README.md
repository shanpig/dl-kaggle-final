# Experiment 14 - Full Context (Lecture+Hint) Under 10h

Date: 2026-05-01

Base:
- Copied from Experiment 13 submission notebook (which is based on Exp12 answer-token-loss)

Goal:
- Use all modalities and context fields in training/eval prompt:
  - image + question + choices + lecture + hint
- Keep expected runtime within Kaggle 10-hour notebook limit.

Key config changes from Exp13:
- `run_name`: `qlora-fullctx-<timestamp>`
- `mode.do_val_eval`: `True`
- `mode.do_test_inference`: `False`
- `prompting.use_lecture`: `True`
- `prompting.use_hint`: `True`
- `prompting.lecture_max_chars`: `0` (no clip)
- `prompting.hint_max_chars`: `0` (no clip)
- `screening.max_train_samples`: `None` (full train)
- `screening.max_val_samples`: `400` (runtime-controlled validation)

Runtime control strategy:
- Keep 1 epoch, 4-bit QLoRA, batch size 1, grad accumulation 16, img_size 192.
- Disable test inference for this experiment (validation-first).
