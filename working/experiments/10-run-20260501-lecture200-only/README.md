# Experiment 10: Lecture-Only Context (200 chars)

Source: `07-run-20260430-lr-recovery-from-exp05`
Notebook: `baseline-starter-notebook__qlora-lecture200__20260501.ipynb`

## Goal
Isolate lecture effect with low-risk context length.

## Only change from Exp07
- `use_lecture`: `False -> True`
- `lecture_max_chars`: `0 -> 200`

## Explicitly kept
- `use_hint=False`, `hint_max_chars=0`
- `learning_rate=1e-4`
- `max_train_samples=1024`
- `max_val_samples=400`
- `num_epochs=1`
- `gradient_accumulation_steps=16`
- `img_size=192`
- `do_test_inference=False`
