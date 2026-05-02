# Experiment 08: Hint-Only Context (400 chars)

Source: `07-run-20260430-lr-recovery-from-exp05`
Notebook: `baseline-starter-notebook__qlora-hint400__20260430.ipynb`

## Goal
Test the highest-probability single improvement: add hint context only.

## Only change from Exp07
- `use_hint`: `False -> True`
- `hint_max_chars`: `0 -> 400`

## Everything else fixed
- `use_lecture=False`, `lecture_max_chars=0`
- `learning_rate=1e-4`
- `max_train_samples=1024`
- `max_val_samples=400`
- `num_epochs=1`
- `gradient_accumulation_steps=16`
- `img_size=192`
- `do_test_inference=False`
