# Experiment Run: qlora-screening-v1

Run timestamp: 2026-04-25 20:20:38 (local)
Parent run: `run-20260425-191921-kaggle-friendly-v1`
Copied notebook: `baseline-starter-notebook__qlora-screening-v1__20260425-202038.ipynb`

## Goal
Start QLoRA fine-tuning with strict validation-first screening. We only run full test inference/submission for top candidates.

## Baseline runtime reference
- Strict evaluator baseline runtime: ~42 minutes (val+test pipeline)

## What this run adds
- Experiment matrix (`experiment-matrix.md`, `experiment-matrix.csv`)
- Config-first approach for tuning reproducibility
- Notebook is prewired for QLoRA training + strict val screening

## Expected per-run artifacts
- `config.json`
- `train_metrics.json`
- `val_strict_eval_predictions.csv`
- `val_summary.json`
- `submission.csv` (only for promoted runs)
- `best_adapter/` (for promoted runs)

## Changelog
### 2026-04-25 20:20:38 - Run initialized
- Changed: Created new experiment folder and copied notebook from strict-eval-success run.
- Reason: Isolate QLoRA trials from previous stable pipeline.
- Expected impact: Faster iteration and clear comparability across runs.
- Validation result: Pending execution.

### 2026-04-25 20:22:30 - QLoRA screening section appended
- Changed: Added Section 5 to notebook with config block, QLoRA model setup, LoRA cap check (<5M), training block, and strict val-screen/test-optional flow.
- Reason: Start fine-tuning from a reproducible config-first workflow while keeping strict evaluator unchanged.
- Expected impact: Enables controlled ablations with per-run artifacts (`config.json`, `train_metrics.json`, `val_summary.json`).
- Validation result: Pending Kaggle execution.

## First run suggestion (A1)
- Keep `CFG["mode"]["do_test_inference"] = False`
- Set prompt config:
  - `use_hint = False`
  - `use_lecture = False`
  - `hint_max_chars = 0`
  - `lecture_max_chars = 0`
- Keep LoRA and train defaults for first screen:
  - `lora_r = 8`, `lora_alpha = 16`, `learning_rate = 2e-4`, `num_epochs = 2`, `seed = 42`
