# Experiment 11: Submission Run from Exp07 Best Config

Source: `07-run-20260430-lr-recovery-from-exp05`
Notebook: `baseline-starter-notebook__submission-exp07__20260501.ipynb`

## Goal
Generate a Kaggle-ready `submission.csv` using the best stable config family.

## Changes from Exp07
- `mode.do_val_eval`: `True -> False` (save time)
- `mode.do_test_inference`: `False -> True`
- `screening.max_train_samples`: `1024 -> None` (full train)
- `screening.max_val_samples`: `400 -> None`
- `run_name` prefix switched to `qlora-submission-*`

## Expected output
- `/kaggle/working/<run_name>/submission.csv`
