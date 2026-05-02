# Experiment Run: qlora-ablation-a1

Run timestamp: 2026-04-26 15:04:43 (local)
Source notebook: `working/experiments/02-run-20260425-202038-qlora-screening-v1/baseline-starter-notebook__qlora-screening-v1__20260425-202038.ipynb`
Notebook for this run: `baseline-starter-notebook__qlora-ablation-a1__20260426-150443.ipynb`

## Why this run
Previous run timed out at 43,200 seconds. This run is the first one-by-one ablation with bounded runtime.

## Runtime-safe defaults for this run
- `num_epochs = 1`
- `max_train_samples = 1200`
- `max_val_samples = 400`
- `do_test_inference = False`
- `RUN_BASELINE_SECTION4 = False` (skips costly baseline val/test loops)

## Expected outputs
- `results/<run_name>/config.json`
- `results/<run_name>/train_metrics.json`
- `results/<run_name>/val_strict_eval_predictions.csv`
- `results/<run_name>/val_summary.json`

## Next ablations (one-by-one)
Follow `ablation-queue.csv` in order and run only one config per Kaggle commit.