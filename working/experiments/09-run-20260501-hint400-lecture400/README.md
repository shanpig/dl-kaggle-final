# Experiment 09: Hint + Lecture (400/400)

Source: `08-run-20260430-hint-only-400`
Notebook: `baseline-starter-notebook__qlora-hint400-lecture400__20260501.ipynb`

## Goal
Test incremental context gain after hint-only run.

## Only change from Exp08
- `use_lecture`: `False -> True`
- `lecture_max_chars`: `0 -> 400`

## Everything else fixed
- `use_hint=True`, `hint_max_chars=400`
- `learning_rate=1e-4`
- `max_train_samples=1024`
- `max_val_samples=400`
- `num_epochs=1`
- `gradient_accumulation_steps=16`
- `img_size=192`
- `do_test_inference=False`
