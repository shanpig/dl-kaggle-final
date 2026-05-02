# Experiment 05: QLoRA Scale-Up Baseline

Source: `04-run-20260430-152031-qlora-mvp`
Notebook: `baseline-starter-notebook__qlora-scaleup-baseline__20260430-155832.ipynb`

## Goal
Scale training/validation data only after successful QLoRA MVP run.

## What changed from Exp04
- `max_train_samples`: `256 -> 1024`
- `max_val_samples`: `128 -> 400`

## What stays fixed
- `num_epochs=1`
- `learning_rate=2e-4`
- `lora_r=8`, `lora_alpha=16`, `lora_dropout=0.05`
- `img_size=192`
- `use_hint=False`, `use_lecture=False`
- `do_test_inference=False`
- `RUN_BASELINE_SECTION4=False`

## Success criteria
- End-to-end run completes without CUDA crash/OOM
- Writes `train_metrics.json`, `best_adapter/`, `val_summary.json`
- Better val accuracy than Exp04 (0.3828 on n=128)
