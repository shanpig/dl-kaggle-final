# Experiment 04: QLoRA MVP (No Ablation)

Source: `02-run-20260425-202038-qlora-screening-v1`
Notebook: `baseline-starter-notebook__qlora-mvp__20260430-152031.ipynb`

## Goal
Get one successful end-to-end QLoRA training run before any ablations.

## Config used (fixed)
- `num_epochs=1`
- `max_train_samples=256`
- `max_val_samples=128`
- `per_device_train_batch_size=1`
- `gradient_accumulation_steps=16`
- `use_hint=False`
- `use_lecture=False`
- `img_size=192`
- `do_test_inference=False`
- `RUN_BASELINE_SECTION4=False`

## Success criteria
- Training completes without CUDA error/OOM
- Writes `config.json`, `train_metrics.json`, `best_adapter/`, `val_summary.json`
