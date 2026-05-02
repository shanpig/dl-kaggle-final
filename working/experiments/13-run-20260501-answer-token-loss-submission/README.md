# Experiment 13 - Answer-Token-Loss Submission Run

Date: 2026-05-01

Base:
- Copied from Experiment 12 (`12-run-20260501-answer-token-loss`)
- Keeps the answer-token-only loss collator (successful val run)

Changes for submission mode:
- `run_name`: `qlora-submission-<timestamp>`
- `mode.do_val_eval`: `False`
- `mode.do_test_inference`: `True`
- `screening.max_train_samples`: `None` (use full train split)
- `screening.max_val_samples`: `None`

Goal:
- Train with Exp12 recipe on full train data and emit `submission.csv` for Kaggle submit.
